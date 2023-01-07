<script>
  let fields = { question: '', answerA: '', answerB: '' };

  const submitHandler = () => {
    console.log(fields);
  }
</script>

<form on:submit|preventDefault={submitHandler}>
  <div class="form-field">
    <label for="question">Poll Question:</label>
    <input type="text" id="question" bind:value={fields.question}>
  </div>
  <div class="form-field">
    <label for="answer-a">Answer-A:</label>
    <input type="text" id="answer-a" bind:value={fields.answerA}>
  </div>
  <div class="form-field">
    <label for="answer-b">Answer-B:</label>
    <input type="text" id="answer-b" bind:value={fields.answerB}>
  </div>
  <button>Add Poll</button>

</form>

<style>
  form{
    widtion: 400px;
    margin: 0 150px;
    text-align: center;
  }
  .form-field{
    margin: 10px auto;
  }
  input{
    width: 400px;
    border-radius: 6px
  }
  label{
    margin: 10px auto;
    text-align: left;
  }
  button {
  display: block;
  margin: 10px auto;
  width: 150px;
  height: 40px;
  background-color: #d91b42;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  }
</style>