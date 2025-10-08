<script lang="ts">
  let { messages } = $props();

  let message = $state(messages[0]);

  const randomMessage = () => {
    let newMessage = messages[Math.floor(Math.random() * messages.length)];
    while (newMessage === message) {
      newMessage = messages[Math.floor(Math.random() * messages.length)];
    }
    message = newMessage;
  };
</script>

<h3>{message} Thanks for visiting!</h3>
<button onclick={randomMessage}>New Greeting</button>
