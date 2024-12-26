    <template>
        <ul class="links-list">
        <li v-for="link in links" :key="link.id">
            <a :href="link.url" target="_blank" rel="noopener noreferrer">
            {{ link.label }}
            </a>
        </li>
        </ul>
    </template>
    
    <script lang="ts" setup>
    // Tipagem para os Links
    interface Link {
        id: number;
        label: string;
        url: string;
    }
    
    // Props recebidas do componente pai
    defineProps<{ links: Link[] }>();
    </script>
    
    <style scoped>
    .links-list {
        list-style-type: none;
        padding: 0;
    }
    
    .links-list li {
        margin: 10px 0;
    }
    
    .links-list a {
        text-decoration: none;
        font-size: 18px;
        color: #2575fc;
        font-weight: bold;
    }
    
    .links-list a:hover {
        color: #1a5bb8;
    }
    </style>
    