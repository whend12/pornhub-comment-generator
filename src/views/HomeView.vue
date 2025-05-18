<template>
  <div class="bg-white min-h-screen flex flex-col items-center py-8 px-4">
    <div
      class="bg-[#1e1e1e] w-full max-w-xl rounded-t-md px-4 py-3 flex items-center justify-between"
    >
      <div class="flex items-center text-2xl font-bold">
        <span class="text-white">Porn</span>
        <span class="bg-[#f7a600] text-black px-2 rounded ml-1">hub</span>
      </div>
      <div>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 text-white"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
          />
        </svg>
      </div>
    </div>

    <div class="bg-[#1e1e1e] w-full max-w-xl px-4 py-2 text-white text-lg font-semibold">
      Top Comments
    </div>

    <!-- Comment dimari -->
    <div
      class="bg-[#111] text-white w-full max-w-xl px-4 py-3 space-y-2 max-h-64 overflow-auto rounded-b-md"
    >
      <div class="flex items-start">
        <img src="https://i.imgur.com/4M34hi2.png" class="w-10 h-10 rounded-full mr-4" />
        <div class="flex-1">
          <div class="flex justify-between text-sm">
            <span class="text-[#f7a600] font-semibold">{{ username || 'anonymous' }}</span>
            <span class="text-gray-400">just now</span>
          </div>
          <p class="text-white mt-1 whitespace-pre-line">
            {{ comment || 'Type a comment below...' }}
          </p>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-sm mt-2">
        <div class="flex items-center space-x-1 bg-[#2c2c2c] px-2 py-1 rounded-md">
          <span>👍</span>
          <span>69</span>
        </div>
        <div class="flex items-center space-x-1 bg-[#2c2c2c] px-2 py-1 rounded-md">
          <span>👎</span>
        </div>
        <div class="text-gray-400 cursor-pointer">Replies</div>
      </div>
    </div>

    <div class="mt-8 w-full max-w-xl space-y-3 text-center">
      <span class="text-[#f7a600] text-sm font-bold">input username</span>
      <input
        v-model="username"
        type="text"
        placeholder="Enter your username"
        class="w-full px-4 py-2 rounded-full border border-gray-300 text-black focus:outline-none"
      />
      <span class="text-[#f7a600] text-sm font-bold">input comment</span>
      <textarea
        v-model="comment"
        placeholder="Write your comment..."
        class="w-full px-4 py-2 rounded-xl border border-gray-300 text-black resize-none focus:outline-none"
        rows="3"
      ></textarea>
      <p class="text-black text-sm">Take A Screenshot To Save!</p>
      <p class="text-gray-500 text-xs mt-2">
        Made by <span class="font-bold text-[#f7a600]">when</span>
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const username = ref('')
const comment = ref('')
</script>
