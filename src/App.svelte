<script>

  // define your component tree before diving into
  // App Header Footer Store {CreatePollForm, PollList -> PollDetails}
  // UI component Button Card Tabs

  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import Tabs from './shared/Tabs.svelte';
  import CreatePollForm from './components/CreatePollForm.svelte';

  // tabs
  let items = ['Current Polls', 'Add New Poll'];
  let activeItem = 'Current Polls'
  const tabChange = (e) => {
    activeItem = e.detail;
  }
</script>

<Header />
<main>
  <Tabs {activeItem} {items} on:tabChange={tabChange}/> <!-- custom event -->
  {#if activeItem === 'Current Polls'}
    <p>Poll list component goes here~</p>
  {:else if activeItem === 'Add New Poll'}
    <CreatePollForm />
  {/if}

</main>
<Footer />

<style>
  main{
    max-width: 960px;
    margin: 40px auto;
  }
</style>