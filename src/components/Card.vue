<template>
  <li
    class="p-4 mb-3 flex justify-between items-center bg-white border border-white cursor-move shadow rounded-lg"
  >
    <div class="flex items-center">
      <img class="w-10 h-10 rounded-full" :src="user.avatar" :alt="user.name" />
      <p class="tracking-wide ml-2 text-gray-700 font-semibold font-sans">
        {{ user.name }}
      </p>
    </div>
    <div class="flex">
      <button
        aria-label="Edit"
        class="p-1 text-teal-500 hover:text-teal-600 focus:outline-none"
      >
        <EditIcon />
      </button>
      <button
        aria-label="Delete"
        class="p-1 text-red-500 hover:text-red-600 focus:outline-none"
      >
        <Trash2Icon />
      </button>
    </div>
  </li>
</template>

<script>
import { Trash2Icon, EditIcon } from 'vue-feather-icons';
export default {
  name: 'card',
  components: {
    Trash2Icon,
    EditIcon
  },
  props: {
    user: {
      type: Object
    }
  }
};
</script>

<style lang="scss" scoped></style>
