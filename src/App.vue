<template>
  <div
    id="app"
    class="min-h-screen w-screen flex justify-center items-center bg-gray-200"
  >
    <draggable
      :list="users"
      :animation="200"
      ghost-class="moving-card"
      group="users"
      filter=".action-button"
      class="w-full max-w-xs"
      tag="ul"
    >
      <card v-for="user in users" :key="user.id" :user="user"></card>
    </draggable>
  </div>
</template>

<script>
import draggable from 'vuedraggable';
import card from './components/Card';
const users = [
  {
    id: 1,
    name: 'Adrian Schubert',
    avatar:
      'https://pickaface.net/gallery/avatar/unr_sample_161118_2054_ynlrg.png'
  },
  {
    id: 2,
    name: 'Violet Gates',
    avatar: 'https://pickaface.net/gallery/avatar/freud51c8b3f65e7dc.png'
  },
  {
    id: 3,
    name: 'Steve Jobs',
    avatar: 'https://pickaface.net/gallery/avatar/Opi51c74d0125fd4.png'
  },
  {
    id: 4,
    name: 'Yassine Smith',
    avatar:
      'https://pickaface.net/gallery/avatar/unr_yassine_191124_2012_3gngr.png'
  },
  {
    id: 5,
    name: 'Senior Saez',
    avatar: 'https://pickaface.net/gallery/avatar/elmedinilla541c03412955c.png'
  }
];

export default {
  name: 'app',
  data() {
    return {
      users
    };
  },
  components: {
    draggable,
    card
  }
};
</script>

<style lang="scss">
.moving-card {
  opacity: 0.5;
  background: #f7fafc;
  border: 1px solid #4299e1;
}
</style>
