<template>
	<header class="page-header">
		<div class="page-header__icon icon icon-git"></div>
		<nav class="nav">
			<router-link to="/" class="nav__item">Home</router-link>
			<router-link to="/commands" class="nav__item">Commands</router-link>
			<router-link to="/gitflow" class="nav__item">Git Flow</router-link>
		</nav>
	</header>
</template>



<script>
export default {
	name: 'PageHeader',
};
</script>



<style lang="scss" scoped>
.page-header {
	width: 100%;
	height: 6rem;
	padding: 1rem 2rem;
	display: flex;
	justify-content: space-between;
	align-items: center;
	position: fixed;
	top: 0;
	left: 0;
	z-index: 999;
	background-color: $color-brand-1;

	&__item {
		display: flex;
	}

	&__icon {
		font-size: 4rem;
		color: $color-white;
	}
}

.nav {
	font-size: 1.2rem;
	font-weight: 600;

	&__item {
		color: $color-brand-2;

		&:not(:last-child) {
			margin-right: 1.5rem;
		}

		&.router-link-exact-active {
			color: $color-white;
		}
	}
}
</style>
