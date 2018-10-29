<template>
	<div>
		<v-navigation-drawer app temporary v-model="drawer"></v-navigation-drawer>

		<v-toolbar app extended>
			<v-toolbar-side-icon class="hidden-sm-and-up" @click="drawer = !drawer"></v-toolbar-side-icon>

			<v-spacer></v-spacer>
			<v-toolbar-title>Муниципальное бюджетное дошкольное образовательное учреждение Детский сад №7 г. Павлово</v-toolbar-title>
			<v-spacer></v-spacer>
			<div class="text-xs-center" slot="extension">
				<v-menu open-on-hover bottom offset-y v-for="link of links" :key="link.id">
					<v-btn slot="activator" flat class="caption">
						<v-icon>{{link.icon}}</v-icon>
						{{link.title}}
						<v-icon>arrow_drop_down</v-icon>
					</v-btn>

					<v-list>
						<v-list-tile v-for="link of links" :key="link.title" @click="">
							<v-list-tile-title class="text-capitalized">{{ link.title }}</v-list-tile-title>
						</v-list-tile>
					</v-list>
				</v-menu>
			</div>
		</v-toolbar>
	</div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      drawer: false,
      links: [
				{ title: "Главное меню", url: "/", id: "1" },
				{ title: "Образовательные стандарты", url: "/", id: "2" },
				{ title: "Дополнительно", url: "/", id: "3" },
				{ title: "Для вас, родители", url: "/", id: "4" },
				{ title: "Полезные ссылки", url: "/", id: "5" },
				{ title: "Горячие линии", url: "/", id: "6" },
				{ title: "", url: "/", id: "7", icon: 'remove_red_eye' }
				]
    };
  }
};
</script>

<style lang="sass" scoped>

</style>
