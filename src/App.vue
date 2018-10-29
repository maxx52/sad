<template>
	<v-app>
		<TopLine/>
		<v-content>
			<v-container fluid>
				<router-view></router-view>
			</v-container>
		</v-content>
		<v-footer app></v-footer>
	</v-app>
</template>

<script>
import TopLine from '@/components/TopLine'
export default {
  name: "App",
  components: {
		TopLine
	},
  data() {
    return {
			// rtr
		}
  }
};
</script>
