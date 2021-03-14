<template>
  <div class="content">
      <div class="image-grid">
          <div class="col">
            <img 
                src="https://images.unsplash.com/photo-1511732351157-1865efcb7b7b?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80" 
                alt="work-from-home" 
            />
          </div>
          <div class="col">
            <img 
                src="https://images.unsplash.com/photo-1491466424936-e304919aada7?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1349&q=80" 
                alt="northern-lights" 
            />
          </div>
      </div>
  </div>
</template>

<script>
export default {
    props: ['mode']
}
</script>

<style>
.content {
    padding: 25px;
}

.content h3 {
    font-size: 28px;
    text-transform: uppercase;
    font-weight: 300;
    margin-bottom: 25px;
}

.image-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 15px;
}

.image-grid img {
    max-width: 100%;
    height: auto;
}
</style>