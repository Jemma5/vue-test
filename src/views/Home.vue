<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for='event in events' :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data() {
    return {
      events:[
        {
          id: 5890909,
          category: 'animal welfare',
          title: 'Cat Adoption Day',
          description: 'Find your new feline friend at this event.',
          location: 'Meow Town',
          date: 'January 28, 2022',
          time: '12.00',
          petsAllowed: true,
          organizer: 'Kat Laydee'
        },
        {
          id: 5890901,
          category: 'animal fun',
          title: 'Dog Adoption Day',
          description: 'Find your new k9 friend at this event.',
          location: 'Bowwow Town',
          date: 'January 29, 2022',
          time: '1.00',
          petsAllowed: true,
          organizer: 'Doggie Boy'
        }
      ]
    }
  }
};
</script>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
