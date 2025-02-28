import { Router, Route, Redirect } from 'svelte-routing';
import About from './About.svelte'; // Pastikan path ini sesuai dengan lokasi file About.svelte
import Contact from './Contact.svelte'; // Pastikan path ini sesuai dengan lokasi file Contact.svelte

<div class="max-w-2xl px-6 py-16 mx-auto space-y-12">
    <Router>
        <Redirect from="/pages/visitor/about" to="/about" />
        <Redirect from="/pages/visitor/contact" to="/contact" />
        
        <Route path="/about" component={About} />
        <Route path="/contact" component={Contact} />
    </Router>

    <article class="space-y-8 dark:bg-gray-100 dark:text-gray-900">
        <div class="space-y-6">
            <h1 class="text-4xl font-bold md:tracking-tight md:text-5xl">
                Suspendisse ut magna et ipsum sodales accumsan.
            </h1>
            <!-- Konten lainnya di sini -->
        </div>
    </article>
</div>
