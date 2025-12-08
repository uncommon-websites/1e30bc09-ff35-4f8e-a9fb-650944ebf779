<script lang="ts">
	// Icons
	import { ArrowRight, Plus, ChevronDown, Play } from 'lucide-svelte';

	// State for FAQ
	let openFaq: number | null = null;
	const toggleFaq = (index: number) => {
		openFaq = openFaq === index ? null : index;
	};

	const faqs = [
		{ q: "What can Memo do?", a: "Memo is designed to handle a variety of household tasks, from tidying up clutter to assisting in the kitchen. It learns from your habits to become more helpful over time." },
		{ q: "Is Memo available for purchase?", a: "We are currently in the beta phase. You can sign up for our newsletter to get the latest updates on availability." },
		{ q: "How much will a Memo cost?", a: "Pricing has not been announced yet. We aim to make Memo accessible to as many households as possible." },
		{ q: "Privacy & Safety: Does Memo record my home?", a: "Memo uses sensors to navigate, but privacy is our top priority. Data is processed locally whenever possible, and we adhere to strict privacy standards." },
		{ q: "Is Memo safe?", a: "Yes, Memo is built with multiple safety layers to ensure it operates safely around people and pets." },
		{ q: "What is the Sunday Beta program?", a: "The Beta program allows early adopters to test Memo in their homes and provide feedback to help us improve the product." }
	];

    // Placeholder images since we don't have the assets
    const heroImage = "https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?q=80&w=2670&auto=format&fit=crop"; 
    const kitchenImage = "https://images.unsplash.com/photo-1556910103-1c02745a30bf?q=80&w=2670&auto=format&fit=crop";
    const homeImage = "https://images.unsplash.com/photo-1484154218962-a1c002085d2f?q=80&w=2670&auto=format&fit=crop";
    const learningImage = "https://images.unsplash.com/photo-1516321497487-e288fb19713f?q=80&w=2670&auto=format&fit=crop";
    const gloveImage = "https://images.unsplash.com/photo-1555255707-c07966088b7b?q=80&w=2532&auto=format&fit=crop";
    const robotHead = "https://images.unsplash.com/photo-1485827404703-89b55fcc595e?q=80&w=2670&auto=format&fit=crop";
    const robotWheel = "https://images.unsplash.com/photo-1535378437323-9555f3e7f6aa?q=80&w=2670&auto=format&fit=crop";
    const robotArm = "https://images.unsplash.com/photo-1581092160562-40aa08e78837?q=80&w=2670&auto=format&fit=crop";
    const robotDetail = "https://images.unsplash.com/photo-1581092335397-9583eb92d232?q=80&w=2670&auto=format&fit=crop";

</script>

<!-- Header -->
<header class="fixed top-0 left-0 right-0 z-50 flex items-center justify-between px-6 py-4 bg-cream/90 backdrop-blur-sm">
	<div class="w-12">
		<button class="w-8 h-8 flex items-center justify-center bg-dark text-white rounded-full">
			<Plus size={20} />
		</button>
	</div>
	<div class="text-sm font-bold tracking-widest uppercase">Sunday</div>
	<div class="w-12 flex justify-end">
		<button class="text-xs font-medium border border-gray-300 rounded-full px-3 py-1 hover:bg-gray-100">EN</button>
	</div>
</header>

<main class="pt-24 pb-20">
	<!-- Hero Section -->
	<section class="container-custom mb-32">
		<div class="flex flex-col items-center text-center mb-12">
			<p class="text-xs text-gray-500 mb-4 max-w-xs">The future home robot<br>built for busy households</p>
			<h1 class="text-6xl md:text-8xl font-medium tracking-tight mb-8">Say hello to Memo</h1>
		</div>

		<div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-3xl overflow-hidden mb-12 bg-gray-200">
			<img src={heroImage} alt="Memo robot in kitchen" class="w-full h-full object-cover" />
		</div>

		<div class="max-w-3xl mx-auto text-center">
			<p class="text-xl md:text-2xl leading-relaxed font-light text-gray-800">
				Built for busy households, Memo works 24/7 to make your life lighter. Hand off your repetitive to-do's, so you can focus on what really matters.
			</p>
		</div>
	</section>

	<!-- Story / Video Section -->
	<section class="container-custom mb-40">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="max-w-sm">
				<p class="text-sm leading-relaxed text-gray-600">
					Robots should give you back what matters most — time. Watch how our team came together to work on this mission.
				</p>
			</div>
			<div class="relative aspect-video rounded-xl overflow-hidden bg-gray-800 group cursor-pointer">
				<img src={kitchenImage} alt="Video thumbnail" class="w-full h-full object-cover opacity-80 group-hover:opacity-60 transition-opacity" />
				<div class="absolute inset-0 flex items-center justify-center">
					<div class="w-12 h-12 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
						<Play size={20} fill="currentColor" />
					</div>
				</div>
				<div class="absolute bottom-4 left-4 text-white text-sm font-medium">01. Our story</div>
			</div>
		</div>
	</section>

	<!-- Typography Section -->
	<section class="container-custom mb-40">
		<div class="flex flex-col text-7xl md:text-9xl font-medium tracking-tighter leading-none mb-24">
			<span class="self-start">Mundane</span>
			<span class="self-center my-4 md:my-8">made</span>
			<span class="self-end">magic</span>
		</div>

		<div class="max-w-2xl mx-auto text-center">
			<p class="text-lg text-gray-600 leading-relaxed">
				Powered by state-of-the-art AI models and an ever-expanding Skill Library, Memo doesn't just know how to do a few tasks—Memo improves its skills faster than any robot that has come before it.
			</p>
		</div>
	</section>

	<!-- Feature 1: Kitchen -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={kitchenImage} alt="Memo in kitchen" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Memo works in the kitchen</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Lightening the load</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end">
				<p class="text-sm text-gray-600 leading-relaxed max-w-xs">
					Memo can quietly and autonomously start loads of plates and delicate glasses, throw out food scraps, and load up your dishwasher before running it. Just like a tidy new one of the crew, so you can go take care of the things only you can do.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden">
				<img src={robotArm} alt="Memo working" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Smart loads at night</div>
			</div>
		</div>
	</section>

	<!-- Feature 2: Homes -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={homeImage} alt="Memo in home" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Memo works in<br>homes it's never seen</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">A true home is different. Memo learns in yours.</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					We believe Memo should be easy to use in the real world, starting autonomously out of the box. Hundreds of people in unique homes show Memo real world scenarios each day, so Memo can robustly handle the chaos of real life.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1593349480506-8433634cdcbe?q=80&w=2670&auto=format&fit=crop" alt="Memo detail" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Adapting to new spaces</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1581092580497-e0d23cbdf1dc?q=80&w=2670&auto=format&fit=crop" alt="Memo detail" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Handling unexpected obstacles</div>
			</div>
		</div>
	</section>

	<!-- Feature 3: Learning -->
	<section class="container-custom mb-32">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={learningImage} alt="Memo learning" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Memo is always learning</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Teach old dogs new tricks.</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					In December 2023, Memo had only one arm and learned its first task: arranging shoes. Today, Memo is trained on multiple skills in parallel. In October 2024, Memo learned to fold piles of laundry, handle glassware, and put a shirt on a hanger.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1581092977092-28ebb64ebcc2?q=80&w=2670&auto=format&fit=crop" alt="Memo skill 1" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Memo picking up laundry</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src="https://images.unsplash.com/photo-1581092162384-8987c1d64718?q=80&w=2670&auto=format&fit=crop" alt="Memo skill 2" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Memo folding a shirt</div>
			</div>
		</div>
	</section>

	<!-- Technology Section (Sage Green) -->
	<section class="bg-sage py-32">
		<div class="container-custom">
			<div class="flex flex-col items-center text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight text-white mb-12 drop-shadow-sm">From imitation to intuition</h2>
				
				<div class="relative w-full max-w-4xl aspect-square md:aspect-[16/9] mb-12">
					<img src={gloveImage} alt="Skill Capture Glove" class="w-full h-full object-contain mix-blend-multiply" />
				</div>

				<div class="max-w-2xl mx-auto mb-12">
					<p class="text-xl text-gray-700 leading-relaxed">
						Our Skill Capture Glove™ enables Memo to distill millions of human movements into its onboard AI, unlocking helpful home skills. What the glove does, Memo learns.
					</p>
				</div>

				<div class="relative w-full max-w-3xl aspect-video rounded-2xl overflow-hidden mb-12 bg-gray-800">
					<img src={learningImage} alt="Video thumbnail" class="w-full h-full object-cover opacity-80" />
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="w-16 h-16 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
							<Play size={24} fill="currentColor" />
						</div>
					</div>
					<div class="absolute bottom-4 left-4 text-white text-xs font-medium">01. Skill Capture Glove in use</div>
				</div>

				<div class="text-center max-w-md mx-auto text-sm text-gray-600 mb-8">
					To date, we've logged over 2,000 hours in our Motion Vocabulary. This robust training is what makes Sunday Memo useful in yours.
				</div>

				<div class="flex gap-8 justify-center text-sm font-medium">
					<a href="#" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Explore Technology</a>
					<a href="#" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Become a Beta Pro</a>
				</div>
			</div>
		</div>
	</section>

	<!-- Design Section -->
	<section class="py-32 bg-cream">
		<div class="container-custom">
			<div class="text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight mb-12">Designed for real<br>use</h2>
				
				<div class="inline-flex bg-white rounded-full p-1 shadow-sm border border-gray-100">
					<button class="px-6 py-2 rounded-full bg-gray-100 text-sm font-medium">Features</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">360°</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Anatomy</button>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
				<!-- Card 1 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden group">
					<img src={robotHead} alt="Privacy" class="w-full h-full object-cover" />
					<div class="absolute inset-0 bg-black/40 p-8 flex flex-col justify-between opacity-0 group-hover:opacity-100 transition-opacity duration-300">
						<div class="text-white">
							<h3 class="font-bold mb-2">Your privacy is protected</h3>
							<p class="text-xs leading-relaxed opacity-90">Memo is an autonomous robot that operates locally. Even through its remote operation features, we ensure strict privacy protocols, keeping your data safe within your home.</p>
						</div>
					</div>
				</div>

				<!-- Card 2 -->
				<div class="bg-[#e8e4dc] rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Safety for the whole family</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						With a full suite of sensors, active avoidance, and a lightweight body, Memo is safe for small members of the family.
					</p>
				</div>

				<!-- Card 3 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden bg-orange-500">
					<img src={robotDetail} alt="Detail" class="w-full h-full object-cover mix-blend-multiply opacity-80" />
                    <div class="absolute bottom-8 right-8 w-12 h-12 bg-black rounded-full flex items-center justify-center text-white">
                        <Plus size={20} />
                    </div>
				</div>

                <!-- Card 4 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src={robotWheel} alt="Wheels" class="w-full h-full object-cover" />
                    <div class="absolute top-8 left-8 text-white max-w-[200px]">
                        <h3 class="font-bold text-sm mb-1">Traverse your home</h3>
                        <p class="text-[10px] opacity-80">Custom wheels allow Memo to navigate carpets and thresholds with ease.</p>
                    </div>
				</div>

                 <!-- Card 5 -->
				<div class="bg-[#dce3de] rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Simple, soft, and easy to clean</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						Memo's face is soft to the touch, wipes clean, withstands bumps, and can be wiped down with any household cleaning product.
					</p>
				</div>

                 <!-- Card 6 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src="https://images.unsplash.com/photo-1616046229478-9901c5536a45?q=80&w=2670&auto=format&fit=crop" alt="Touch" class="w-full h-full object-cover" />
				</div>
			</div>
            
            <div class="flex justify-center mt-12">
                 <div class="inline-flex bg-white rounded-full p-1 shadow-sm border border-gray-100">
					<button class="px-6 py-2 rounded-full bg-gray-100 text-sm font-medium">Features</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">360°</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Anatomy</button>
				</div>
            </div>
		</div>
	</section>

	<!-- Customization Section (Sky Blue) -->
	<section class="bg-sky py-32">
		<div class="container-custom flex flex-col items-center text-center">
			<div class="flex items-center justify-between w-full max-w-4xl mb-12">
				<span class="text-sm font-medium text-gray-500">Memo wears many hats.</span>
				<div class="w-32 h-32 md:w-48 md:h-48 text-black animate-spin-slow">
					<svg viewBox="0 0 100 100" fill="currentColor" class="w-full h-full">
						<path d="M50 0C58 0 65 7 65 15C65 23 58 30 50 30C42 30 35 23 35 15C35 7 42 0 50 0ZM85 15C93 15 100 22 100 30C100 38 93 45 85 45C77 45 70 38 70 30C70 22 77 15 85 15ZM85 55C93 55 100 62 100 70C100 78 93 85 85 85C77 85 70 78 70 70C70 62 77 55 85 55ZM50 70C58 70 65 77 65 85C65 93 58 100 50 100C42 100 35 93 35 85C35 77 42 70 50 70ZM15 55C23 55 30 62 30 70C30 78 23 85 15 85C7 85 0 78 0 70C0 62 7 55 15 55ZM15 15C23 15 30 22 30 30C30 38 23 45 15 45C7 45 0 38 0 30C0 22 7 15 15 15Z" />
					</svg>
				</div>
				<span class="text-sm font-medium text-gray-500">Which should it wear next?</span>
			</div>
			
			<button class="bg-black text-white px-8 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
				Cast your choice
			</button>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-32 container-custom">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
			<div>
				<h2 class="text-sm font-medium text-gray-500 uppercase tracking-wide">Frequently asked questions</h2>
			</div>
			<div class="md:col-span-2">
				<div class="space-y-4">
					{#each faqs as faq, i}
						<div class="border-b border-gray-200 pb-4">
							<button 
								class="w-full flex items-center justify-between text-left py-4 focus:outline-none group"
								onclick={() => toggleFaq(i)}
							>
								<span class="text-lg font-medium group-hover:text-gray-600 transition-colors">{faq.q}</span>
								<ChevronDown class="transition-transform duration-300 {openFaq === i ? 'rotate-180' : ''}" />
							</button>
							{#if openFaq === i}
								<div class="pb-4 text-gray-600 leading-relaxed">
									{faq.a}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</section>
</main>

<!-- Footer -->
<footer class="bg-neon-yellow pt-20 pb-8 rounded-t-[3rem] mt-[-2rem] relative z-10">
	<div class="container-custom">
		<!-- Black CTA Box -->
		<div class="bg-dark text-white rounded-3xl p-12 md:p-24 text-center mb-20 relative overflow-hidden">
			<div class="relative z-10">
				<h2 class="text-2xl md:text-4xl font-medium mb-8">We are hiring. Join our Founding Team. <span class="text-gray-400">Create robots. Demand parts. Blueprint.</span></h2>
				<a href="#" class="inline-flex items-center border border-white/30 rounded-full px-6 py-2 hover:bg-white/10 transition-colors text-sm">
					Apply to join <ArrowRight size={16} class="ml-2" />
				</a>
			</div>
		</div>

		<!-- Footer Links -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-20 text-sm">
			<div class="col-span-2 md:col-span-1">
				<p class="mb-4">Get the latest news</p>
				<form class="flex border-b border-black pb-2">
					<input type="email" placeholder="Email address" class="bg-transparent border-none outline-none w-full placeholder-gray-600" />
					<button type="submit" class="font-medium">Subscribe</button>
				</form>
			</div>
			
			<div class="md:col-start-3">
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Explore</a></li>
					<li><a href="#" class="hover:underline">Technology</a></li>
					<li><a href="#" class="hover:underline">Mission</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Home</a></li>
					<li><a href="#" class="hover:underline">Features</a></li>
					<li><a href="#" class="hover:underline">Careers</a></li>
					<li><a href="#" class="hover:underline">Beta Program</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Press</a></li>
					<li><a href="#" class="hover:underline">Instagram</a></li>
					<li><a href="#" class="hover:underline">X (Twitter)</a></li>
					<li><a href="#" class="hover:underline">YouTube</a></li>
				</ul>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-wider text-gray-800 border-t border-black/10 pt-8">
			<div class="mb-4 md:mb-0">© 2024 Sunday Inc.</div>
			<div class="flex gap-8">
				<a href="#" class="hover:underline">Terms of Service</a>
				<a href="#" class="hover:underline">Privacy and Cookies</a>
			</div>
		</div>
        
        <div class="flex justify-center mt-16 mb-8">
            <div class="flex flex-col items-center gap-2">
                <div class="text-[10px] uppercase tracking-widest text-center max-w-xs leading-relaxed">
                    The future has arrived. Memo is watching out for right now.<br>
                    Mountain View, CA · New York City, NY
                </div>
                <div class="mt-8">
                    <div class="w-8 h-8 bg-black text-neon-yellow rounded-full flex items-center justify-center">
                        <Plus size={20} />
                    </div>
                </div>
                 <div class="mt-2">
                    <div class="w-8 h-8 bg-black text-neon-yellow rounded-full flex items-center justify-center">
                        <Plus size={20} />
                    </div>
                </div>
            </div>
        </div>
	</div>
</footer>

<style>
	/* Custom animations or utilities if needed */
	.animate-spin-slow {
		animation: spin 10s linear infinite;
	}
	@keyframes spin {
		from { transform: rotate(0deg); }
		to { transform: rotate(360deg); }
	}
</style>

