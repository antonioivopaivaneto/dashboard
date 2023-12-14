<template>
  <CustomHeader @create-account="handleAccountCreate" @login="handleLogin" />
  <ContactPage />
  <div class="flex justify-center py-10 bg-brand-gray">
    <p class="font-medium text-center text-gray-800">feedback 2023</p>
  </div>
</template>

<script>
import CustomHeader from './CustomHeader.vue'
import ContactPage from './ContactPage.vue'
import { onMounted } from 'vue'
import { useRouter } from 'vue-router'

export default {
  components: { CustomHeader, ContactPage },
  setup () {
    const router = useRouter()

    onMounted(() => {
      const token = window.localStorage.getItem('token')
      if (token) {
        router.push({ name: 'Feedbacks' })
      }
    })

    function handleLogin () {

    }
    function handleAccountCreate () {

    }

    return {
      handleLogin,
      handleAccountCreate
    }
  }
}
</script>
