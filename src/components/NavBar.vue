<template>
<section>
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <button type="button" id="sidebarCollapse" class="btn btn-info">
      <i class="fas fa-align-right"></i>
        <span></span>
    </button>
    <button class="btn btn-dark d-inline-block d-lg-none ml-auto" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <i class="fas fa-align-justify"></i>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Add Students</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" href="#">Archive Students</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" href="#">Download Data</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" href="#">Delete</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
</section>
</template>

<script>
export default {};
</script>