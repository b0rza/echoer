<script>
  // import template from './template.html';

  export default {
    // template,
    props: [
      'channel',
      'pusher',
    ],
    data() {
      return {
        tweets: [],
      };
    },
  };
</script>
