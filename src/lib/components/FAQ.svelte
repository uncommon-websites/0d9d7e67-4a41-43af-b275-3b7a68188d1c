<script lang="ts">
    let openIndex: number | null = 0;

    const faqs = [
        { q: "What is the US Tech Force (Tech Force)?", a: "Tech Force will be an elite group of ~1,000 technology specialists hired by agencies to accelerate artificial intelligence (AI) implementation and solve the federal government's most critical technological challenges. Tech Force will primarily recruit early-career technologists from traditional recruiting channels, along with experienced engineering managers from private sector partners, to serve two-year employment terms in the federal government. Tech Force will include centralized organization and programming and serve as a recruiting platform post-employment." },
        { q: "What are the key steps in the recruiting process?", a: "Details about the recruiting process..." },
        { q: "What skills are required?", a: "Details about required skills..." },
        { q: "Are specific educational credentials required to participate?", a: "Details about credentials..." },
        { q: "Is there a minimum experience level required to apply?", a: "Details about experience..." },
        { q: "Is this a political appointment?", a: "Details about political appointment..." },
        { q: "When am I expected to start?", a: "Details about start date..." },
        { q: "Where will the employment be located?", a: "Details about location..." },
        { q: "What is the expected compensation for participants?", a: "Details about compensation..." },
        { q: "What projects will participants work on?", a: "Details about projects..." },
        { q: "What agencies will participate in Tech Force?", a: "Details about agencies..." },
        { q: "What companies are participating in Tech Force?", a: "Details about companies..." },
        { q: "How do private sector companies partner with Tech Force?", a: "Details about partnerships..." },
        { q: "Are there any other benefits?", a: "Details about benefits..." },
        { q: "What is the duration of the program?", a: "Details about duration..." },
        { q: "What happens after the employment is completed?", a: "Details about post-employment..." },
        { q: "What is the duration of Tech Force as a whole?", a: "Details about program duration..." },
        { q: "Will the program have a political mission?", a: "Details about mission..." },
        { q: "How do candidates nominated by a private sector company participate? Do they retain their private sector employment?", a: "Details about nomination..." },
        { q: "Will participants nominated by private sector companies be able to retain their deferred compensation packages (RSUs, options, etc.)?", a: "Details about compensation packages..." },
        { q: "How is Tech Force related to other government technology programs, including ones at GSA or the United States DOGE Service?", a: "Details about relations..." },
    ];

    function toggle(index: number) {
        openIndex = openIndex === index ? null : index;
    }
</script>

<section class="bg-[#0a0a0a] text-white px-6 md:px-12 py-24">
    <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-medium mb-12">Frequently Asked Questions</h2>
        
        <div class="border-t border-white/20">
            {#each faqs as faq, i}
                <div class="border-b border-white/20">
                    <button 
                        class="w-full py-6 flex justify-between items-center text-left hover:text-gray-300 transition-colors"
                        onclick={() => toggle(i)}
                        aria-expanded={openIndex === i}
                    >
                        <span class="text-lg font-light pr-8">{faq.q}</span>
                        <span class="text-xl font-light">{openIndex === i ? '×' : '+'}</span>
                    </button>
                    {#if openIndex === i}
                        <div class="pb-6 text-gray-400 font-light leading-relaxed max-w-4xl">
                            {faq.a}
                        </div>
                    {/if}
                </div>
            {/each}
        </div>
    </div>
</section>