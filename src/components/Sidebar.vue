<template>
  <div class="w-full flex-shrink-0 lg:w-1/4 lg:flex-shrink rounded-xl h-full bg-white shadow-xl">

     <div class="w-full mt-10">
        <div class="flex justify-end m-5">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M13.586 3.586a2 2 0 112.828 2.828l-.793.793-2.828-2.828.793-.793zM11.379 5.793L3 14.172V17h2.828l8.38-8.379-2.83-2.828z" />
            </svg>
        </div>
        <div class="flex items-center justify-center">
            <div class="flex items-center justify-center w-40 h-40 border border-1 bg-purple-200 rounded-full">
                <div class="text-orange-700 font-semibold text-4xl">
                    45%
                </div>
            </div>
        </div>
    </div>

    <div class="w-full mt-10">
        <div class="flex items-center justify-between m-5">
            <div class="text-gray-600 font-semibold">Mi tarjeta</div>
            <div class="text-blue-500">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM7 9H5v2h2V9zm8 0h-2v2h2V9zM9 9h2v2H9V9z" clip-rule="evenodd" />
                </svg>
            </div>
        </div>
        <div class="m-10">
            <img src="img/visa.jpg" />
        </div>
    </div>

    <div class="w-full mt-10">
      <div class="flex items-center justify-between m-5">
          <div class="text-gray-600 font-semibold">Transacciones</div>
          <div class="text-red-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v2H7a1 1 0 100 2h2v2a1 1 0 102 0v-2h2a1 1 0 100-2h-2V7z" clip-rule="evenodd" />
              </svg>
          </div>
      </div>
      <div class="flex items-center justify-between m-5">
          <div class="text-red-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M12 1.586l-4 4v12.828l4-4V1.586zM3.707 3.293A1 1 0 002 4v10a1 1 0 00.293.707L6 18.414V5.586L3.707 3.293zM17.707 5.293L14 1.586v12.828l2.293 2.293A1 1 0 0018 16V6a1 1 0 00-.293-.707z" clip-rule="evenodd" />
              </svg>
          </div>
          <div class="flex flex-col">
              <div class="text-grey-700">Taxi</div>
              <div class="text-gray-400">02:35 pm</div>
          </div>
          <div class="text-gray-700 font-semibold">-9.50</div>
      </div>
      <hr />
      <div class="flex items-center justify-between m-5">
          <div class="text-red-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 2a4 4 0 00-4 4v1H5a1 1 0 00-.994.89l-1 9A1 1 0 004 18h12a1 1 0 00.994-1.11l-1-9A1 1 0 0015 7h-1V6a4 4 0 00-4-4zm2 5V6a2 2 0 10-4 0v1h4zm-6 3a1 1 0 112 0 1 1 0 01-2 0zm7-1a1 1 0 100 2 1 1 0 000-2z" clip-rule="evenodd" />
              </svg>
          </div>
          <div class="flex flex-col">
              <div class="text-grey-700">Compras C.C.T</div>
              <div class="text-gray-400">08:51 pm</div>
          </div>
          <div class="text-gray-700 font-semibold">185.99</div>
      </div>
      <hr />
      <div class="flex items-center justify-between m-5">
          <div class="text-red-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M3 5a2 2 0 012-2h10a2 2 0 012 2v8a2 2 0 01-2 2h-2.22l.123.489.804.804A1 1 0 0113 18H7a1 1 0 01-.707-1.707l.804-.804L7.22 15H5a2 2 0 01-2-2V5zm5.771 7H5V5h10v7H8.771z" clip-rule="evenodd" />
              </svg>
          </div>
          <div class="flex flex-col">
              <div class="text-grey-700">Computadora</div>
              <div class="text-gray-400">11:15 am</div>
          </div>
          <div class="text-gray-700 font-semibold">-1590.99</div>
      </div>
    </div>
   
  </div>
</template>

<script>
export default {
  name: "App",
  components: { },
} 
</script>

<style>

</style>
