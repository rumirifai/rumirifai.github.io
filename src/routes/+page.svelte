<script lang="ts">
  type Project = {
    title: string;
    description: string;
    tags: string[];
    linkBE?: string; 
    linkFE?: string;
    linkDemo?: string;
    image?: string;
  };

  const projects: Project[] = [
    {
      title: "Himatif Apps V2",
      description: "Official website of the Unpad Informatics Engineering Student Association",
      tags: ["Express.js", "React.js", "MySQL"],
      linkDemo: "https://apps.himatif.org/",
      image: "/images/himapps.png",
    },
    {
      title: "Becycle - Waste Exchange (Full-Stack)",
      description: "Collaborative web application for management and exchange of recyclable waste, part of the PPL project.",
      tags: ["Express.js", "Flask", "React.js"],
      linkBE: "https://github.com/MSATRIAD/Project-PPL",
      linkFE: "https://github.com/rumirifai/becycle-web",
      linkDemo: "https://becycle-web.netlify.app/",
      image: "/images/becycle.png",
    },
    {
      title: "Wawacan Digital (Full-Stack)",
      description: "Semantic website for reading and searching Sundanese Wawacan manuscripts.",
      tags: ["FastAPI", "SvelteKit"],
      linkBE: "https://github.com/rumirifai/wawacan-api",
      linkFE: "https://github.com/rumirifai/wawacan-web",
      linkDemo: "https://wawacan-web.netlify.app",
      image: "/images/wawacan.png",
    },
    {
      title: "Codetid API (Backend)",
      description: "Codet.id mobile application RESTful API, for Capstone Project Bangkit 2025 batch 2",
      tags: ["Express.js", "FastAPI", "Google Cloud Platform", "Google Cloud SQL"],
      linkBE: "https://github.com/rumirifai/codetid-api",
      image: "/images/codetid.png",
    },
    {
      title: "Dominant Color Picker (Web Tool)",
      description: "Web tool to extract dominant color palette from user-uploaded images.",
      tags: ["Python", "KMeans", "Streamlit"],
      linkBE: "https://github.com/rumirifai/Dominant-Color-Picker-Website",
      linkDemo: "https://docopick.streamlit.app/",
      image: "/images/docopick.png",
    },
    {
      title: "KEPO 2024 (Static Web)",
      description: "A static informative website for the KEPO 2024 event, designed to be fast, responsive, and easily accessible to participants.",
      tags: ["Javascripts", "HTML", "CSS"],
      linkBE: "https://github.com/rumirifai/KEPO-2024-WEB-APP",
      linkDemo: "https://kepo2024.vercel.app/",
      image: "/images/kepo2024.png",
    },
  ];

  let isMenuOpen = false;
</script>

<div class="bg-stone-950 text-stone-300 font-sans">
    <nav class="bg-stone-950/80 backdrop-blur-md shadow-lg fixed top-0 w-full z-10 border-b border-stone-800/50">
        <div class="max-w-5xl mx-auto px-4">
          <div class="flex items-center justify-between h-16">
            
            <div class="flex-shrink-0">
              <h1 class="text-xl font-bold text-stone-100">Rumi Rifai</h1>
            </div>
      
            <div class="hidden md:block">
              <div class="ml-10 flex items-baseline space-x-4">
                <a href="#about" class="text-stone-300 hover:text-orange-400 transition-colors px-3 py-2 rounded-md text-sm font-medium">About</a>
                <a href="#projects" class="text-stone-300 hover:text-orange-400 transition-colors px-3 py-2 rounded-md text-sm font-medium">Projects</a>
                <a href="#experience" class="text-stone-300 hover:text-orange-400 transition-colors px-3 py-2 rounded-md text-sm font-medium">Experience</a>
                <a href="#contact" class="text-stone-300 hover:text-orange-400 transition-colors px-3 py-2 rounded-md text-sm font-medium">Contact</a>
                <!-- <a href="#blog" class="text-stone-300 hover:text-orange-400 transition-colors px-3 py-2 rounded-md text-sm font-medium">Blog</a> -->
              </div>
            </div>
      
            <div class="-mr-2 flex md:hidden">
              <button on:click={() => isMenuOpen = !isMenuOpen} type="button" class="inline-flex items-center justify-center p-2 rounded-md text-stone-400 hover:text-white hover:bg-stone-700 focus:outline-none" aria-controls="mobile-menu" aria-expanded="false">
                <span class="sr-only">Open main menu</span>
                {#if !isMenuOpen}
                  <svg class="block h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                  </svg>
                {/if}
                {#if isMenuOpen}
                  <svg class="block h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                {/if}
              </button>
            </div>
      
          </div>
        </div>
      
        {#if isMenuOpen}
          <div class="md:hidden" id="mobile-menu">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
              <a href="#about" class="text-stone-300 hover:bg-stone-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">About</a>
              <a href="#projects" class="text-stone-300 hover:bg-stone-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Projects</a>
              <a href="#experience" class="text-stone-300 hover:bg-stone-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Experience</a>
              <a href="#contact" class="text-stone-300 hover:bg-stone-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Contact</a>
              <a href="#blog" class="text-stone-300 hover:bg-stone-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Blog</a>
            </div>
          </div>
        {/if}
      </nav>

  <main class="pt-16">
    <section id="about" class="min-h-screen flex items-center justify-center text-center">
        <div class="max-w-2xl mx-auto px-4">
          <h2 class="text-4xl md:text-5xl font-bold text-stone-100 mb-4">
            Welcome! You've found my corner of the internet.
          </h2>
          <p class="text-xl md:text-2xl text-orange-400 font-medium mb-8">
            Hello! I'm Rumi. I turn coffee into code.
          </p>
          <div class="text-left max-w-md mx-auto space-y-3 text-stone-400">
            <p class="flex items-center">
              <span class="text-xl mr-3">🎓</span>
              <span>Informatics Engineering Students at <strong>Padjadjaran University</strong>.</span>
            </p>
            <p class="flex items-center">
              <span class="text-xl mr-3">💻</span>
              <span>Have high enthusiasm in software development, especially building scalable <strong>backend systems</strong>.</span>
            </p>
            <p class="flex items-center">
              <span class="text-xl mr-3">💡</span>
              <span>Always curious, committed to <strong>continuous learning</strong>, and open to new challenges.</span>
            </p>
          </div>
        </div>
    </section>

    <section id="projects" class="py-20 bg-stone-900">
        <div class="max-w-5xl mx-auto px-4">
          <h3 class="text-3xl font-bold text-center mb-12 text-stone-100">Projects</h3>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            {#each projects as project}
              <div class="bg-stone-950 rounded-lg shadow-lg hover:shadow-orange-500/10 transition-shadow flex flex-col border border-stone-800">
                {#if project.image}
                    <img src={project.image} alt={project.title} class="rounded-t-lg mb-1 w-full h-48 object-contain" />
                {/if}
                <div class="p-6 flex-grow">
                  <h4 class="font-bold text-lg mb-2 text-stone-100">{project.title}</h4>
                  <p class="text-stone-400 text-sm mb-4">{project.description}</p>
                </div>
                <div class="p-6 pt-0 mt-auto">
                  <div class="flex flex-wrap gap-2 mb-4">
                    {#each project.tags as tag}
                      <span class="text-xs font-semibold bg-orange-400/10 text-orange-300 px-2 py-1 rounded-full">{tag}</span>
                    {/each}
                  </div>
                  <div class="flex flex-col space-y-2">
                    {#if project.linkDemo}
                      <a href={project.linkDemo} target="_blank" class="block w-full text-center bg-orange-500 text-stone-900 font-bold py-2 px-4 rounded-md hover:bg-orange-600 transition-colors">
                        Live Demo
                      </a>
                    {/if}
                
                    {#if project.linkFE && project.linkBE}
                      <div class="flex space-x-2">
                        <a href={project.linkFE} target="_blank" class="block w-full text-center bg-stone-800 text-stone-100 font-semibold py-2 px-4 rounded-md hover:bg-stone-700 transition-colors">
                          Frontend
                        </a>
                        <a href={project.linkBE} target="_blank" class="block w-full text-center bg-stone-800 text-stone-100 font-semibold py-2 px-4 rounded-md hover:bg-stone-700 transition-colors">
                          Backend
                        </a>
                      </div>
                    {:else if project.linkBE && !project.linkFE}
                      <a href={project.linkBE} target="_blank" class="block w-full text-center bg-stone-800 text-stone-100 font-semibold py-2 px-4 rounded-md hover:bg-stone-700 transition-colors">
                        Code
                      </a>
                    {/if}
                </div>
                  </div>
              </div>
            {/each}
          </div>
        </div>
    </section>

    <section id="experience" class="py-20">
        <div class="max-w-3xl mx-auto px-4">
          <h3 class="text-3xl font-bold text-center mb-16 text-stone-100">Professional Experience</h3>
      
          <div class="relative border-l-2 border-stone-700 space-y-12">
            
            <div class="relative pl-10">
              <div class="absolute -left-[11px] top-1 w-5 h-5 bg-orange-500 rounded-full border-4 border-stone-900"></div>
              
              <div class="flex justify-between items-center">
                <h4 class="font-bold text-lg text-stone-100">Backend Developer & Maintainer</h4>
                <p class="text-sm text-stone-400">02/2025 – Present</p>
              </div>
              <p class="text-stone-300 font-medium mb-3">Himatif Apps | Himpunan Mahasiswa Teknik Informatika UNPAD</p>
              
              <ul class="list-disc list-outside ml-5 text-stone-400 space-y-2 text-sm">
                <li>Maintained the stability, security, and performance of all backend services for the official student association website.</li>
                <li>Developed, tested, and integrated new features and API endpoints in response to organizational requirements.</li>
                <li>Managed the MySQL database, including schema updates and routine backups to ensure data integrity.</li>
                <li>Collaborated with the frontend team to ensure seamless API integration and resolve technical issues.</li>
              </ul>
            </div>

            <div class="relative pl-10">
              <div class="absolute -left-[11px] top-1 w-5 h-5 bg-orange-500 rounded-full border-4 border-stone-900"></div>
              
              <div class="flex justify-between items-center">
                <h4 class="font-bold text-lg text-stone-100">Laboratory Teaching Assistant</h4>
                <p class="text-sm text-stone-400">02/2024 – Present</p>
              </div>
              <p class="text-stone-300 font-medium mb-3">Padjadjaran University</p>
              
              <ul class="list-disc list-outside ml-5 text-stone-400 space-y-2 text-sm">
                <li>Mentored and instructed over 50+ students in fundamental Object-Oriented Programming concepts through engaging weekly lectures.</li>
                <li>Designed and delivered a 2-hour weekly practical lecture, translating complex theories into understandable, hands-on programming exercises.</li>
                <li>Evaluated and provided constructive feedback on weekly assignments to reinforce learning objectives and improve student code quality.</li>
              </ul>
            </div>
      
            <div class="relative pl-10">
              <div class="absolute -left-[11px] top-1 w-5 h-5 bg-orange-500 rounded-full border-4 border-stone-900"></div>
      
              <div class="flex justify-between items-center">
                <h4 class="font-bold text-lg text-stone-100">Cloud Computing Cohort (Capstone Project)</h4>
                <p class="text-sm text-stone-400">09/2024 – 01/2025</p>
              </div>
              <p class="text-stone-300 font-medium mb-3">Bangkit Academy led by Google, GoTo, & Traveloka</p>
      
              <ul class="list-disc list-outside ml-5 text-stone-400 space-y-2 text-sm">
                <li>Developed and deployed a scalable backend API for the Capstone Project as a key member of a 6-person cross-functional team (Cloud, ML, Mobile).</li>
                <li>Implemented backend services using Go and PostgreSQL, deploying the application on Google Cloud Platform (GCP) utilizing services like Cloud Run and Cloud SQL.</li>
                <li>Mastered DevOps principles by completing over 40+ hands-on labs on Google Cloud Skills Boost and Dicoding, covering CI/CD, containerization, and IAM.</li>
              </ul>
            </div>
      
          </div>
        </div>
      </section>
    
    <section id="contact" class="py-20 bg-stone-900">
        <div class="text-center max-w-2xl mx-auto px-4">
          <h3 class="text-3xl font-bold mb-3 text-stone-100">Let's Connect</h3>
          <p class="text-stone-400 mb-10">
            I'm currently open to new opportunities. Feel free to reach out.
          </p>
      
          <div class="flex flex-row items-center justify-center gap-x-8">
            
            <a href="https://github.com/rumirifai" target="_blank" aria-label="My GitHub Profile" title="GitHub (@rumirifai)" class="text-stone-400 hover:text-orange-400 transition-transform hover:scale-110">
              <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" class="w-7 h-7"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.168 6.839 9.492.5.092.682-.217.682-.482 0-.237-.009-.868-.014-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.031-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844a9.564 9.564 0 012.518.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.203 2.398.1 2.651.64.7 1.03 1.595 1.03 2.688 0 3.848-2.338 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.001 10.001 0 0022 12c0-5.523-4.477-10-10-10z" clip-rule="evenodd"/></svg>
            </a>
      
            <a href="https://www.linkedin.com/in/rumirifai/" target="_blank" aria-label="Contact me via LinkedIn" title="LinkedIn (Rumi Rifai)" class="text-stone-400 hover:text-orange-400 transition-transform hover:scale-110">
              <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" class="w-7 h-7"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
            </a>
      
            <a href="mailto:rumirifai96@gmail.com" aria-label="Send me an email" title="Email (rumirifai96@gmail.com)" class="text-stone-400 hover:text-orange-400 transition-transform hover:scale-110">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7"><path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" /></svg>
            </a>
            
            <a href="/Resume_Rumi_Rifai.pdf" target="_blank" aria-label="Download my CV" title="Download my CV" class="text-stone-400 hover:text-orange-400 transition-transform hover:scale-110">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7"><path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z" /></svg>
            </a>
      
          </div>
        </div>
      </section>
  </main>

  <footer class="text-center py-6 bg-stone-900 border-t border-stone-800">
      <p class="text-stone-500 text-sm">&copy; {new Date().getFullYear()} Rumi Rifai. All rights reserved.</p>
  </footer>
</div>
