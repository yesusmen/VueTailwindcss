<template>
    <div class="flex lg:space-x-10">
        <div class="hidden lg:w-1/2 lg:block">
            <SearchForm />
        </div>
        <div class="w-full lg:w-1/2">
            <div class="flex justify-between">
                <div class="lg:hidden">
                    <a href="#" class="flex justify-center items-center w-14 h-14 rounded-xl bg-gray-50">
                        <!-- <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-800" viewBox="0 0 20 20" fill="currentColor">
                            <path d="M11 17a1 1 0 001.447.894l4-2A1 1 0 0017 15V9.236a1 1 0 00-1.447-.894l-4 2a1 1 0 00-.553.894V17zM15.211 6.276a1 1 0 000-1.788l-4.764-2.382a1 1 0 00-.894 0L4.789 4.488a1 1 0 000 1.788l4.764 2.382a1 1 0 00.894 0l4.764-2.382zM4.447 8.342A1 1 0 003 9.236V15a1 1 0 00.553.894l4 2A1 1 0 009 17v-5.764a1 1 0 00-.553-.894l-4-2z" />
                        </svg> -->
                        <img src="img/logo_yesus.png" alt="">
                    </a>
                </div>
                <div class="h-10 hidden lg:flex items-center space-x-6 font-semibold dark:text-white">
                    <a href="#" class="hover:text-blue-800">Análisis</a>
                    <a href="#" class="hover:text-blue-800">Contactos</a>
                    <a href="#" class="hover:text-blue-800">Ayuda</a>
                </div>

                <div class="flex items-center space-x-4">

                    <!--beging::ModeDark-->
                    <span class="text-purple-800 dark:text-gray-100">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" clip-rule="evenodd" />
                        </svg>
                    </span>
                    <label for="toggle" class="w-9 h-5 flex items-center bg-gray-300 rounded-full p-1 cursor-pointer duration-300 ease-in-out dark:bg-gray-600">
                        <div class="toggle-dot bg-white w-4 h-4 rounded-full shadow-md transform duration-300 ease-in-out" :class="isDark ? 'translate-x-3' : ''"></div>
                    </label>
                    <span class="text-gray-800 dark:text-purple-600">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z" />
                        </svg>
                    </span>
                    <input id="toggle" type="checkbox" class="hidden toggle" :checked="isDark ? true : false"  @change="$emit('toggle'),theme()"  />
                    <!--beging::ModeDark-->

                    <a href="#" class="flex items-center justify-center w-10 h-10 text-gray-300 hover:text-gray-700 relative">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z" />
                        </svg>

                        <div class="w-2 h-2 bg-red-500 rounded-full absolute top-2 right-2 borde border-white"></div>
                    </a>

                    <div class="lg:relative">
                        <button class="w-10 h-10  rounded-full overflow-hidden focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-800 focus:ring-offset-white" @click="isOpen = !isOpen">
                            <!-- <img src="https://tailwindcss.com/_next/static/media/sarah-dayan.a8ff3f1095a58085a82e3bb6aab12eb2.jpg" alt="" class="w-10 h-10 object-cover"> -->
                            <img src="/img/perfil_yesus.jpeg" alt="" class="w-10 h-10 object-cover">
                        </button>

                        <button v-if="isOpen" @click="isOpen = false" class="fixed inset-0 w-full h-full z-30 cursor-default" tabindex="-1"></button>

                        <transition
                            enter-active-class="transition ease-out duration-100 transform"
                            enter-form-class="opacity-0 scale-95"
                            enter-to-class="opacity-100 scale-100"
                            leave-active-class="transition ease-in duration-75 transform"
                            leave-form-class="opacity-100 scale-100"
                            leave-to-class="opacity-0 scale-95"
                        >
                            <div class="absolute z-40 right-0 mt-2 w-full lg:w-48" v-if="isOpen">
                                <div class="bg-white mx-4 lg:mx-0 rounded-md shadow-lg py-1 ring-1 ring-black ring-opacity-5"> 

                                    <div class="lg:hidden p-3">
                                        <SearchForm />
                                    </div>

                                    <div class="lg:hidden border-b">
                                        <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Análisis</a>
                                        <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Contactos</a>
                                        <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Ayuda</a>
                                    </div>

                                    <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Perfil</a>
                                    <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Configuración</a>
                                    <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Cerra sesión</a>
                                </div>
                            </div>
                        </transition>

                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
import SearchForm from './SearchForm.vue';
export default {
    name: 'Tools',
    components: { SearchForm },
    data() {
        return {
            isOpen: false,
            isDark: false,
        }
    },
    methods: {
        theme() {
            this.isDark = !this.isDark
            localStorage.setItem('userModeDark', JSON.stringify(this.isDark))
        }
    },
    created(){
        const result = JSON.parse(localStorage.getItem("userModeDark"))
        if (result){
            this.isDark = true
        }else{
            this.isDark= false
        }
    }
}
</script>