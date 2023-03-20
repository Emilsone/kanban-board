<template>
  <main>
    <!-- component -->
    <section class="task-section">
      <div class="w-full p-8  flex justify-around ">
        <div class="rounded bg-grey-light w-64 p-2 card-bg">
          <div class="flex justify-between py-1">
            <h3 class="text-lg">New Pitch</h3>
            <svg class="h-4 fill-current text-grey-dark cursor-pointer" xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24">
              <path
                d="M5 10a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4z" />
            </svg>
          </div>
          <div class="text-sm mt-2">
            <!-- <div class=""> -->
            <draggable class="draggable-list" :list="tasks.newPitch" group="tasks">
              <div v-for="(task, i) in tasks.newPitch" :key="i">
                <div class="bg-white p-2  py-6 rounded mt-1 border-b border-grey cursor-pointer hover:bg-grey-lighter">
                  <p>{{ task }}</p>
                  <div class="text-grey-darker mt-2 ml-2 flex justify-between items-start">
                    <span class="text-xs flex items-center">
                      <svg class="h-4 fill-current mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
                        <path
                          d="M11 4c-3.855 0-7 3.145-7 7v28c0 3.855 3.145 7 7 7h28c3.855 0 7-3.145 7-7V11c0-3.855-3.145-7-7-7zm0 2h28c2.773 0 5 2.227 5 5v28c0 2.773-2.227 5-5 5H11c-2.773 0-5-2.227-5-5V11c0-2.773 2.227-5 5-5zm25.234 9.832l-13.32 15.723-8.133-7.586-1.363 1.465 9.664 9.015 14.684-17.324z" />
                      </svg>
                      3/5
                    </span>
                    <img src="https://i.imgur.com/OZaT7jl.png" class="rounded-full" />
                  </div>
                </div>
              </div>

              <div class="flex justify-between align-middle items-center m-3">
                <p class="mt-3 text-grey-dark flex justify-between"><svg xmlns="http://www.w3.org/2000/svg" fill="none"
                    viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 ">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                  </svg>
                  <span>Add a card...</span>
                </p>
                <span class="pt-3">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="w-4 h-4">
                    <path stroke-linecap="round" stroke-linejoin="round"
                      d="M13.5 16.875h3.375m0 0h3.375m-3.375 0V13.5m0 3.375v3.375M6 10.5h2.25a2.25 2.25 0 002.25-2.25V6a2.25 2.25 0 00-2.25-2.25H6A2.25 2.25 0 003.75 6v2.25A2.25 2.25 0 006 10.5zm0 9.75h2.25A2.25 2.25 0 0010.5 18v-2.25a2.25 2.25 0 00-2.25-2.25H6a2.25 2.25 0 00-2.25 2.25V18A2.25 2.25 0 006 20.25zm9.75-9.75H18a2.25 2.25 0 002.25-2.25V6A2.25 2.25 0 0018 3.75h-2.25A2.25 2.25 0 0013.5 6v2.25a2.25 2.25 0 002.25 2.25z" />
                  </svg>

                </span>
              </div>
            </draggable>
            <!-- </div> -->

          </div>
        </div>

        <div class="rounded bg-grey-light w-64 p-2 card-bg">
          <div class="flex justify-between py-1">
            <h3 class="text-lg">Content in Progress</h3>
            <svg class="h-4 fill-current text-grey-dark cursor-pointer" xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24">
              <path
                d="M5 10a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4z" />
            </svg>
          </div>
          <div class="text-sm mt-2">
            <div class="">
              <draggable class="draggable-list" :list="tasks.contentInProgress" group="tasks">
                <div v-for="(task, i) in tasks.contentInProgress" :key="i">
                  <div class="bg-white p-2  py-6 rounded mt-1 border-b border-grey cursor-pointer hover:bg-grey-lighter">
                    <p>{{ task }}</p>
                    <div class="text-grey-darker mt-2 ml-2 flex justify-between items-start">
                      <span class="text-xs flex items-center">
                        <svg class="h-4 fill-current mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
                          <path
                            d="M11 4c-3.855 0-7 3.145-7 7v28c0 3.855 3.145 7 7 7h28c3.855 0 7-3.145 7-7V11c0-3.855-3.145-7-7-7zm0 2h28c2.773 0 5 2.227 5 5v28c0 2.773-2.227 5-5 5H11c-2.773 0-5-2.227-5-5V11c0-2.773 2.227-5 5-5zm25.234 9.832l-13.32 15.723-8.133-7.586-1.363 1.465 9.664 9.015 14.684-17.324z" />
                        </svg>
                        3/5
                      </span>
                      <img src="https://i.imgur.com/OZaT7jl.png" class="rounded-full" />
                    </div>
                  </div>
                </div>

                <div class="flex justify-between align-middle items-center m-3">
                  <p class="mt-3 text-grey-dark flex justify-between"><svg xmlns="http://www.w3.org/2000/svg" fill="none"
                      viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 ">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                    </svg>
                    <span>Add a card...</span>
                  </p>
                  <span class="pt-3">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                      stroke="currentColor" class="w-4 h-4">
                      <path stroke-linecap="round" stroke-linejoin="round"
                        d="M13.5 16.875h3.375m0 0h3.375m-3.375 0V13.5m0 3.375v3.375M6 10.5h2.25a2.25 2.25 0 002.25-2.25V6a2.25 2.25 0 00-2.25-2.25H6A2.25 2.25 0 003.75 6v2.25A2.25 2.25 0 006 10.5zm0 9.75h2.25A2.25 2.25 0 0010.5 18v-2.25a2.25 2.25 0 00-2.25-2.25H6a2.25 2.25 0 00-2.25 2.25V18A2.25 2.25 0 006 20.25zm9.75-9.75H18a2.25 2.25 0 002.25-2.25V6A2.25 2.25 0 0018 3.75h-2.25A2.25 2.25 0 0013.5 6v2.25a2.25 2.25 0 002.25 2.25z" />
                    </svg>

                  </span>
                </div>
              </draggable>
            </div>

          </div>
        </div>

        <div class="rounded bg-grey-light w-64 p-2  card-bg">
          <div class="flex justify-between py-1">
            <h3 class="text-lg">Draft Received</h3>
            <svg class="h-4 fill-current text-grey-dark cursor-pointer" xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24">
              <path
                d="M5 10a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4z" />
            </svg>
          </div>
          <div class="text-sm mt-2">
            <div class="">
              <draggable class="draggable-list" :list="tasks.draftReceived" group="tasks">
                <div v-for="(task, i) in tasks.draftReceived" :key="i">
                  <div class="bg-white p-2  py-6 rounded mt-1 border-b border-grey cursor-pointer hover:bg-grey-lighter">
                    <p>{{ task }}</p>
                    <div class="text-grey-darker mt-2 ml-2 flex justify-between items-start">
                      <span class="text-xs flex items-center">
                        <svg class="h-4 fill-current mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
                          <path
                            d="M11 4c-3.855 0-7 3.145-7 7v28c0 3.855 3.145 7 7 7h28c3.855 0 7-3.145 7-7V11c0-3.855-3.145-7-7-7zm0 2h28c2.773 0 5 2.227 5 5v28c0 2.773-2.227 5-5 5H11c-2.773 0-5-2.227-5-5V11c0-2.773 2.227-5 5-5zm25.234 9.832l-13.32 15.723-8.133-7.586-1.363 1.465 9.664 9.015 14.684-17.324z" />
                        </svg>
                        3/5
                      </span>
                      <img src="https://i.imgur.com/OZaT7jl.png" class="rounded-full" />
                    </div>
                  </div>
                </div>

                <div class="flex justify-between align-middle items-center m-3">
                  <p class="mt-3 text-grey-dark flex justify-between"><svg xmlns="http://www.w3.org/2000/svg" fill="none"
                      viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 ">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                    </svg>
                    <span>Add a card...</span>
                  </p>
                  <span class="pt-3">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                      stroke="currentColor" class="w-4 h-4">
                      <path stroke-linecap="round" stroke-linejoin="round"
                        d="M13.5 16.875h3.375m0 0h3.375m-3.375 0V13.5m0 3.375v3.375M6 10.5h2.25a2.25 2.25 0 002.25-2.25V6a2.25 2.25 0 00-2.25-2.25H6A2.25 2.25 0 003.75 6v2.25A2.25 2.25 0 006 10.5zm0 9.75h2.25A2.25 2.25 0 0010.5 18v-2.25a2.25 2.25 0 00-2.25-2.25H6a2.25 2.25 0 00-2.25 2.25V18A2.25 2.25 0 006 20.25zm9.75-9.75H18a2.25 2.25 0 002.25-2.25V6A2.25 2.25 0 0018 3.75h-2.25A2.25 2.25 0 0013.5 6v2.25a2.25 2.25 0 002.25 2.25z" />
                    </svg>

                  </span>
                </div>
              </draggable>
            </div>

          </div>

        </div>

        <div class="rounded bg-grey-light w-64 p-2 card-bg">
          <div class="flex justify-between py-1">
            <h3 class="text-lg">In Review</h3>
            <svg class="h-4 fill-current text-grey-dark cursor-pointer" xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24">
              <path
                d="M5 10a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4zm7 0a1.999 1.999 0 1 0 0 4 1.999 1.999 0 1 0 0-4z" />
            </svg>
          </div>
          <div class="text-sm mt-2">
            <div class="">
              <draggable class="draggable-list" :list="tasks.inReview" group="tasks">
                <div v-for="(task, i) in tasks.inReview" :key="i">
                  <div class="bg-white p-2  py-6 rounded mt-1 border-b border-grey cursor-pointer hover:bg-grey-lighter">
                    <p>{{ task }}</p>
                    <div class="text-grey-darker mt-2 ml-2 flex justify-between items-start">
                      <span class="text-xs flex items-center">
                        <svg class="h-4 fill-current mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
                          <path
                            d="M11 4c-3.855 0-7 3.145-7 7v28c0 3.855 3.145 7 7 7h28c3.855 0 7-3.145 7-7V11c0-3.855-3.145-7-7-7zm0 2h28c2.773 0 5 2.227 5 5v28c0 2.773-2.227 5-5 5H11c-2.773 0-5-2.227-5-5V11c0-2.773 2.227-5 5-5zm25.234 9.832l-13.32 15.723-8.133-7.586-1.363 1.465 9.664 9.015 14.684-17.324z" />
                        </svg>
                        3/5
                      </span>
                      <img src="https://i.imgur.com/OZaT7jl.png" class="rounded-full" />
                    </div>
                  </div>
                </div>

                <div class="flex justify-between align-middle items-center m-3">
                  <p class="mt-3 text-grey-dark flex justify-between"><svg xmlns="http://www.w3.org/2000/svg" fill="none"
                      viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 ">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                    </svg>
                    <span>Add a card...</span>
                  </p>
                  <span class="pt-3">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                      stroke="currentColor" class="w-4 h-4">
                      <path stroke-linecap="round" stroke-linejoin="round"
                        d="M13.5 16.875h3.375m0 0h3.375m-3.375 0V13.5m0 3.375v3.375M6 10.5h2.25a2.25 2.25 0 002.25-2.25V6a2.25 2.25 0 00-2.25-2.25H6A2.25 2.25 0 003.75 6v2.25A2.25 2.25 0 006 10.5zm0 9.75h2.25A2.25 2.25 0 0010.5 18v-2.25a2.25 2.25 0 00-2.25-2.25H6a2.25 2.25 0 00-2.25 2.25V18A2.25 2.25 0 006 20.25zm9.75-9.75H18a2.25 2.25 0 002.25-2.25V6A2.25 2.25 0 0018 3.75h-2.25A2.25 2.25 0 0013.5 6v2.25a2.25 2.25 0 002.25 2.25z" />
                    </svg>

                  </span>
                </div>
              </draggable>
            </div>

          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import draggable from "vuedraggable";
export default {
  name: 'HelloWorld',
  components: {
    draggable,
  },
  data() {
    return {
      tasks: {
        newPitch: ["Introduction to Tailwind CSS", "Grapql and Vue: Consume API", "Frontend:React vs Vue"],
        contentInProgress: ["Vuex vs Pinia", "Svelte vs React"],
        draftReceived: ["Implement Web3 Features", "Bump to vite.js"],
        inReview: [""],
      },
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.task-section {
  font-family: 'Work Sans', sans-serif;
  background-image: url(https://trello-backgrounds.s3.amazonaws.com/SharedBackground/1663x1920/c429dd4ede333ffefe94abbb4d512691/photo-1613824320065-3d07b66b8d32.jpg);
  height: 100vh;
  background-size: cover;
  background-position: center;
}

.card-bg {
  background-color: #DAE4E8;
}
</style>