<template>
	<div>
		<template v-if="mobileDrawAnim == '1'">
			<v-navigation-drawer fixed v-model="drawer" app>
				<v-list dense>
					<v-list-tile to="/">
						<v-list-tile-action>
							<v-icon large>home</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Home</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile href="/docs" target="_blank">
						<v-list-tile-action>
							<v-icon large>help</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Documentazione</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<!--
				<v-list-tile to="/help">
					<v-list-tile-action>
						<v-icon large>help</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title class="navEntry">Aiuto</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>
			-->
					<br>
					<v-divider>
					</v-divider>
					<br>
					<!--
				<v-list-tile to="/activity">
					<v-list-tile-action>
						<v-icon>open_in_new</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>Apri Attività</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>
				<v-list-tile to="/new">
					<v-list-tile-action>
						<v-icon>add</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>Nuova Attività</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>
				-->
					<h3>Attività</h3>
					<v-list-tile to="/activity/open">
						<v-list-tile-action>
							<v-icon>open_in_new</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title>Apri</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/activity/new">
						<v-list-tile-action>
							<v-icon>add</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title>Nuova</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<br>
					<v-divider>
					</v-divider>
					<br>
					<v-list-tile to="/program">
						<v-list-tile-action>
							<v-icon large>flip_to_front</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Programma</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/control">
						<v-list-tile-action>
							<v-icon large>games</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Controlla</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/settings">
						<v-list-tile-action>
							<v-icon large>settings</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Impostazioni</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/gallery">
						<v-list-tile-action>
							<v-icon large>photo_library</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Galleria</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<br>
					<v-layout row wrap fill-height>
						<v-flex xs12 style="position:absolute; bottom: 1%;">
							<small>
								&nbsp; &copy;2019 - CoderBot.org, UNIMIB.
								<!-- — <router-link to="/credits"><a>Credits</a></router-link>-->
							</small>
						</v-flex>
					</v-layout>
				</v-list>
			</v-navigation-drawer>
		</template>
		<template v-else>
			<v-navigation-drawer fixed v-model="drawer" app :mobile-break-point="0">
				<v-list dense>
					<v-list-tile to="/">
						<v-list-tile-action>
							<v-icon large>home</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Home</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile href="/docs" target="_blank">
						<v-list-tile-action>
							<v-icon large>help</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Documentazione</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<!--
				<v-list-tile to="/help">
					<v-list-tile-action>
						<v-icon large>help</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title class="navEntry">Aiuto</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>
			-->
					<br>
					<v-divider>
					</v-divider>
					<br>
					<!--
				<v-list-tile to="/activity">
					<v-list-tile-action>
						<v-icon>open_in_new</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>Apri Attività</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>
			-->
					<h3>Attività</h3>
					<v-list-tile to="/activity/open">
						<v-list-tile-action>
							<v-icon>open_in_new</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title>Apri</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/activity/new">
						<v-list-tile-action>
							<v-icon>add</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title>Nuova</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<br>
					<v-divider>
					</v-divider>
					<br>
					<v-list-tile to="/program">
						<v-list-tile-action>
							<v-icon large>flip_to_front</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Programma</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/control">
						<v-list-tile-action>
							<v-icon large>games</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Controlla</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/settings">
						<v-list-tile-action>
							<v-icon large>settings</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Impostazioni</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<v-list-tile to="/gallery">
						<v-list-tile-action>
							<v-icon large>photo_library</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="navEntry">Galleria</v-list-tile-title>
						</v-list-tile-content>
					</v-list-tile>
					<br>
					<v-layout row wrap fill-height>
						<v-flex xs12 style="position:absolute; bottom: 1%;">
							<small>
								&nbsp; &copy;2019 - CoderBot.org, UNIMIB.
								<!-- — <router-link to="/credits"><a>Credits</a></router-link>-->
							</small>
						</v-flex>
					</v-layout>
					<div>
						<!--
						<v-btn v-for="el in socials" :key="el.icon" class="mx-3 gray--text" icon :href="el.link" target="_blank">
							<v-icon size="24px">{{ el.icon }}</v-icon>
						</v-btn>-->
						<br>
						<center>
						</center>
					</div>
				</v-list>
			</v-navigation-drawer>
		</template>
	</div>
</template>
<script>
export default {
	data() {

		return {
			socials: [
				{ icon: 'fab fa-facebook', link: 'https://facebook.com/coderbot' },
				{ icon: 'fab fa-twitter', link: 'https://twitter.com/coderbotorg' },
				{ icon: 'fab fa-instagram', link: 'https://www.instagram.com/coderbotorg/' },
				{ icon: 'fab fa-github', link: 'https://www.github.com/coderbotorg' },
			],
		}
	},
	methods: {
		editModal() {
			let axios = this.$axios
			let CB = this.$data.CB
			//let programList = this.$data.programList
			axios.get(CB + '/listActivities')
				.then(function(response) {
					this.$data.editModal = true,
						this.$data.activitiesList = response.data;
				}.bind(this))
		},
	},
	props: {
		mobileDrawAnim: {
			type: String,
			default: "1",
		}
	},
	computed: {
		drawer: {
			get() {
				return this.$store.state.drawer
			},
			set(val) {
				this.$store.commit('toggleDrawer', val)
			}
		}
	}
}

</script>
<style scoped>
</style>
