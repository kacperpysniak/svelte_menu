<script>
    let isOpen = false;
    
    function toggleMenu() {
      isOpen = !isOpen;
    }
  </script>
  
  <header>
    <div class="container">
      <h1>FIRMA</h1>
      <button on:click={toggleMenu} class="menu-button">☰</button>
    </div>
  </header>
  
  <nav class="{isOpen ? 'open' : ''}">
    <ul>
      <li><a on:click={toggleMenu} href="/">Home</a></li>
      <li><a on:click={toggleMenu} href="/about">About</a></li>
      <li><a on:click={toggleMenu} href="/services">Services</a></li>
      <li><a on:click={toggleMenu} href="/contact">Contact</a></li>
    </ul>
  </nav>


  <style>
    header {
      align-items: center;
      justify-content: flex-end;
      padding: 0.5em;
      background-color: #252525;
      color: #ffff;
    }
  
    .container {
      display: flex;
      align-items: center;
      
    }
  
    h1 {
      margin: 0;
      font-size: 1.2em;
      font-weight: normal;
    }
  
    button.menu-button {
      font-size: 1.5em;
      background-color: transparent;
      border: none;
      color: #fff;
      cursor: pointer;
      margin-right: 0;
      margin-left: auto;
    }
  
    nav {
      position: absolute;
      left: 0;
      width: 100%;
      height: 0;
      overflow: hidden;
      transition: height 0.3s ease-out;
      background-color: #252525;
      color: #fff;
    }
  
    nav.open {
      height: 100%;
    }
  
    ul {
      margin: 0;
      padding: 0;
      list-style: none;
      font-size: 1em;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  
    li {
      margin: 0;
      padding: 0;
      list-style: none;
      font-size: 1em;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    li:hover {
        background-color: #333333;
        border-radius: 5px;
    }
  
    a {
      text-decoration: none;
      color: #ffff;
      padding: 0.5em;
    }
  </style>
  