<template>
  <div class="admin">
    <admin-header/>
    <div class="ad-contain">
      <div id="ad-side">
        <admin-nav/>
      </div>
      <div id="ad-display">
        <router-view/>
      </div>
    </div>
  </div>
</template>

<script>
import AdminHeader from '@/components/AdminHeader.vue';
import AdminNav from '@/components/AdminNav.vue';
export default {
    name: 'AdminLayout',
    components: {
      AdminHeader,
      AdminNav
    }
}
</script>

<style>
  .ad-contain {
    display: flex;
  }
  #ad-side {
    width: 20%;
    border-right: solid 1px black;
    height: 100%;
  }
  #ad-display { 
    width: 100%;
    padding: 10px;
    text-align: left;
  }
</style>