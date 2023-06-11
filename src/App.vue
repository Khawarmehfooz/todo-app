<script setup>

</script>

<template>
  <main>
    <section id="header">
      <h1>TODOS</h1>
      <input type="text" name="" placeholder="What needs to be done?" autofocus id="input-todo">
    </section>
    <section>
      <div class="todo-list-header">
        <h2>Remaining Todos</h2>
        <button>Mark all as completed</button>
      </div>
      <ul class="todo-items">
        <li class="todo-item">
          <div class="todo-item-left">
            <button class="mark-complete"><i class="fa-regular fa-circle-check"></i></button>
            <!-- check completed: <i class="fa-solid fa-circle-check"></i> -->
            <p class="todo-title">Todo Item 1</p>
          </div>
          <div class="todo-item-right">
            <button class="edit"><i class="fa-regular fa-pen-to-square"></i></button>
            <button class="delete"><i class="fa-solid fa-trash"></i></button>
          </div>
        </li>
        <li class="todo-item">
            <div class="todo-item-left">
              <button class="mark-complete"><i class="fa-regular fa-circle-check"></i></button>
              <!-- check completed: <i class="fa-solid fa-circle-check"></i> -->
              <p class="todo-title">Todo Item 1</p>
            </div>
            <div class="todo-item-right">
              <button class="edit"><i class="fa-regular fa-pen-to-square"></i></button>
              <button class="delete"><i class="fa-solid fa-trash"></i></button>
            </div>
          </li>
      </ul>
    </section>
    <section class="filter">
      <a class="active" href="#/all">All</a>
      <a href="#/active">Active</a>
      <a href="#/completed">Completed</a>
    </section>
    <section class="clear-completed">
      <button>Clear Completed</button>
    </section>
  </main>
</template>

<style scoped>
*{
  box-sizing: border-box;
}
  main{
    width: min(40rem,95%);
    margin-inline:auto;
    margin-top: 3rem;
    padding: 1.5rem;
    border: 1px solid;
  }
  #header h1{
    font-size: 2rem;
    text-align: center;
  }
  #header input{
    display: inline;
    width: 100%;
    padding: 8px;
    border: 2px solid gray;
    border-radius: 5px;
    font-size: 1.2rem;
    outline: transparent;
  }
  #header input:focus{
    border-color: black;
  }
  .todo-list-header{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 28px 0;
  }
  .todo-list-header h2{
    margin: 0;
  }
  .todo-list-header button{
    background-color: greenyellow;
    color: black;
    padding: 8px 16px;
    font-size: 1rem;
    outline: transparent;
    border: 1px solid black;
    border-radius: 5px;
  }
  .todo-list-header button:hover{
    background-color: white;
    border-color: greenyellow;
    cursor: pointer;
    transition: .3s ease-in-out;
  }
  .todo-items{
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }
  .todo-item{
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #eee;
    border-radius: 5px;
    padding: 0 1rem;
  }
  .todo-item-left{
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .todo-title{
    font-size: 18px;
  }
  .todo-item-right{
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .todo-items button{
    background-color: transparent;
    padding: 5px;
    outline: none;
    border: none;
  }
  .todo-items button:hover{
    cursor: pointer;
  }
  .todo-items button i{
    font-size: 18px;
  }
  .filter {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    margin-top: 28px;
  }
  .filter a{
    border: 1px solid gray;
    padding: 5px 15px;
    text-align: center;
    text-decoration: none;
    border-radius: 5px;
    color: gray;
  }
  .filter a.active{
    border-color: black;
    color: black;

  }
  .clear-completed{
    text-align: center;
    margin-top: 18px;
  }
  .clear-completed button{
    padding: 8px 20px;
    background-color:darkorange;
    color: white;
    font-size: 18px;
    border: 2px solid black;
    border-radius: 8px;
  }
  .clear-completed button:hover{
    border-color: darkorange;
    background-color: white;
    color: black;
    cursor: pointer;
  }
</style>
