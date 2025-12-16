<script lang="ts">
  export let title: string = "Tech Force";
</script>

<header class="fixed top-0 left-0 w-full z-50 mix-blend-difference text-white py-6 px-6 md:px-12 flex justify-between items-center bg-transparent">
  <div class="flex items-center gap-3">
    <!-- Logo Icon -->
    <div class="w-5 h-5 flex flex-col justify-between">
        <div class="flex gap-0.5 h-1.5">
            <div class="w-1.5 bg-white"></div>
            <div class="w-1.5 bg-white"></div>
            <div class="w-1.5 bg-white"></div>
        </div>
        <div class="flex gap-0.5 h-1.5">
            <div class="w-1.5 bg-white"></div>
            <div class="w-full bg-white"></div>
        </div>
    </div>
    <span class="font-medium text-lg tracking-tight">{title}</span>
  </div>
  <a href="#" class="text-[10px] uppercase tracking-[0.2em] font-bold hover:underline">Apply Now</a>
</header>