<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Workshop PLC - Event Setup Design, Branding & Construction</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              dark: '#1E2923',
              green: '#2A3831',
              lightGreen: '#3C4F46',
              ochre: '#D88435',
              ochreDark: '#B86A22',
              bgLight: '#F7F8F6',
              surface: '#FFFFFF',
              border: '#E2E8F0',
              textPrimary: '#1F2937',
              textSecondary: '#4B5563'
            }
          },
          fontFamily: {
            sans: ['Inter', 'sans-serif']
          }
        }
      }
    }
  </script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    
    html {
      scroll-behavior: smooth;
    }
    
    body {
      font-family: 'Inter', sans-serif;
      background-color: #F7F8F6;
      color: #1F2937;
    }

    /* Slider animation */
    .slide-enter {
      opacity: 0;
      transform: scale(1.03);
      transition: opacity 0.7s ease-in-out, transform 0.7s ease-in-out;
    }
    .slide-active {
      opacity: 1;
      transform: scale(1);
      transition: opacity 0.7s ease-in-out, transform 0.7s ease-in-out;
    }

    /* Custom solid clean card shadow */
    .clean-card {
      background: #FFFFFF;
      border: 1px solid #E2E8F0;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
      transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
    }
    .clean-card:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
      border-color: #CBD5E1;
    }
  </style>
</head>
<body class="antialiased flex flex-col min-h-screen">

  <!-- TOP HEADER / NAV -->
  <header class="sticky top-0 z-50 bg-brand-dark text-white border-b border-brand-lightGreen/40 shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      
      <!-- Logo -->
      <a href="#home" class="flex items-center gap-3">
        <div class="bg-brand-ochre text-white font-black text-2xl w-10 h-10 rounded flex items-center justify-center shadow">
          W
        </div>
        <div>
          <span class="text-xl font-bold tracking-tight text-white block leading-none">The Workshop<span class="text-brand-ochre">.</span></span>
          <span class="text-[10px] text-gray-400 uppercase tracking-widest block font-medium mt-1">PLC Ethiopia</span>
        </div>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
        <a href="#about" class="text-gray-200 hover:text-brand-ochre transition">About Us</a>
        <a href="#services" class="text-gray-200 hover:text-brand-ochre transition">Services</a>
        <a href="#portfolio" class="text-gray-200 hover:text-brand-ochre transition">Track Record</a>
        <a href="#team" class="text-gray-200 hover:text-brand-ochre transition">Leadership</a>
        <a href="#calculator" class="text-gray-200 hover:text-brand-ochre transition">Estimator</a>
        <a href="#contact" class="bg-brand-ochre hover:bg-brand-ochreDark text-white px-5 py-2.5 rounded font-semibold transition shadow-sm">
          Contact Us
        </a>
      </nav>

      <!-- Mobile Menu Button -->
      <button id="mobileMenuBtn" class="md:hidden text-gray-300 hover:text-white p-2 focus:outline-none">
        <i class="fa-solid fa-bars text-2xl"></i>
      </button>
    </div>

    <!-- Mobile Nav Dropdown -->
    <div id="mobileMenu" class="hidden md:hidden bg-brand-green border-t border-brand-lightGreen px-4 pt-3 pb-6 space-y-3">
      <a href="#about" class="block text-gray-200 hover:text-brand-ochre py-1">About Us</a>
      <a href="#services" class="block text-gray-200 hover:text-brand-ochre py-1">Services</a>
      <a href="#portfolio" class="block text-gray-200 hover:text-brand-ochre py-1">Track Record</a>
      <a href="#team" class="block text-gray-200 hover:text-brand-ochre py-1">Leadership</a>
      <a href="#calculator" class="block text-gray-200 hover:text-brand-ochre py-1">Estimator</a>
      <a href="#contact" class="block bg-brand-ochre text-white text-center py-2.5 rounded font-medium mt-2">Contact Us</a>
    </div>
  </header>

  <main class="flex-grow">

    <!-- HERO SECTION WITH SLIDING ANIMATED SHOWCASE -->
    <section id="home" class="relative bg-brand-green text-white overflow-hidden py-12 lg:py-20">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
          
          <!-- Hero Text Content -->
          <div class="lg:col-span-5 space-y-6">
            <div class="inline-flex items-center gap-2 bg-brand-ochre/20 border border-brand-ochre/40 px-3 py-1 rounded-full text-brand-ochre text-xs font-semibold uppercase tracking-wider">
              <i class="fa-solid fa-square-check text-xs"></i> Sister Company to Ethel Events
            </div>
            <h1 class="text-3xl sm:text-4xl lg:text-5xl font-extrabold text-white leading-tight">
              Event Setup, Design & <span class="text-brand-ochre">Custom Booth</span> Construction
            </h1>
            <p class="text-gray-300 text-base sm:text-lg leading-relaxed">
              We transform event spaces in Ethiopia and East Africa into engaging, functional, and visually compelling brand environments through precision 3D design, fabrication, and large-format printing.
            </p>
            <div class="flex flex-wrap gap-4 pt-2">
              <a href="#portfolio" class="bg-brand-ochre hover:bg-brand-ochreDark text-white font-semibold px-6 py-3 rounded shadow transition flex items-center gap-2">
                View Our Projects <i class="fa-solid fa-arrow-right text-sm"></i>
              </a>
              <a href="#contact" class="bg-transparent hover:bg-white/10 text-white font-semibold px-6 py-3 rounded border border-white/30 transition">
                Get In Touch
              </a>
            </div>

            <!-- Key Metrics -->
            <div class="grid grid-cols-3 gap-4 pt-6 border-t border-brand-lightGreen/50 text-center">
              <div>
                <p class="text-2xl sm:text-3xl font-extrabold text-brand-ochre">10+</p>
                <p class="text-xs text-gray-300">Years Synergy</p>
              </div>
              <div>
                <p class="text-2xl sm:text-3xl font-extrabold text-brand-ochre">8+</p>
                <p class="text-xs text-gray-300">Big 5 Custom Booths</p>
              </div>
              <div>
                <p class="text-2xl sm:text-3xl font-extrabold text-brand-ochre">100%</p>
                <p class="text-xs text-gray-300">Turnkey Execution</p>
              </div>
            </div>
          </div>

          <!-- Interactive Animated Image Slider Showcase -->
          <div class="lg:col-span-7">
            <div class="relative bg-brand-dark rounded-xl border border-brand-lightGreen/60 overflow-hidden shadow-2xl group">
              
              <!-- Slide Container -->
              <div id="sliderContainer" class="relative w-full h-[320px] sm:h-[420px] overflow-hidden">
                
                <!-- Slide 1 -->
                <div class="slide-item absolute inset-0 opacity-100 transition-all duration-700">
                  <img src="https://images.unsplash.com/photo-1511578314322-379afb476865?auto=format&fit=crop&w=1200&q=80" alt="Exhibition Booth Construction" class="w-full h-full object-cover">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent flex items-end p-6">
                    <div>
                      <span class="bg-brand-ochre text-xs font-bold uppercase px-2.5 py-1 rounded text-white mb-2 inline-block">Exhibition Construction</span>
                      <h3 class="text-xl font-bold text-white">Big 5 Construct Ethiopia Custom Booths</h3>
                      <p class="text-xs text-gray-200 mt-1">Tailored 3D architectural booth design and precision on-site setup.</p>
                    </div>
                  </div>
                </div>

                <!-- Slide 2 -->
                <div class="slide-item absolute inset-0 opacity-0 transition-all duration-700">
                  <img src="https://images.unsplash.com/photo-1540575861501-7cf05a4b125a?auto=format&fit=crop&w=1200&q=80" alt="3D Event Setup & Lighting" class="w-full h-full object-cover">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent flex items-end p-6">
                    <div>
                      <span class="bg-brand-ochre text-xs font-bold uppercase px-2.5 py-1 rounded text-white mb-2 inline-block">3D Stage & Lighting</span>
                      <h3 class="text-xl font-bold text-white">Ethio Health & Corporate Trade Shows</h3>
                      <p class="text-xs text-gray-200 mt-1">Innovative technical planning and immersive lighting solutions.</p>
                    </div>
                  </div>
                </div>

                <!-- Slide 3 -->
                <div class="slide-item absolute inset-0 opacity-0 transition-all duration-700">
                  <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?auto=format&fit=crop&w=1200&q=80" alt="High Quality Printing & Branding" class="w-full h-full object-cover">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent flex items-end p-6">
                    <div>
                      <span class="bg-brand-ochre text-xs font-bold uppercase px-2.5 py-1 rounded text-white mb-2 inline-block">In-House Printing</span>
                      <h3 class="text-xl font-bold text-white">High-Precision Large Format Printing</h3>
                      <p class="text-xs text-gray-200 mt-1">State-of-the-art digital printing for vibrant indoor and outdoor branding.</p>
                    </div>
                  </div>
                </div>

                <!-- Slide 4 -->
                <div class="slide-item absolute inset-0 opacity-0 transition-all duration-700">
                  <img src="https://images.unsplash.com/photo-1475721027785-f74eccf877e2?auto=format&fit=crop&w=1200&q=80" alt="Stride Ethiopia Expo" class="w-full h-full object-cover">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent flex items-end p-6">
                    <div>
                      <span class="bg-brand-ochre text-xs font-bold uppercase px-2.5 py-1 rounded text-white mb-2 inline-block">Space Branding</span>
                      <h3 class="text-xl font-bold text-white">STRIDE Ethiopia Expo & Agrofood</h3>
                      <p class="text-xs text-gray-200 mt-1">Comprehensive arena branding, signage, and material deployment.</p>
                    </div>
                  </div>
                </div>

              </div>

              <!-- Slide Controls (Arrows) -->
              <button id="prevSlide" class="absolute left-3 top-1/2 -translate-y-1/2 bg-black/50 hover:bg-brand-ochre text-white w-10 h-10 rounded-full flex items-center justify-center transition border border-white/20">
                <i class="fa-solid fa-chevron-left"></i>
              </button>
              <button id="nextSlide" class="absolute right-3 top-1/2 -translate-y-1/2 bg-black/50 hover:bg-brand-ochre text-white w-10 h-10 rounded-full flex items-center justify-center transition border border-white/20">
                <i class="fa-solid fa-chevron-right"></i>
              </button>

              <!-- Slide Indicators / Dots -->
              <div id="slideDots" class="absolute bottom-3 left-1/2 -translate-x-1/2 flex space-x-2">
                <button class="w-3 h-3 rounded-full bg-brand-ochre transition-all" data-index="0"></button>
                <button class="w-3 h-3 rounded-full bg-white/50 hover:bg-white transition-all" data-index="1"></button>
                <button class="w-3 h-3 rounded-full bg-white/50 hover:bg-white transition-all" data-index="2"></button>
                <button class="w-3 h-3 rounded-full bg-white/50 hover:bg-white transition-all" data-index="3"></button>
              </div>

            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ABOUT & SYNERGY WITH ETHEL EVENTS -->
    <section id="about" class="py-16 bg-white border-b border-brand-border">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto mb-12">
          <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Background & Synergy</h2>
          <p class="text-3xl font-extrabold text-brand-dark">Built on Over a Decade of Industry Leadership</p>
          <div class="w-16 h-1 bg-brand-ochre mx-auto mt-4 rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          
          <div class="space-y-5 text-brand-textSecondary text-base leading-relaxed">
            <p>
              <strong class="text-brand-dark">The Workshop PLC</strong> is a dynamic and innovative company operating as a sister company to <strong class="text-brand-dark">Ethel Events and Communication</strong>, an established leader in the event management industry in Ethiopia.
            </p>
            <p>
              With over a decade of expertise in organizing major trade fairs and corporate events, Ethel Events has built a reputation for excellence by serving multinational corporations, government entities, and private sector leaders.
            </p>
            <p>
              Leveraging this rich heritage, The Workshop PLC was specifically established to focus on <span class="text-brand-dark font-semibold">branding, 3D event setup design, custom booth construction, and high-quality fabrication</span>. We transform event spaces into engaging, interactive environments that captivate attendees and elevate client brand equity.
            </p>
            
            <div class="pt-4 grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div class="clean-card p-4 rounded-lg flex items-start gap-3">
                <i class="fa-solid fa-bullseye text-brand-ochre text-xl mt-1"></i>
                <div>
                  <h4 class="font-bold text-brand-dark text-sm">Our Mission</h4>
                  <p class="text-xs text-gray-600 mt-1">Delivering exceptional setup design, construction, consultation, and high-grade printing for seamless event success.</p>
                </div>
              </div>

              <div class="clean-card p-4 rounded-lg flex items-start gap-3">
                <i class="fa-solid fa-eye text-brand-ochre text-xl mt-1"></i>
                <div>
                  <h4 class="font-bold text-brand-dark text-sm">Our Vision</h4>
                  <p class="text-xs text-gray-600 mt-1">To become the leading full-fledged event branding and specialized setup service provider across East Africa.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Core Values Grid -->
          <div class="bg-brand-bgLight p-6 sm:p-8 rounded-xl border border-brand-border space-y-4">
            <h3 class="text-xl font-bold text-brand-dark mb-4 border-b border-gray-200 pb-3 flex items-center gap-2">
              <i class="fa-solid fa-star text-brand-ochre"></i> Our Core Values
            </h3>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div class="bg-white p-3.5 rounded border border-gray-200">
                <h4 class="font-bold text-brand-green text-sm flex items-center gap-2">
                  <i class="fa-solid fa-check text-brand-ochre text-xs"></i> Quality
                </h4>
                <p class="text-xs text-gray-600 mt-1">Highest safety, sustainability, and quality standards in every build.</p>
              </div>

              <div class="bg-white p-3.5 rounded border border-gray-200">
                <h4 class="font-bold text-brand-green text-sm flex items-center gap-2">
                  <i class="fa-solid fa-sliders text-brand-ochre text-xs"></i> Flexibility
                </h4>
                <p class="text-xs text-gray-600 mt-1">Custom-tailored event setups designed to align with client budget specs.</p>
              </div>

              <div class="bg-white p-3.5 rounded border border-gray-200">
                <h4 class="font-bold text-brand-green text-sm flex items-center gap-2">
                  <i class="fa-solid fa-lightbulb text-brand-ochre text-xs"></i> Innovation
                </h4>
                <p class="text-xs text-gray-600 mt-1">Cutting-edge 3D technical designs and creative interactive displays.</p>
              </div>

              <div class="bg-white p-3.5 rounded border border-gray-200">
                <h4 class="font-bold text-brand-green text-sm flex items-center gap-2">
                  <i class="fa-solid fa-list-check text-brand-ochre text-xs"></i> End-to-End
                </h4>
                <p class="text-xs text-gray-600 mt-1">Managing every step from concept and prototyping to on-site dismantle.</p>
              </div>
            </div>

            <div class="bg-brand-green text-white p-4 rounded mt-4 flex items-center justify-between">
              <div>
                <p class="text-xs font-semibold uppercase text-brand-ochre">Dedicated Support</p>
                <p class="text-sm font-medium">In-house printing, senior designers, and technical operations team.</p>
              </div>
              <i class="fa-solid fa-gears text-2xl text-brand-ochre"></i>
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- OUR SERVICES (3 MAIN CATEGORIES) -->
    <section id="services" class="py-16 bg-brand-bgLight">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto mb-14">
          <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Complete Solutions</h2>
          <p class="text-3xl font-extrabold text-brand-dark">Our Specialized Service Offerings</p>
          <p class="text-sm text-brand-textSecondary mt-2">Comprehensive branding, 3D setup design, and custom construction tailored for corporate excellence.</p>
          <div class="w-16 h-1 bg-brand-ochre mx-auto mt-4 rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          
          <!-- Category 1: Printing and Branding -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white border-b-4 border-brand-ochre">
              <div class="w-12 h-12 bg-white/10 rounded-lg flex items-center justify-center text-brand-ochre text-2xl mb-3">
                <i class="fa-solid fa-print"></i>
              </div>
              <h3 class="text-xl font-bold">1. Printing & Branding</h3>
              <p class="text-xs text-gray-300 mt-1">High-impact indoor & outdoor promotional media</p>
            </div>
            <div class="p-6 flex-grow space-y-4 text-sm text-brand-textSecondary">
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Promotional Items
                </h4>
                <p class="text-xs text-gray-600 mt-1">Custom-made promotional products highlighting brand identity and creating lasting customer impressions.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Digital & Paper Printing
                </h4>
                <p class="text-xs text-gray-600 mt-1">State-of-the-art printing machines producing crisp, vibrant, and durable indoor/outdoor graphics.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Space Branding Services
                </h4>
                <p class="text-xs text-gray-600 mt-1">Transforming offices, showrooms, and display areas with wall graphics, signage, and branded finishes.</p>
              </div>
            </div>
          </div>

          <!-- Category 2: Design and Services -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white border-b-4 border-brand-ochre">
              <div class="w-12 h-12 bg-white/10 rounded-lg flex items-center justify-center text-brand-ochre text-2xl mb-3">
                <i class="fa-solid fa-cubes"></i>
              </div>
              <h3 class="text-xl font-bold">2. Design & Technical</h3>
              <p class="text-xs text-gray-300 mt-1">Spatial 3D design & operational management</p>
            </div>
            <div class="p-6 flex-grow space-y-4 text-sm text-brand-textSecondary">
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Event Setup 3D Design
                </h4>
                <p class="text-xs text-gray-600 mt-1">Detailed 3D design renders enabling clients to visualize and adjust event layouts prior to physical construction.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Graphic Design
                </h4>
                <p class="text-xs text-gray-600 mt-1">Crafting compelling visuals and graphics from initial creative concepts to final production.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Event HR Supply
                </h4>
                <p class="text-xs text-gray-600 mt-1">Supplying trained event personnel including ushers, parking attendants, security, and setup staff.</p>
              </div>
            </div>
          </div>

          <!-- Category 3: Construction & Rental Services -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white border-b-4 border-brand-ochre">
              <div class="w-12 h-12 bg-white/10 rounded-lg flex items-center justify-center text-brand-ochre text-2xl mb-3">
                <i class="fa-solid fa-hammer"></i>
              </div>
              <h3 class="text-xl font-bold">3. Construction & Rentals</h3>
              <p class="text-xs text-gray-300 mt-1">Custom booth building & event gear rentals</p>
            </div>
            <div class="p-6 flex-grow space-y-4 text-sm text-brand-textSecondary">
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Custom Exhibition Booths
                </h4>
                <p class="text-xs text-gray-600 mt-1">Designing and building bespoke exhibition stands that engage visitors and maximize brand visibility.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Bespoke Material Production
                </h4>
                <p class="text-xs text-gray-600 mt-1">Fabricating custom podiums, stages, brochure racks, and tailored furniture items.</p>
              </div>
              <div>
                <h4 class="font-bold text-brand-dark flex items-center gap-2">
                  <i class="fa-solid fa-circle-dot text-brand-ochre text-[10px]"></i> Event Material Rental
                </h4>
                <p class="text-xs text-gray-600 mt-1">Comprehensive rental inventory including TVs, carpets, executive chairs, tables, sofas, and exhibition stands.</p>
              </div>
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- TRACK RECORD & MAJOR EXHIBITIONS SHOWCASE -->
    <section id="portfolio" class="py-16 bg-white border-b border-brand-border">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
          <div>
            <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Proven Track Record</h2>
            <p class="text-3xl font-extrabold text-brand-dark">Major Trade Fairs & Projects</p>
          </div>
          <p class="text-sm text-brand-textSecondary mt-2 md:mt-0 max-w-md">
            Full event setup and branding delivered for Ethiopia's premier international expos.
          </p>
        </div>

        <!-- Major Featured Project Banner: Big 5 Construct -->
        <div class="bg-brand-green rounded-xl p-6 sm:p-8 text-white mb-10 shadow-lg border border-brand-lightGreen">
          <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
            <div class="lg:col-span-7 space-y-4">
              <div class="inline-block bg-brand-ochre text-white text-xs font-bold px-3 py-1 rounded">
                Flagship Project
              </div>
              <h3 class="text-2xl sm:text-3xl font-extrabold">Big 5 Construct Ethiopia</h3>
              <p class="text-gray-200 text-sm leading-relaxed">
                The Workshop PLC successfully produced <strong class="text-white">8 custom-made exhibition booths</strong> for Big 5 Construct Ethiopia, the largest international construction trade show in the region. Included 3D spatial renders, structural engineering, on-site setup, and dismantling.
              </p>
              <div class="flex flex-wrap gap-2 pt-2 text-xs">
                <span class="bg-brand-dark/60 border border-brand-lightGreen px-3 py-1 rounded text-gray-300">3D Design Renders</span>
                <span class="bg-brand-dark/60 border border-brand-lightGreen px-3 py-1 rounded text-gray-300">On-site Logistics</span>
                <span class="bg-brand-dark/60 border border-brand-lightGreen px-3 py-1 rounded text-gray-300">Custom Lighting & Finishing</span>
              </div>
            </div>

            <div class="lg:col-span-5 grid grid-cols-2 gap-3">
              <div class="rounded-lg overflow-hidden border border-white/20 h-32">
                <img src="https://images.unsplash.com/photo-1511578314322-379afb476865?auto=format&fit=crop&w=600&q=80" alt="Big 5 Stand 1" class="w-full h-full object-cover">
              </div>
              <div class="rounded-lg overflow-hidden border border-white/20 h-32">
                <img src="https://images.unsplash.com/photo-1475721027785-f74eccf877e2?auto=format&fit=crop&w=600&q=80" alt="Big 5 Stand 2" class="w-full h-full object-cover">
              </div>
            </div>
          </div>
        </div>

        <!-- Track Record Grid -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          
          <div class="clean-card rounded-lg overflow-hidden p-5">
            <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold text-lg mb-3">
              01
            </div>
            <h4 class="font-bold text-brand-dark text-base">Big 5 Construct Ethiopia</h4>
            <p class="text-xs text-brand-textSecondary mt-2">Comprehensive branding, custom booth construction, and technical drawings for top construction exhibitors.</p>
          </div>

          <div class="clean-card rounded-lg overflow-hidden p-5">
            <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold text-lg mb-3">
              02
            </div>
            <h4 class="font-bold text-brand-dark text-base">Ethiopia Agrofood Expo</h4>
            <p class="text-xs text-brand-textSecondary mt-2">Large format printing, arena branding, and specialized promotional booth setups.</p>
          </div>

          <div class="clean-card rounded-lg overflow-hidden p-5">
            <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold text-lg mb-3">
              03
            </div>
            <h4 class="font-bold text-brand-dark text-base">Ethio Health Exhibition</h4>
            <p class="text-xs text-brand-textSecondary mt-2">Stage setup, high-resolution signage, and full space branding for medical and pharmaceutical forums.</p>
          </div>

          <div class="clean-card rounded-lg overflow-hidden p-5">
            <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold text-lg mb-3">
              04
            </div>
            <h4 class="font-bold text-brand-dark text-base">STRIDE Ethiopia Expo</h4>
            <p class="text-xs text-brand-textSecondary mt-2">Custom event material fabrication, usher personnel supply, and full event lifecycle operations.</p>
          </div>

        </div>

      </div>
    </section>

    <!-- KEY LEADERSHIP / TEAM SECTION (UPDATED: ONLY HAIMANOT, DANIEL, FASIL) -->
    <section id="team" class="py-16 bg-brand-bgLight">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto mb-14">
          <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Our Key Personnel</h2>
          <p class="text-3xl font-extrabold text-brand-dark">Experienced Leadership Team</p>
          <p class="text-sm text-brand-textSecondary mt-2">Seasoned professionals driving innovation, creative setup design, and operational excellence.</p>
          <div class="w-16 h-1 bg-brand-ochre mx-auto mt-4 rounded-full"></div>
        </div>

        <!-- 3 Key Team Members -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          
          <!-- Haimanot Tesfaye -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white text-center border-b-4 border-brand-ochre">
              <div class="w-24 h-24 mx-auto rounded-full bg-brand-lightGreen border-2 border-brand-ochre flex items-center justify-center text-3xl font-bold text-white mb-3 shadow">
                HT
              </div>
              <h3 class="text-xl font-bold">Haimanot Tesfaye</h3>
              <p class="text-xs text-brand-ochre font-semibold uppercase tracking-wider mt-1">Chief Executive Officer (CEO)</p>
            </div>
            <div class="p-6 flex-grow space-y-3 text-xs text-brand-textSecondary leading-relaxed">
              <p>
                Haimanot Tesfaye brings a wealth of expertise to The Workshop PLC with over <strong class="text-brand-dark">10 years of experience</strong> in event management and 4 years in marketing, media, and branding.
              </p>
              <p>
                She has successfully led numerous high-profile corporate events and trade shows in Ethiopia. Haimanot is also the Founder & CEO of <strong class="text-brand-dark">Ethel Events and Communication</strong>.
              </p>
              <div class="pt-2 border-t border-gray-200 flex items-center gap-2 text-brand-dark font-medium">
                <i class="fa-solid fa-award text-brand-ochre"></i> Strategy & Executive Vision
              </div>
            </div>
          </div>

          <!-- Daniel Tesfaye -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white text-center border-b-4 border-brand-ochre">
              <div class="w-24 h-24 mx-auto rounded-full bg-brand-lightGreen border-2 border-brand-ochre flex items-center justify-center text-3xl font-bold text-white mb-3 shadow">
                DT
              </div>
              <h3 class="text-xl font-bold">Daniel Tesfaye</h3>
              <p class="text-xs text-brand-ochre font-semibold uppercase tracking-wider mt-1">Head of Creative & Production</p>
            </div>
            <div class="p-6 flex-grow space-y-3 text-xs text-brand-textSecondary leading-relaxed">
              <p>
                Daniel Tesfaye, co-founder of Ethel Events and Communication, is an <strong class="text-brand-dark">Electrical Engineer</strong> by profession with over <strong class="text-brand-dark">10 years of experience</strong> in graphics and 3D setup design.
              </p>
              <p>
                His deep technical background combined with creative vision ensures every event setup is both visually stunning and structurally sound.
              </p>
              <div class="pt-2 border-t border-gray-200 flex items-center gap-2 text-brand-dark font-medium">
                <i class="fa-solid fa-pen-ruler text-brand-ochre"></i> 3D Design & Technical Renders
              </div>
            </div>
          </div>

          <!-- Fasil Endalamaw -->
          <div class="clean-card rounded-xl overflow-hidden flex flex-col">
            <div class="bg-brand-green p-6 text-white text-center border-b-4 border-brand-ochre">
              <div class="w-24 h-24 mx-auto rounded-full bg-brand-lightGreen border-2 border-brand-ochre flex items-center justify-center text-3xl font-bold text-white mb-3 shadow">
                FE
              </div>
              <h3 class="text-xl font-bold">Fasil Endalamaw</h3>
              <p class="text-xs text-brand-ochre font-semibold uppercase tracking-wider mt-1">Production Manager</p>
            </div>
            <div class="p-6 flex-grow space-y-3 text-xs text-brand-textSecondary leading-relaxed">
              <p>
                Fasil Endalamaw is a seasoned <strong class="text-brand-dark">Civil Engineer</strong> with extensive experience in fabricating both temporary exhibition booths and permanent space branding structures.
              </p>
              <p>
                He oversees on-site production, safety compliance, structural integrity, and logistical execution from ground setup to post-event teardown.
              </p>
              <div class="pt-2 border-t border-gray-200 flex items-center gap-2 text-brand-dark font-medium">
                <i class="fa-solid fa-helmet-safety text-brand-ochre"></i> On-Site Engineering & Fabrication
              </div>
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- INTERACTIVE ESTIMATE CALCULATOR TOOL -->
    <section id="calculator" class="py-16 bg-white border-y border-brand-border">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-2xl mx-auto mb-10">
          <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Instant Planning Tool</h2>
          <p class="text-3xl font-extrabold text-brand-dark">Event Setup Cost Estimator</p>
          <p class="text-xs text-brand-textSecondary mt-2">Get an estimated range for your custom booth, branding, or rental package in Ethiopia.</p>
        </div>

        <div class="clean-card p-6 sm:p-8 rounded-xl">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            
            <!-- Controls -->
            <div class="space-y-5">
              <div>
                <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-2">
                  1. Event Setup Type
                </label>
                <select id="calcType" class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                  <option value="booth">Custom Exhibition Booth Fabrication</option>
                  <option value="branding">Office / Space Branding Services</option>
                  <option value="rental">Event Material & Furniture Rental</option>
                  <option value="full">Full Turnkey Event Setup (3D + Print + Build)</option>
                </select>
              </div>

              <div>
                <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-2">
                  2. Area Size (Sqm): <span id="areaVal" class="text-brand-ochre font-extrabold">18</span> sq.m
                </label>
                <input type="range" id="calcArea" min="9" max="200" step="1" value="18" class="w-full accent-brand-ochre cursor-pointer">
                <div class="flex justify-between text-[10px] text-gray-500 mt-1">
                  <span>9 sq.m (Standard)</span>
                  <span>100 sq.m</span>
                  <span>200+ sq.m</span>
                </div>
              </div>

              <div>
                <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-2">
                  3. Additional Services
                </label>
                <div class="space-y-2 text-xs">
                  <label class="flex items-center gap-2 cursor-pointer">
                    <input type="checkbox" id="addDesign" checked class="rounded border-gray-300 text-brand-ochre focus:ring-brand-ochre">
                    <span>3D Technical Architectural Renderings</span>
                  </label>
                  <label class="flex items-center gap-2 cursor-pointer">
                    <input type="checkbox" id="addHR" class="rounded border-gray-300 text-brand-ochre focus:ring-brand-ochre">
                    <span>On-site Event Personnel (Ushers & Security)</span>
                  </label>
                  <label class="flex items-center gap-2 cursor-pointer">
                    <input type="checkbox" id="addDismantle" checked class="rounded border-gray-300 text-brand-ochre focus:ring-brand-ochre">
                    <span>Post-Event Teardown & Logistics</span>
                  </label>
                </div>
              </div>
            </div>

            <!-- Estimated Calculation Result -->
            <div class="bg-brand-green text-white p-6 rounded-lg flex flex-col justify-between border border-brand-lightGreen">
              <div>
                <span class="text-[10px] uppercase font-bold text-brand-ochre tracking-widest block mb-1">Budget Overview</span>
                <h4 class="text-xl font-bold">Estimated Cost Breakdown</h4>
                <p class="text-xs text-gray-300 mt-1">Based on standard materials, printing specifications, and on-site support in Addis Ababa.</p>
                
                <div class="mt-6 pt-4 border-t border-brand-lightGreen/60 space-y-2 text-xs">
                  <div class="flex justify-between">
                    <span class="text-gray-300">Base Fabrication Rate:</span>
                    <span id="rateEst" class="font-bold text-white">ETB 1,800 / sq.m</span>
                  </div>
                  <div class="flex justify-between">
                    <span class="text-gray-300">Estimated Setup Days:</span>
                    <span id="daysEst" class="font-bold text-white">2 - 3 Days</span>
                  </div>
                </div>
              </div>

              <div class="mt-8 pt-4 border-t border-brand-lightGreen">
                <div class="text-xs text-gray-300">Estimated Budget Range:</div>
                <div id="totalEst" class="text-2xl sm:text-3xl font-extrabold text-brand-ochre mt-1">
                  ETB 45,000 - 65,000
                </div>
                <p class="text-[10px] text-gray-400 mt-1">*Final quote depends on material choices and custom 3D design specs.</p>
                
                <a href="#contact" class="mt-4 block text-center bg-brand-ochre hover:bg-brand-ochreDark text-white text-xs font-bold py-2.5 rounded transition">
                  Request Official Proposal
                </a>
              </div>
            </div>

          </div>
        </div>

      </div>
    </section>

    <!-- CONTACT & LOCATION SECTION -->
    <section id="contact" class="py-16 bg-brand-bgLight">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
          
          <!-- Contact Information & Address -->
          <div class="lg:col-span-5 space-y-6">
            <div>
              <h2 class="text-xs font-bold text-brand-ochre uppercase tracking-widest mb-2">Get In Touch</h2>
              <p class="text-3xl font-extrabold text-brand-dark">Let's Build Your Next Event</p>
              <p class="text-xs text-brand-textSecondary mt-2">Visit our office or reach out to discuss your exhibition, printing, and event setup requirements.</p>
            </div>

            <div class="space-y-4 text-sm">
              <div class="clean-card p-4 rounded-lg flex items-start gap-4">
                <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold shrink-0">
                  <i class="fa-solid fa-location-dot"></i>
                </div>
                <div>
                  <h4 class="font-bold text-brand-dark text-sm">Headquarters Address</h4>
                  <p class="text-xs text-gray-600 mt-1">Bole, Atlas, Noah Centrum Apartment, Ground Floor</p>
                  <p class="text-xs text-gray-500">Addis Ababa, Ethiopia</p>
                </div>
              </div>

              <div class="clean-card p-4 rounded-lg flex items-start gap-4">
                <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold shrink-0">
                  <i class="fa-solid fa-phone"></i>
                </div>
                <div>
                  <h4 class="font-bold text-brand-dark text-sm">Phone Numbers</h4>
                  <p class="text-xs text-gray-600 mt-1">+251 920 69 29 91</p>
                  <p class="text-xs text-gray-600">+251 911 25 92 29</p>
                </div>
              </div>

              <div class="clean-card p-4 rounded-lg flex items-start gap-4">
                <div class="w-10 h-10 bg-brand-ochre/10 rounded flex items-center justify-center text-brand-ochre font-bold shrink-0">
                  <i class="fa-solid fa-envelope"></i>
                </div>
                <div>
                  <h4 class="font-bold text-brand-dark text-sm">Email Inquiry</h4>
                  <p class="text-xs text-brand-ochre font-medium mt-1">info@theworkshopet.com</p>
                </div>
              </div>
            </div>

            <!-- Affiliation Banner -->
            <div class="bg-brand-green text-white p-4 rounded-lg text-xs space-y-1">
              <p class="font-bold text-brand-ochre">Affiliated Sister Company:</p>
              <p class="text-gray-300">Ethel Events and Communication PLC</p>
            </div>
          </div>

          <!-- Contact Form -->
          <div class="lg:col-span-7">
            <div class="clean-card p-6 sm:p-8 rounded-xl">
              <h3 class="text-xl font-bold text-brand-dark mb-4 border-b border-gray-200 pb-3">Send Us a Direct Message</h3>
              
              <form id="contactForm" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                  <div>
                    <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Full Name *</label>
                    <input type="text" required placeholder="e.g. Abebe Kebede" class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                  </div>
                  <div>
                    <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Company / Organization</label>
                    <input type="text" placeholder="e.g. Ethio Telecom" class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                  </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                  <div>
                    <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Phone Number *</label>
                    <input type="tel" required placeholder="+251 9..." class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                  </div>
                  <div>
                    <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Email Address *</label>
                    <input type="email" required placeholder="name@company.com" class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                  </div>
                </div>

                <div>
                  <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Service Interest</label>
                  <select class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre">
                    <option>Exhibition Booth Construction</option>
                    <option>Printing & Space Branding</option>
                    <option>Event Setup 3D Design</option>
                    <option>Material Rental Services</option>
                    <option>General Inquiry / Consultation</option>
                  </select>
                </div>

                <div>
                  <label class="block text-xs font-bold text-brand-dark uppercase tracking-wider mb-1">Project Details / Message *</label>
                  <textarea rows="4" required placeholder="Please describe your event dates, booth dimensions, or branding scope..." class="w-full bg-brand-bgLight border border-gray-300 rounded p-2.5 text-sm text-brand-dark focus:outline-none focus:border-brand-ochre"></textarea>
                </div>

                <button type="submit" class="w-full bg-brand-ochre hover:bg-brand-ochreDark text-white font-bold py-3 rounded transition shadow flex items-center justify-center gap-2 text-sm">
                  <i class="fa-solid fa-paper-plane"></i> Send Project Inquiry
                </button>

                <div id="formStatus" class="hidden text-xs text-center p-3 rounded bg-green-100 text-green-800 font-medium">
                  Thank you! Your inquiry has been received. Our team will contact you shortly.
                </div>
              </form>
            </div>
          </div>

        </div>

      </div>
    </section>

  </main>

  <!-- FOOTER -->
  <footer class="bg-brand-dark text-white border-t border-brand-lightGreen/40 py-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8 text-xs text-gray-300">
        
        <div class="space-y-3">
          <div class="flex items-center gap-2">
            <div class="bg-brand-ochre text-white font-bold text-lg w-8 h-8 rounded flex items-center justify-center">W</div>
            <span class="text-base font-bold text-white">The Workshop PLC</span>
          </div>
          <p class="leading-relaxed">Custom event setup, 3D design renders, exhibition stand building, and high-precision printing solutions in Ethiopia.</p>
        </div>

        <div>
          <h4 class="font-bold text-white uppercase tracking-wider mb-3 text-xs">Quick Links</h4>
          <ul class="space-y-2">
            <li><a href="#about" class="hover:text-brand-ochre transition">About Company</a></li>
            <li><a href="#services" class="hover:text-brand-ochre transition">Our Services</a></li>
            <li><a href="#portfolio" class="hover:text-brand-ochre transition">Track Record & Booths</a></li>
            <li><a href="#team" class="hover:text-brand-ochre transition">Leadership Team</a></li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-white uppercase tracking-wider mb-3 text-xs">Major Services</h4>
          <ul class="space-y-2">
            <li>Exhibition Stand Construction</li>
            <li>3D Setup Design & Visualization</li>
            <li>Large Format Digital Printing</li>
            <li>Event Furniture & Equipment Rentals</li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-white uppercase tracking-wider mb-3 text-xs">Location</h4>
          <p class="leading-relaxed">Bole, Atlas, Noah Centrum Apartment</p>
          <p class="mt-1">Ground Floor, Addis Ababa, Ethiopia</p>
          <p class="mt-2 text-brand-ochre font-semibold">+251 920 69 29 91 / +251 911 25 92 29</p>
        </div>

      </div>

      <div class="pt-6 border-t border-brand-lightGreen/40 flex flex-col sm:flex-row justify-between items-center text-[11px] text-gray-400">
        <p>&copy; 2026 The Workshop PLC. All rights reserved. Sister company to Ethel Events.</p>
        <div class="flex space-x-4 mt-2 sm:mt-0">
          <a href="#" class="hover:text-brand-ochre"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#" class="hover:text-brand-ochre"><i class="fa-brands fa-linkedin-in"></i></a>
          <a href="#" class="hover:text-brand-ochre"><i class="fa-brands fa-telegram"></i></a>
          <a href="#" class="hover:text-brand-ochre"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </footer>

  <!-- JAVASCRIPT FOR INTERACTION & SLIDER ANIMATION -->
  <script>
    // Mobile menu toggle
    const mobileMenuBtn = document.getElementById('mobileMenuBtn');
    const mobileMenu = document.getElementById('mobileMenu');

    mobileMenuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });

    // Landing Page Animated Image Slider
    const slides = document.querySelectorAll('.slide-item');
    const dots = document.querySelectorAll('#slideDots button');
    const prevBtn = document.getElementById('prevSlide');
    const nextBtn = document.getElementById('nextSlide');
    
    let currentSlide = 0;
    let slideInterval = null;

    function showSlide(index) {
      if (index >= slides.length) currentSlide = 0;
      else if (index < 0) currentSlide = slides.length - 1;
      else currentSlide = index;

      slides.forEach((slide, idx) => {
        if (idx === currentSlide) {
          slide.style.opacity = '1';
          slide.style.zIndex = '10';
        } else {
          slide.style.opacity = '0';
          slide.style.zIndex = '0';
        }
      });

      dots.forEach((dot, idx) => {
        if (idx === currentSlide) {
          dot.className = 'w-6 h-3 rounded-full bg-brand-ochre transition-all';
        } else {
          dot.className = 'w-3 h-3 rounded-full bg-white/50 hover:bg-white transition-all';
        }
      });
    }

    function nextSlide() {
      showSlide(currentSlide + 1);
    }

    function prevSlide() {
      showSlide(currentSlide - 1);
    }

    function startAutoSlide() {
      slideInterval = setInterval(nextSlide, 4500);
    }

    function resetAutoSlide() {
      clearInterval(slideInterval);
      startAutoSlide();
    }

    nextBtn.addEventListener('click', () => {
      nextSlide();
      resetAutoSlide();
    });

    prevBtn.addEventListener('click', () => {
      prevSlide();
      resetAutoSlide();
    });

    dots.forEach(dot => {
      dot.addEventListener('click', (e) => {
        const idx = parseInt(e.target.getAttribute('data-index'));
        showSlide(idx);
        resetAutoSlide();
      });
    });

    // Start automated slider
    startAutoSlide();

    // Cost Estimator Interactive Logic
    const calcType = document.getElementById('calcType');
    const calcArea = document.getElementById('calcArea');
    const areaVal = document.getElementById('areaVal');
    const addDesign = document.getElementById('addDesign');
    const addHR = document.getElementById('addHR');
    const addDismantle = document.getElementById('addDismantle');
    
    const rateEst = document.getElementById('rateEst');
    const daysEst = document.getElementById('daysEst');
    const totalEst = document.getElementById('totalEst');

    function updateEstimator() {
      const area = parseInt(calcArea.value);
      areaVal.textContent = area;

      let baseRate = 2200; // ETB per sq.m
      let days = "2 - 3 Days";

      if (calcType.value === 'booth') {
        baseRate = 2400;
        days = area > 50 ? "3 - 5 Days" : "2 - 3 Days";
      } else if (calcType.value === 'branding') {
        baseRate = 1400;
        days = "1 - 2 Days";
      } else if (calcType.value === 'rental') {
        baseRate = 1100;
        days = "1 Day";
      } else if (calcType.value === 'full') {
        baseRate = 3100;
        days = area > 50 ? "4 - 6 Days" : "2 - 4 Days";
      }

      let subtotal = area * baseRate;

      if (addDesign.checked) subtotal += 12000;
      if (addHR.checked) subtotal += 8000;
      if (addDismantle.checked) subtotal += 6000;

      const minEst = Math.round(subtotal * 0.9);
      const maxEst = Math.round(subtotal * 1.15);

      rateEst.textContent = `ETB ${baseRate.toLocaleString()} / sq.m`;
      daysEst.textContent = days;
      totalEst.textContent = `ETB ${minEst.toLocaleString()} - ${maxEst.toLocaleString()}`;
    }

    [calcType, calcArea, addDesign, addHR, addDismantle].forEach(elem => {
      elem.addEventListener('input', updateEstimator);
    });

    // Form Submit handling
    function handleFormSubmit(e) {
      e.preventDefault();
      const status = document.getElementById('formStatus');
      status.classList.remove('hidden');
      e.target.reset();
      setTimeout(() => {
        status.classList.add('hidden');
      }, 5000);
    }
  </script>
</body>
</html>
