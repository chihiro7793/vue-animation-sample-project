<template>
    <div class="home">
        <Toast v-if="showToast" />
        <Todos @badValue="triggerToast" />
    </div>
</template>

<script>
import Toast from '../components/Toast'
import Todos from '../components/Todos'

export default {
    components: { Toast, Todos },
    data: () => ({ showToast: false }),
    methods: {
        triggerToast() {
            this.showToast = true
            setTimeout(() => (this.showToast = false), 3000)
        },
    },
}
</script>

<style></style>
