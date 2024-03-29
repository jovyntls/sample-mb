<head-bottom>
  <link rel="stylesheet" href="{{baseUrl}}/stylesheets/main.css">
</head-bottom>

<header fixed>
  <navbar type="dark">
    <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">Your Logo</a>
    <li><a href="{{baseUrl}}/contents/topic1.html" class="nav-link">Topic 1</a></li>
    <li><a href="{{baseUrl}}/contents/topic2.html" class="nav-link">Topic 2</a></li>
    <dropdown header="Topic 3" class="nav-link">
      <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3a</a></li>
      <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3b</a></li>
    </dropdown>
    <li slot="right">
      <form class="navbar-form">
        <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right></searchbar>
      </form>
    </li>
    <dropdown header="Topic 3" class="nav-link">
      <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3c</a></li>
      <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
      <dropdown header="Topic 3" class="nav-link">
        <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3c</a></li>
        <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
        <dropdown header="Topic 3" class="nav-link">
          <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3c</a></li>
          <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
          <dropdown header="Topic 3" class="nav-link">
            <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3ccccccccc</a></li>
            <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
            <dropdown header="Topic 3" class="nav-link">
              <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3cccccccccccccccccccccccs</a></li>
              <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
              <dropdown header="Topic 3" class="nav-link">
                <li><a href="{{baseUrl}}/contents/topic3a.html" class="dropdown-item">Topic 3ccccccccc</a></li>
                <li><a href="{{baseUrl}}/contents/topic3b.html" class="dropdown-item">Topic 3d</a></li>
              </dropdown>
            </dropdown>
          </dropdown>
        </dropdown>
      </dropdown>
    </dropdown>
  </navbar>
</header>

<div id="flex-body">
  <nav id="site-nav" class="fixed-header-padding">
    <div class="site-nav-top">
      <div class="font-weight-bold mb-2" style="font-size: 1.25rem;">Template</div>
    </div>
    <div class="nav-component slim-scroll">
      <site-nav>
* [Home :house:]({{ baseUrl }}/index.html)
* [Topic 1]({{baseUrl}}/contents/topic1.html)
* [Topic 2]({{baseUrl}}/contents/topic2.html)
* Topic 3 :expanded:
  * [Topic 3a]({{baseUrl}}/contents/topic3a.html)
  * [Topic 3b]({{baseUrl}}/contents/topic3b.html)
      </site-nav>
    </div>
  </nav>
  <div id="content-wrapper" class="fixed-header-padding">
    {{ content }}
  </div>
  <nav id="page-nav" class="fixed-header-padding">
    <div class="nav-component slim-scroll">
      <page-nav />
    </div>
  </nav>
</div>

<footer>
  <!-- Support MarkBind by including a link to us on your landing page! -->
  <div class="text-center">
    <small>[Generated by {{MarkBind}}]</small>
  </div>
</footer>
