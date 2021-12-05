<template>
    <button @click="onClick()" :style="{ background: color }" class="btn">
        {{text}}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    methods: {
        onClick() {
            this.$emit('btn-click')
        }
    },
    data() {
        return {
            tasks: [],
        }
    },
    created() {
        // life cycle hook
        this.tasks = [
    {
      "id": "1",
      "text": "Doctors Appointment",
      "day": "March 5th at 2:30pm",
      "reminder": true
    },
    {
      "id": "2",
      "text": "Meeting with boss",
      "day": "March 6th at 1:30pm",
      "reminder": true
    },
    {
      "id": "3",
      "text": "Food shopping",
      "day": "March 7th at 2:00pm",
      "reminder": false
    }
  ];
    }
}
</script>
