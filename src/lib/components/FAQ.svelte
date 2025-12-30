<script lang="ts">
    let openIndex: number | null = 0;

    const faqs = [
        { q: "What makes Atheon Labs different from existing defense software providers?", a: "We take a minimalist approach to mission-critical software. While competitors add layers of complexity, we strip it away. Our platform is built for extreme environments where reliability isn't optional—it's essential. Every feature is designed for high-stakes operational decisions." },
        { q: "What types of defense programs does Atheon Labs support?", a: "We focus on high-priority defense programs where operational decisions have immediate consequences. Our platform supports command and control systems, intelligence operations, and mission planning across multiple domains. We specialize in environments where legacy systems have historically failed." },
        { q: "How does Atheon Labs ensure software reliability in extreme environments?", a: "Reliability is built into our architecture from day one. We use redundant systems, rigorous testing protocols, and minimalist design principles to eliminate points of failure. Our software is engineered to operate in contested environments with limited connectivity, extreme weather, and high-stress operational conditions." },
        { q: "What is your deployment model?", a: "We offer flexible deployment options including on-premise, air-gapped, and cloud-hybrid solutions. Our platform can operate in fully disconnected environments and synchronize when connectivity is restored. Security and operational requirements drive our deployment architecture." },
        { q: "How does Atheon Labs handle security and compliance?", a: "Security is fundamental to everything we build. We maintain compliance with DoD security standards, including FedRAMP, CMMC, and IL5/IL6 requirements. Our platform undergoes continuous security auditing and penetration testing. We design for zero-trust architectures by default." },
        { q: "What is the typical contract structure?", a: "We start with pilot programs on high-priority missions, typically 6-12 months. Once we prove operational value and become mission-critical, we transition to multi-year contracts. Our goal is to become so essential to operations that renewal is automatic." },
        { q: "How quickly can Atheon Labs deploy to a new program?", a: "Our minimalist architecture enables rapid deployment. Initial pilot programs can be operational within weeks, not months. We prioritize speed to value—getting capabilities into operators' hands quickly while maintaining our reliability standards." },
        { q: "Does Atheon Labs integrate with existing legacy systems?", a: "Yes, but we're selective about integration points. We can interface with legacy systems where necessary, but our philosophy is to replace fragile infrastructure rather than build on top of it. We focus on clean data pipelines and modern APIs." },
        { q: "What kind of training and support does Atheon Labs provide?", a: "We provide comprehensive operator training and 24/7 mission support. Our platform is designed to be intuitive—minimizing training overhead. For mission-critical deployments, we embed technical specialists to ensure operational success." },
        { q: "How does pricing work?", a: "Our pricing is based on mission scope and operational scale. We structure contracts to align with program budgets and multi-year funding cycles. Initial pilots are designed to demonstrate ROI quickly, justifying expanded deployment and long-term commitment." },
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