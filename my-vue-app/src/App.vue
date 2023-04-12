<script>
export default {
  data() {
    return {

    }
  }
}

</script>

<template>
  <div class="container">
    <h1>Hello World</h1>
  </div>
  
</template>

<style>
h1 {
  color:brown;
  padding: 115px 0;
}

.container {
	--angle: 0deg;
	width: 70vmin;
	height: 50vmin;
	border: 4vmin solid;
	/* This will work but yield a wrong result: */
	border-image: linear-gradient(var(--angle), red, yellow, lime, aqua, blue, magenta) 1;
	animation: 10s rotate linear infinite;
  box-shadow: 0px 15px 20px rgba(0, 0, 0, 0.2);
}

@property --angle {
	syntax: '<angle>';
	initial-value: 0deg;
	inherits: false;
}

@keyframes rotate {
	to {
		--angle: 360deg;
	}
}



</style>
