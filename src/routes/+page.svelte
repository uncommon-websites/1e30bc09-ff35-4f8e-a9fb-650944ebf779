<script lang="ts">
	// Icons
	import { ArrowRight, Bell, ChevronDown, Zap, Trophy, Users, DollarSign } from 'lucide-svelte';

	// State for FAQ
	let openFaq: number | null = null;
	const toggleFaq = (index: number) => {
		openFaq = openFaq === index ? null : index;
	};

	const faqs = [
		{ q: "Which sports leagues does Hatewatch support?", a: "We currently support NFL, MLB, NHL, and NBA. We monitor all games in real-time across these major leagues, ensuring you never miss a rival failure moment." },
		{ q: "How fast are the notifications?", a: "Our notifications are instant. We use real-time sports data feeds to detect rival team failures the moment they happen, so you get the schadenfreude while it's still fresh." },
		{ q: "How much does Hatewatch cost?", a: "Your first rival team is completely free, forever. Each additional rival team is just $1/month. No hidden fees, cancel anytime." },
		{ q: "Can I track multiple rival teams?", a: "Absolutely! Track as many rivals as you want. Your first rival is free, and each additional rival is only $1/month. Perfect for fans with multiple nemeses." },
		{ q: "What counts as a 'rival failure'?", a: "We notify you when your rival team loses a game, gets eliminated from playoffs, suffers a major injury to a star player, or experiences other significant setbacks. You control which types of notifications you receive." },
		{ q: "Will I get spammed with notifications?", a: "No. You have full control over notification settings. Choose to get alerts only for losses, playoff eliminations, or all rival failures. Customize it to your preference." }
	];

    // Generated images
    const heroImage = "/generated/image-sports-fans-celebrating-and-cheering-int-1765512390173-0.webp"; 
    const phoneImage = "/generated/image-close-up-of-a-smartphone-showing-sports--1765512393009-1.webp";
    const fanImage = "/generated/image-die-hard-sports-fan-watching-game-on-tv--1765512395976-2.webp";
    const celebrateImage = "/generated/image-group-of-friends-celebrating-a-sports-mo-1765512398306-3.webp";
    const scoreboardImage = "/generated/image-sports-stadium-scoreboard-showing-game-r-1765512400693-4.webp";
    const disappointedImage = "/generated/image-person-looking-disappointed-or-frustrate-1765512403145-5.webp";

</script>

<!-- Header -->
<header class="fixed top-0 left-0 right-0 z-50 flex items-center justify-between px-6 py-4 bg-white/90 backdrop-blur-sm border-b border-gray-100">
	<div class="flex items-center gap-2">
		<div class="w-8 h-8 text-primary-600">
			<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path
					fill-rule="evenodd"
					clip-rule="evenodd"
					d="M9.61185 4.17065C8.2158 4.17065 6.92581 4.91543 6.22779 6.12444L3.72109 10.4662C3.02307 11.6752 3.02307 13.1647 3.72109 14.3737L6.22779 18.7155C6.92581 19.9245 8.2158 20.6693 9.61185 20.6693H14.6252C16.0213 20.6693 17.3113 19.9245 18.0093 18.7155L20.516 14.3737C21.214 13.1647 21.214 11.6752 20.516 10.4662L18.0093 6.12444C17.3113 4.91543 16.0213 4.17065 14.6252 4.17065H9.61185ZM14.6252 6.77569H11.4919C10.9905 6.77569 10.6773 7.31837 10.9283 7.75232C11.7029 9.09123 12.4793 10.4291 13.2527 11.7687C13.4854 12.1717 13.4854 12.6682 13.2527 13.0712C12.4793 14.4108 11.7029 15.7487 10.9283 17.0876C10.6773 17.5215 10.9905 18.0642 11.4919 18.0642H14.6252C15.0906 18.0642 15.5206 17.8159 15.7533 17.4129L18.26 13.0712C18.4927 12.6682 18.4927 12.1717 18.26 11.7687L15.7533 7.42695C15.5206 7.02395 15.0906 6.77569 14.6252 6.77569Z"
					fill="currentColor"
				/>
			</svg>
		</div>
		<div class="text-xl font-bold tracking-tight">Hatewatch</div>
	</div>
	<nav class="hidden md:flex items-center gap-6 text-sm">
		<a href="#features" class="hover:text-primary-600 transition-colors">Features</a>
		<a href="#pricing" class="hover:text-primary-600 transition-colors">Pricing</a>
		<a href="#faq" class="hover:text-primary-600 transition-colors">FAQ</a>
	</nav>
	<div class="flex items-center gap-3">
		<button class="text-sm font-medium hover:text-primary-600 transition-colors">Sign In</button>
		<button class="bg-primary-600 text-white px-4 py-2 rounded-lg text-sm font-medium hover:bg-primary-700 transition-colors">Get Started</button>
	</div>
</header>

<main class="pt-24 pb-20">
	<!-- Hero Section -->
	<section class="container-custom mb-32">
		<div class="flex flex-col items-center text-center mb-12">
			<div class="inline-flex items-center gap-2 bg-primary-50 text-primary-700 px-4 py-2 rounded-full text-sm font-medium mb-6">
				<Bell size={16} />
				<span>Instant rival failure notifications</span>
			</div>
			<h1 class="text-5xl md:text-7xl lg:text-8xl font-bold tracking-tight mb-6 max-w-5xl">
				Never miss your rival's<br/><span class="text-primary-600">epic failure</span> again
			</h1>
			<p class="text-lg md:text-xl text-gray-600 mb-8 max-w-2xl">
				Real-time notifications when your rival teams lose, choke, or crash out. Because watching them fail is almost as good as your team winning.
			</p>
			<div class="flex flex-col sm:flex-row gap-4 items-center">
				<button class="bg-primary-600 text-white px-8 py-4 rounded-lg text-base font-semibold hover:bg-primary-700 transition-colors shadow-lg shadow-primary-200">
					Start Watching Free
				</button>
				<button class="border border-gray-300 px-8 py-4 rounded-lg text-base font-semibold hover:bg-gray-50 transition-colors">
					See How It Works
				</button>
			</div>
			<p class="text-sm text-gray-500 mt-4">First rival team free forever • $1/month per additional rival</p>
		</div>

		<div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-2xl overflow-hidden mb-12 bg-gray-100 shadow-2xl">
			<img src={heroImage} alt="Sports fans celebrating" class="w-full h-full object-cover" />
			<div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent"></div>
		</div>

		<div class="max-w-3xl mx-auto text-center">
			<p class="text-xl md:text-2xl leading-relaxed text-gray-700">
				185M US sports fans miss crucial rival failures checking scores manually. Hatewatch delivers instant schadenfreude notifications across NFL, MLB, NHL, and NBA.
			</p>
		</div>
	</section>

	<!-- Problem Section -->
	<section class="container-custom mb-40">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="relative aspect-square md:aspect-[4/3] rounded-2xl overflow-hidden bg-gray-100">
				<img src={disappointedImage} alt="Missing the moment" class="w-full h-full object-cover" />
				<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
				<div class="absolute bottom-6 left-6 text-white">
					<p class="text-sm font-medium mb-1">The Problem</p>
					<p class="text-xs opacity-90">Missing the sweet moment of rival failure</p>
				</div>
			</div>
			<div class="max-w-lg">
				<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-6">
					You're missing the<br/>best moments
				</h2>
				<p class="text-lg leading-relaxed text-gray-600 mb-6">
					Die-hard sports fans spend hours checking scores manually, yet still miss the exact moment their rival team chokes in the playoffs or loses to a basement dweller.
				</p>
				<p class="text-lg leading-relaxed text-gray-600">
					That schadenfreude hit is fleeting. By the time you check the score, the moment has passed. Hatewatch ensures you never miss it again.
				</p>
			</div>
		</div>
	</section>

	<!-- Typography Section -->
	<section class="container-custom mb-40">
		<div class="flex flex-col text-6xl md:text-8xl lg:text-9xl font-bold tracking-tighter leading-none mb-24">
			<span class="self-start text-gray-900">Instant</span>
			<span class="self-center my-4 md:my-8 text-primary-600">schadenfreude</span>
			<span class="self-end text-gray-900">delivered</span>
		</div>

		<div class="max-w-2xl mx-auto text-center">
			<p class="text-lg text-gray-600 leading-relaxed">
				Powered by real-time sports data monitoring across NFL, MLB, NHL, and NBA. The moment your rival fails, you know. No delays. No checking scores. Just pure, instant satisfaction.
			</p>
		</div>
	</section>

	<!-- Feature 1: Real-Time Notifications -->
	<section id="features" class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-2xl overflow-hidden mb-4 group">
			<img src={phoneImage} alt="Instant notifications" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center bg-black/40">
				<h2 class="text-4xl md:text-6xl text-white font-bold text-center px-4 drop-shadow-lg">Lightning-fast alerts</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/90 text-sm font-medium">Real-time monitoring</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
			<div class="bg-gray-50 rounded-2xl p-8 flex items-end border border-gray-100">
				<div>
					<div class="flex items-center gap-2 text-primary-600 mb-3">
						<Zap size={20} />
						<span class="text-sm font-semibold">Instant Delivery</span>
					</div>
					<p class="text-sm text-gray-700 leading-relaxed">
						Our real-time sports data feeds detect rival failures the moment they happen. Get push notifications within seconds of the final buzzer, the crushing interception, or the playoff elimination. No refresh needed.
					</p>
				</div>
			</div>
			<div class="relative aspect-[4/3] rounded-2xl overflow-hidden">
				<img src={scoreboardImage} alt="Live scoreboard" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/40 px-3 py-1.5 rounded-lg backdrop-blur-sm">Live data across 4 major leagues</div>
			</div>
		</div>
	</section>

	<!-- Feature 2: Multi-Sport Coverage -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-2xl overflow-hidden mb-4 group">
			<img src={celebrateImage} alt="Celebrating fans" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center bg-black/40">
				<h2 class="text-4xl md:text-6xl text-white font-bold text-center px-4 drop-shadow-lg">All your rivals,<br/>all in one place</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/90 text-sm font-medium">NFL • MLB • NHL • NBA</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-50 rounded-2xl p-8 flex items-end md:col-span-1 border border-gray-100">
				<div>
					<div class="flex items-center gap-2 text-primary-600 mb-3">
						<Trophy size={20} />
						<span class="text-sm font-semibold">4 Major Leagues</span>
					</div>
					<p class="text-sm text-gray-700 leading-relaxed">
						Track rivals across NFL, MLB, NHL, and NBA. Whether it's football season or basketball playoffs, never miss a rival failure moment. One app for all your sports hatred.
					</p>
				</div>
			</div>
			<div class="bg-primary-950 text-white rounded-2xl p-8 flex flex-col justify-center md:col-span-1">
				<div class="text-5xl font-bold mb-2">185M</div>
				<p class="text-sm opacity-90">US sports fans who could benefit from instant rival failure alerts</p>
			</div>
			<div class="bg-gray-50 rounded-2xl p-8 flex flex-col justify-center md:col-span-1 border border-gray-100">
				<div class="text-5xl font-bold text-primary-600 mb-2">500K</div>
				<p class="text-sm text-gray-700">Target users in our first year across all major sports rivalries</p>
			</div>
		</div>
	</section>

	<!-- Feature 3: Customization -->
	<section class="container-custom mb-32">
		<div class="relative w-full aspect-[16/9] rounded-2xl overflow-hidden mb-4 group">
			<img src={fanImage} alt="Die-hard fan" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center bg-black/40">
				<h2 class="text-4xl md:text-6xl text-white font-bold text-center px-4 drop-shadow-lg">Your hatred,<br/>your rules</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/90 text-sm font-medium">Fully customizable alerts</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-50 rounded-2xl p-8 flex items-end md:col-span-1 border border-gray-100">
				<div>
					<div class="flex items-center gap-2 text-primary-600 mb-3">
						<Users size={20} />
						<span class="text-sm font-semibold">Your Way</span>
					</div>
					<p class="text-sm text-gray-700 leading-relaxed">
						Choose which types of failures matter to you. Get alerts for every loss, just playoff eliminations, or everything in between. Control notification timing, frequency, and style.
					</p>
				</div>
			</div>
			<div class="bg-primary-600 text-white rounded-2xl p-8 flex flex-col justify-between md:col-span-1">
				<div>
					<div class="text-sm font-semibold mb-3 opacity-90">Notification Types</div>
					<ul class="space-y-2 text-sm">
						<li class="flex items-center gap-2">
							<div class="w-1.5 h-1.5 bg-white rounded-full"></div>
							<span>Game losses</span>
						</li>
						<li class="flex items-center gap-2">
							<div class="w-1.5 h-1.5 bg-white rounded-full"></div>
							<span>Playoff eliminations</span>
						</li>
						<li class="flex items-center gap-2">
							<div class="w-1.5 h-1.5 bg-white rounded-full"></div>
							<span>Embarrassing defeats</span>
						</li>
						<li class="flex items-center gap-2">
							<div class="w-1.5 h-1.5 bg-white rounded-full"></div>
							<span>Star player injuries</span>
						</li>
					</ul>
				</div>
			</div>
			<div class="bg-gray-50 rounded-2xl p-8 flex flex-col justify-center md:col-span-1 border border-gray-100">
				<div class="text-4xl font-bold text-primary-600 mb-2">∞</div>
				<p class="text-sm text-gray-700">Track unlimited rivals. First one free, $1/month for each additional team.</p>
			</div>
		</div>
	</section>

	<!-- Pricing Section -->
	<section id="pricing" class="bg-gray-950 text-white py-32">
		<div class="container-custom">
			<div class="flex flex-col items-center text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-bold tracking-tight mb-6">Simple, honest pricing</h2>
				<p class="text-xl text-gray-400 mb-12 max-w-2xl">
					Start free. Scale as your hatred grows. No hidden fees, no contracts.
				</p>

				<div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full max-w-4xl">
					<!-- Free Plan -->
					<div class="bg-gray-900 rounded-2xl p-8 border border-gray-800">
						<div class="text-left">
							<div class="text-sm font-semibold text-primary-400 mb-2">FREE FOREVER</div>
							<div class="text-5xl font-bold mb-2">$0</div>
							<div class="text-gray-400 text-sm mb-6">First rival team</div>
							
							<ul class="space-y-3 mb-8">
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-primary-600/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-primary-600"></div>
									</div>
									<span class="text-sm text-gray-300">Track one rival team forever</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-primary-600/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-primary-600"></div>
									</div>
									<span class="text-sm text-gray-300">Real-time loss notifications</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-primary-600/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-primary-600"></div>
									</div>
									<span class="text-sm text-gray-300">All 4 major leagues</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-primary-600/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-primary-600"></div>
									</div>
									<span class="text-sm text-gray-300">Custom notification settings</span>
								</li>
							</ul>

							<button class="w-full bg-gray-800 text-white px-6 py-3 rounded-lg font-semibold hover:bg-gray-700 transition-colors">
								Start Free
							</button>
						</div>
					</div>

					<!-- Paid Plan -->
					<div class="bg-primary-600 rounded-2xl p-8 relative overflow-hidden">
						<div class="absolute top-4 right-4 bg-white/20 backdrop-blur-sm px-3 py-1 rounded-full text-xs font-semibold">
							MOST POPULAR
						</div>
						<div class="text-left relative z-10">
							<div class="text-sm font-semibold text-primary-100 mb-2">PAY AS YOU HATE</div>
							<div class="text-5xl font-bold mb-2">$1</div>
							<div class="text-primary-100 text-sm mb-6">per additional rival/month</div>
							
							<ul class="space-y-3 mb-8">
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-white/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-white"></div>
									</div>
									<span class="text-sm text-white">Everything in Free</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-white/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-white"></div>
									</div>
									<span class="text-sm text-white">Track unlimited rival teams</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-white/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-white"></div>
									</div>
									<span class="text-sm text-white">Priority notifications</span>
								</li>
								<li class="flex items-start gap-3">
									<div class="w-5 h-5 rounded-full bg-white/20 flex items-center justify-center flex-shrink-0 mt-0.5">
										<div class="w-2 h-2 rounded-full bg-white"></div>
									</div>
									<span class="text-sm text-white">Advanced failure analytics</span>
								</li>
							</ul>

							<button class="w-full bg-white text-primary-600 px-6 py-3 rounded-lg font-semibold hover:bg-gray-100 transition-colors">
								Get Started
							</button>
						</div>
					</div>
				</div>

				<div class="text-center max-w-2xl mx-auto text-sm text-gray-400 mt-12">
					<p class="mb-4">Cancel anytime. No contracts. No BS. Just instant rival failure notifications.</p>
					<div class="flex items-center justify-center gap-2 text-primary-400">
						<DollarSign size={16} />
						<span>Example: Track 5 rival teams = Free + $4/month</span>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- How It Works Section -->
	<section class="py-32 bg-white">
		<div class="container-custom">
			<div class="text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-bold tracking-tight mb-6">How it works</h2>
				<p class="text-xl text-gray-600 max-w-2xl mx-auto">
					Three simple steps to never miss a rival failure again
				</p>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
				<!-- Step 1 -->
				<div class="relative">
					<div class="absolute -top-4 -left-4 w-12 h-12 bg-primary-600 text-white rounded-full flex items-center justify-center text-xl font-bold">
						1
					</div>
					<div class="bg-gray-50 rounded-2xl p-8 pt-12 border border-gray-100 h-full">
						<div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-lg flex items-center justify-center mb-4">
							<Users size={24} />
						</div>
						<h3 class="font-bold text-xl mb-3">Pick your rivals</h3>
						<p class="text-sm text-gray-600 leading-relaxed">
							Select the teams you love to hate. Choose from NFL, MLB, NHL, and NBA. Your first rival is free forever.
						</p>
					</div>
				</div>

				<!-- Step 2 -->
				<div class="relative">
					<div class="absolute -top-4 -left-4 w-12 h-12 bg-primary-600 text-white rounded-full flex items-center justify-center text-xl font-bold">
						2
					</div>
					<div class="bg-gray-50 rounded-2xl p-8 pt-12 border border-gray-100 h-full">
						<div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-lg flex items-center justify-center mb-4">
							<Bell size={24} />
						</div>
						<h3 class="font-bold text-xl mb-3">Customize alerts</h3>
						<p class="text-sm text-gray-600 leading-relaxed">
							Choose what failures matter to you. Get notified for every loss, just playoffs, or everything in between.
						</p>
					</div>
				</div>

				<!-- Step 3 -->
				<div class="relative">
					<div class="absolute -top-4 -left-4 w-12 h-12 bg-primary-600 text-white rounded-full flex items-center justify-center text-xl font-bold">
						3
					</div>
					<div class="bg-gray-50 rounded-2xl p-8 pt-12 border border-gray-100 h-full">
						<div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-lg flex items-center justify-center mb-4">
							<Zap size={24} />
						</div>
						<h3 class="font-bold text-xl mb-3">Enjoy the moment</h3>
						<p class="text-sm text-gray-600 leading-relaxed">
							Get instant notifications when your rivals fail. No checking scores. No missing moments. Pure schadenfreude, delivered.
						</p>
					</div>
				</div>
			</div>

			<div class="text-center mt-12">
				<button class="bg-primary-600 text-white px-8 py-4 rounded-lg text-base font-semibold hover:bg-primary-700 transition-colors shadow-lg shadow-primary-200">
					Start Watching Free
				</button>
			</div>
		</div>
	</section>

	<!-- FAQ Section -->
	<section id="faq" class="py-32 container-custom bg-gray-50">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12 max-w-6xl mx-auto">
			<div>
				<h2 class="text-sm font-bold text-primary-600 uppercase tracking-wide mb-2">FAQ</h2>
				<p class="text-3xl md:text-4xl font-bold">Common questions</p>
			</div>
			<div class="md:col-span-2">
				<div class="space-y-4">
					{#each faqs as faq, i}
						<div class="border-b border-gray-200 pb-4">
							<button 
								class="w-full flex items-center justify-between text-left py-4 focus:outline-none group"
								onclick={() => toggleFaq(i)}
							>
								<span class="text-lg font-semibold group-hover:text-primary-600 transition-colors">{faq.q}</span>
								<ChevronDown class="transition-transform duration-300 flex-shrink-0 ml-4 {openFaq === i ? 'rotate-180' : ''}" />
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
<footer class="bg-gray-950 text-white pt-20 pb-8">
	<div class="container-custom">
		<!-- CTA Box -->
		<div class="bg-primary-600 text-white rounded-2xl p-12 md:p-16 text-center mb-20 relative overflow-hidden">
			<div class="relative z-10">
				<h2 class="text-3xl md:text-5xl font-bold mb-4">Ready to celebrate rival failures?</h2>
				<p class="text-lg md:text-xl mb-8 text-primary-100 max-w-2xl mx-auto">
					Join thousands of sports fans who never miss a rival team's epic collapse.
				</p>
				<div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
					<button class="bg-white text-primary-600 px-8 py-4 rounded-lg text-base font-semibold hover:bg-gray-100 transition-colors">
						Start Free Trial
					</button>
					<button class="border border-white/30 text-white px-8 py-4 rounded-lg text-base font-semibold hover:bg-white/10 transition-colors">
						View Pricing
					</button>
				</div>
				<p class="text-sm text-primary-100 mt-4">First rival free forever • No credit card required</p>
			</div>
		</div>

		<!-- Footer Links -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-16 text-sm">
			<div class="col-span-2 md:col-span-1">
				<div class="flex items-center gap-2 mb-4">
					<div class="w-8 h-8 text-primary-600">
						<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
							<path
								fill-rule="evenodd"
								clip-rule="evenodd"
								d="M9.61185 4.17065C8.2158 4.17065 6.92581 4.91543 6.22779 6.12444L3.72109 10.4662C3.02307 11.6752 3.02307 13.1647 3.72109 14.3737L6.22779 18.7155C6.92581 19.9245 8.2158 20.6693 9.61185 20.6693H14.6252C16.0213 20.6693 17.3113 19.9245 18.0093 18.7155L20.516 14.3737C21.214 13.1647 21.214 11.6752 20.516 10.4662L18.0093 6.12444C17.3113 4.91543 16.0213 4.17065 14.6252 4.17065H9.61185ZM14.6252 6.77569H11.4919C10.9905 6.77569 10.6773 7.31837 10.9283 7.75232C11.7029 9.09123 12.4793 10.4291 13.2527 11.7687C13.4854 12.1717 13.4854 12.6682 13.2527 13.0712C12.4793 14.4108 11.7029 15.7487 10.9283 17.0876C10.6773 17.5215 10.9905 18.0642 11.4919 18.0642H14.6252C15.0906 18.0642 15.5206 17.8159 15.7533 17.4129L18.26 13.0712C18.4927 12.6682 18.4927 12.1717 18.26 11.7687L15.7533 7.42695C15.5206 7.02395 15.0906 6.77569 14.6252 6.77569Z"
								fill="currentColor"
							/>
						</svg>
					</div>
					<span class="text-xl font-bold">Hatewatch</span>
				</div>
				<p class="text-gray-400 text-sm mb-4">Never miss your rival's epic failure again.</p>
				<form class="flex border-b border-gray-700 pb-2">
					<input type="email" placeholder="Email address" class="bg-transparent border-none outline-none w-full placeholder-gray-500 text-sm" />
					<button type="submit" class="font-medium text-primary-400 text-sm">Subscribe</button>
				</form>
			</div>
			
			<div>
				<h3 class="font-semibold mb-3 text-white">Product</h3>
				<ul class="space-y-2 text-gray-400">
					<li><a href="#features" class="hover:text-white transition-colors">Features</a></li>
					<li><a href="#pricing" class="hover:text-white transition-colors">Pricing</a></li>
					<li><a href="#faq" class="hover:text-white transition-colors">FAQ</a></li>
					<li><a href="#" class="hover:text-white transition-colors">How It Works</a></li>
				</ul>
			</div>

			<div>
				<h3 class="font-semibold mb-3 text-white">Company</h3>
				<ul class="space-y-2 text-gray-400">
					<li><a href="#" class="hover:text-white transition-colors">About</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Blog</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Careers</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Press</a></li>
				</ul>
			</div>

			<div>
				<h3 class="font-semibold mb-3 text-white">Social</h3>
				<ul class="space-y-2 text-gray-400">
					<li><a href="#" class="hover:text-white transition-colors">Twitter</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Reddit</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Discord</a></li>
					<li><a href="#" class="hover:text-white transition-colors">Instagram</a></li>
				</ul>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="flex flex-col md:flex-row justify-between items-center text-xs text-gray-400 border-t border-gray-800 pt-8">
			<div class="mb-4 md:mb-0">© 2024 Hatewatch. All rights reserved.</div>
			<div class="flex gap-6">
				<a href="#" class="hover:text-white transition-colors">Terms of Service</a>
				<a href="#" class="hover:text-white transition-colors">Privacy Policy</a>
				<a href="#" class="hover:text-white transition-colors">Cookie Policy</a>
			</div>
		</div>
	</div>
</footer>
