<script>

  // define your component tree before diving into
  // App Header Footer Store {CreatePollForm, PollList -> PollDetails}
  // UI component Button Card Tabs

  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import Tabs from './shared/Tabs.svelte';

  // tabs
  let items = ['Current Polls~', 'Add New Poll'];
  let activeItem = 'Current Polls'
</script>

<Header />
<main>
  <Tabs {items}/>


</main>
<Footer />

<style>
  main{
    max-width: 960px;
    margin: 40px auto;
  }
</style>