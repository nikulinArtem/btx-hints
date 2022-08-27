<script setup>
import MainTable from "./components/MainTable.vue";
import IconSearch from "./components/icons/IconSearch.vue"

</script>

<template>
  <header>
    <nav class="navbar bg-black">
      <div class="container-fluid">
        <a class="navbar-brand ms-md-3 ms-lg-5 ms-sm-0 text-white text-center">[ 1С-Битрикс Шпаргалка ]</a>
        <form class="d-flex pe-md-3 pe-lg-5 pe-sm-0" role="search" @formdata.prevent>
          <input class="form-control bg-black rounded-0 text-white me-2 border-white border-start-0 border-top-0 border-end-0"
                 id="search"
                 type="text"
                 placeholder="Поиск"
                 aria-label="Search"
                 autocomplete="off"
          >
          <button class="btn btn-outline-light "
                  type="submit">
              <IconSearch/>
          </button>
        </form>
      </div>
    </nav>
  </header>

  <main>
    <MainTable />
  </main>
</template>

<style scoped>

</style>


