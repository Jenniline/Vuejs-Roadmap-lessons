<template>

    <navbar 
        :pages="pages"
        active-page="activePage">
    </navbar>
   
    <page-viewer 
        :page="pages[activePage]">
    </page-viewer>
    
</template>

<script>
import PageViewer from './components/PageViewer.vue';

import Navbar from './components/Navbar.vue';


 export default {
    components: {
        Navbar,
        PageViewer
    },

    data() {
            return {
                activePage: 0,
                pages: [
                    {
                        link: {text: 'Home', url: 'index.html'},
                        pageTitle: 'Home Page',
                        content: 'This is the home content'
                    },
                    {
                        link: {text: 'About', url: 'about.html'},
                        pageTitle: 'About Page',
                        content: 'This is the about content'
                    },  {
                        link: {text: 'Contact', url: 'contact.html'},
                        pageTitle: 'Contact Page',
                        content: 'This is the contact content'
                    },
                ],
                pageTitle: 'Hello, vue',
                content: 'Welcome to the Wonderful world of Vue'
            };
        },
 }
</script>