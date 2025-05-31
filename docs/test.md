# This is a long css-file

#### *A long file with a lot of things*

```html
<script setup lang="ts">
import { ref } from 'vue';
import { RouterView, useRouter, RouterLink } from 'vue-router';
import { Collapse } from 'bootstrap';

const router = useRouter();

const blogPosts = ref([
  { slug: 'sample', title: 'Sample Markdown Post' },
  { slug: 'preface', title: 'Preface to all the Times' }
]);

const navigateAndCloseNav = (routePath: string) => {
  router.push(routePath);
  const navbarCollapse = document.getElementById("navbarNav");
  if (navbarCollapse && navbarCollapse.classList.contains("show")) {
    const bsCollapse = new Collapse(navbarCollapse, {
      toggle: false,
    });
    bsCollapse.hide();
  }
};
</script>

<style>
/* Global Styles (no 'scoped' keyword) */
html, body {
  height: 100%; /* Make html and body take full viewport height */
  margin: 0; /* Remove default margins */
  padding: 0; /* Remove default padding */
  box-sizing: border-box; /* Include padding and border in the element's total width and height */
  font-family: sans-serif; /* Good practice for default font */
}

body {
  display: flex; /* Enable flexbox */
  flex-direction: column; /* Arrange children (navbar, content) vertically */
  /* Background styles for the entire page */
  background-image: url('https://picsum.photos/1920/1080'); /* Example random image */
  background-size: cover;
  background-attachment: fixed; /* Keeps the background fixed when scrolling */
  background-position: center;
}

/* Optional: Semi-transparent overlay on the body background */
body::before {
  content: '';
  position: fixed; /* Covers the whole viewport */
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.1); /* Subtle dark overlay */
  z-index: -1; /* Puts it behind everything else */
}
</style>

<style scoped>
/* Scoped Styles (specific to this component) */

/* Add the frosted glass effect to the navbar */
.frosted-navbar {
  background-color: rgba(255, 255, 255, 0.5); /* Semi-transparent background */
  backdrop-filter: blur(10px); /* Adjust the blur intensity as needed */
  -webkit-backdrop-filter: blur(10px); /* For Safari support */
  border-bottom: 1px solid rgba(255, 255, 255, 0.2); /* Optional: subtle border */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Optional: subtle shadow */
  flex-shrink: 0; /* Prevents the navbar from shrinking */
}

/* Frosted glass for the main content area (RouterView) */
.content-full-height {
  flex-grow: 1; /* This makes the content area expand to fill all available vertical space */
  /* Remove fixed top/bottom margins as flexbox now controls spacing */
  /* margin-top: 20px; /* REMOVE THIS */
  /* margin-bottom: 20px; /* REMOVE THIS */

  /* Add padding inside the container for content */
  padding-top: 20px;
  padding-bottom: 20px;
  /* Bootstrap's .container already provides horizontal padding and max-width */

  /* Frosted glass styles for content area */
  background-color: rgba(255, 255, 255, 0.3); /* Semi-transparent white */
  backdrop-filter: blur(10px); /* Apply the blur */
  -webkit-backdrop-filter: blur(10px); /* Safari support */
  border-radius: 8px; /* Optional: subtle rounded corners */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15); /* More prominent shadow */

  min-height: 0; /* Allows the flex item to shrink below its content size if needed */
  overflow-y: auto; /* Allows scrolling within this content area if content overflows vertically */
}

/* Specific styling for the 'About' link to override Bootstrap's blue */
.about-link {
  color: black; /* Set your desired color, e.g., black or #343a40 */
  text-decoration: none; /* Remove underline if present */
  font-weight: 600; /* Keep the font-semibold weight */
}


/* Existing brand and navbar interior styles */
.brand-v {
  font-family: 'Montserrat', sans-serif;
  font-size: 40px;
  font-weight: 700;
  color: #007bff;
}

.brand-one {
  font-family: 'Open Sans', sans-serif;
  font-size: 30px;
  color: #343a40;
}

div.navbar-div {
  margin-top: 1%;
  margin-bottom: 0.5%;
  margin-left: 10%;
}

.dropdown-menu {
  --bs-dropdown-bg: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  border: 1px solid rgba(0, 0, 0, 0.1);
}

.navbar-link {
  font-size: 20px;
  margin-right: 20%;
}

.font-semibold {
  font-weight: 600;
}
</style>
```

