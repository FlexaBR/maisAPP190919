<template>
	<div id="app">
		<Header title="+APP" :hideToggle="false"/>
		<Menu />
		<Content />
		<Footer />
	</div>
</template>

<script>
import Header from "@/components/template/Header"
import Menu from "@/components/template/Menu"
import Content from "@/components/template/Content"
import Footer from "@/components/template/Footer"

export default {
	name: "App",
	components: { Header, Menu, Content, Footer }
}
// style
// font-family referenciada no index.html
// margin: 0 para app não ter margem
// webkit e moz para deixar as fontes mais suaves
// height 100vh... ocupa a tela inteira do APP
// grid-template-rows: 60px 1fr 40px; ===> Header 60 1 frame para Conteudo (maximo q der) 3 40 para Footer 
// grid-template-columns: 300px 1fr ===> 300 p Menu e o qe sobra para conteudo

</script>

<style>
	* {
		font-family: "Lato", sans-serif;
	}
	body {
		margin: 0;
	}
	#app {
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;

		height: 100vh;
		display: grid;
		grid-template-rows: 60px 1fr 40px;
		grid-template-columns: 300px 1fr;
		grid-template-areas:
			"header header"
			"menu content"
			"menu footer";
	}
</style>