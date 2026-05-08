<template>
  <section id="order" class="section-pad relative overflow-hidden" style="background: #F8F9FA;">
    <div style="position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,transparent,#C9A84C,transparent);"></div>

    <div class="max-w-2xl mx-auto px-4 sm:px-6 relative z-10">
      <div class="text-center mb-12 form-header gsap-fade-up">
        <span class="section-tag">📦 اطلب الآن</span>
        <h2 class="section-title mt-3 mb-3">تواصل معنا للطلب</h2>
        <div class="gold-divider"></div>
        <p class="section-subtitle mx-auto mt-5">اطلب الآن والتوصيل لحد بابك خلال 48 ساعة</p>

        <div class="mt-8 flex flex-col sm:flex-row gap-4 justify-center items-center">
          <a href="https://wa.me/201070503748?text=مرحباً،%20أريد%20الطلب%20من%20سينا%20جولد"
            target="_blank" rel="noopener" class="btn-wa w-full sm:w-auto px-8 py-4 text-lg">
            <svg class="w-6 h-6 flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12.031 6.172c-3.181 0-5.767 2.586-5.768 5.766-.001 1.298.38 2.27 1.019 3.287l-.582 2.128 2.182-.573c.978.58 1.911.928 3.145.929 3.178 0 5.767-2.587 5.768-5.766.001-3.187-2.575-5.77-5.764-5.771zm3.392 8.244c-.144.405-.837.774-1.17.824-.299.045-.677.063-1.092-.125-.339-.153-.889-.356-1.785-.886-1.139-.672-1.89-1.802-1.947-1.879-.057-.077-.464-.618-.464-1.178 0-.56.289-.838.391-.947.102-.109.222-.136.297-.136l.214.004c.068.004.156-.027.244.184l.328.792c.027.054.045.118.012.191-.034.073-.051.118-.102.219-.051.101-.107.219-.153.272-.051.063-.105.129-.044.234.061.105.274.453.586.733.404.362.748.475.857.531.109.056.173.045.237-.027.064-.073.277-.323.352-.434.075-.111.149-.092.245-.056l.713.339c.105.051.175.077.201.12.026.043.026.25-.118.655z"/>
            </svg>
            اطلب عبر واتساب
          </a>
          <a href="https://t.me/+201014762938"
            target="_blank" rel="noopener"
            class="btn-olive-outline text-base px-8 py-4 w-full sm:w-auto justify-center">
            ✈️ تيليجرام
          </a>
          <a href="mailto:Goldsiniia@gmail.com?subject=طلب زيت سينا جولد"
            class="btn-olive-outline text-base px-8 py-4 w-full sm:w-auto justify-center">
            📧 إيميل
          </a>
        </div>

        <div class="mt-8 inline-flex items-center gap-2 px-6 py-2 rounded-full"
          style="background:rgba(16,185,129,0.06);border:1px solid rgba(16,185,129,0.18);">
          <span class="w-2.5 h-2.5 bg-green-500 rounded-full" style="animation:pulse 1.5s infinite;"></span>
          <span style="color:#059669;font-size:0.9rem;font-weight:700;">الدفع عند الاستلام 100%</span>
        </div>
      </div>

      <div class="mt-12 grid grid-cols-1 sm:grid-cols-3 gap-4 form-trust gsap-fade-up">
        <div v-for="t in trustBadges" :key="t.label" class="white-card p-6 flex flex-col items-center text-center gap-3">
          <div style="font-size:2rem;">{{ t.icon }}</div>
          <p style="font-size:0.85rem;font-weight:700;color:#6B7E64;line-height:1.4;">{{ t.label }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue';
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger);

const trustBadges = [
  { icon:'🚚', label:'توصيل لكل المحافظات' },
  { icon:'💳', label:'مش هنختلف علي الدفع يحج' },
  { icon:'↩️', label:'ضمان جودة أو استرداد' },
];

onMounted(() => {
  gsap.to('.form-header', { scrollTrigger:{trigger:'.form-header',start:'top 85%'}, y:0,opacity:1,duration:0.8,ease:'power3.out' });
  gsap.to('.form-trust',  { scrollTrigger:{trigger:'.form-trust', start:'top 90%'}, y:0,opacity:1,duration:0.6,delay:0.2 });
});
</script>