<script>
  import axios from 'axios';
  let items = [];

  const fetchItems = async () => {
    const response = await axios.get('http://127.0.0.1:8000/api/items/');
    items = response.data;
    console.log(items)
  };

  fetchItems();
</script>
<h1>HELLO!!</h1>
<ul>
  {#each items as item}
    <li>{item.name}: {item.description}</li>
  {/each}
</ul>