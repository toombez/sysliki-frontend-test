<script setup lang="ts">
const { getProviderAuthenticationUrl, authenticateProvider } = useStrapiAuth()

const route = useRoute()
const router = useRouter()

const onClick = async () => {
  // authenticateProvider('google', route.query.access_token)
  window.location.href = getProviderAuthenticationUrl('google') + '/callback'

  // console.log(getProviderAuthenticationUrl('google'))

  // router.go(getProviderAuthenticationUrl('google'))
}
</script>

<template>
  <div>
    <button @click="onClick">
      login
    </button>
  </div>
</template>
