<template>
    <b-navbar 
        toggleable="lg" 
        type="light" 
        variant="light"
    >
        <b-navbar-brand :to="{ name: 'catalog' }">{{ $t("navbar.brand") }}</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse" />
        <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
                <b-nav-item :to="{ name: 'catalog', query: { type: 'desktop'} }">{{ $t("navbar.links.desktop") }}</b-nav-item>
                <b-nav-item :to="{ name: 'catalog', query: { type: 'laptop' } }">{{ $t("navbar.links.laptop") }}</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav class="ml-auto">
                <b-nav-form>
                    <b-form-input disabled size="sm" class="mr-sm-2" :placeholder="$t('navbar.search.placeholder')" />
                </b-nav-form>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
</template>

<script>
export default {
    name: "Navbar"
}
</script>

<style>

</style>
