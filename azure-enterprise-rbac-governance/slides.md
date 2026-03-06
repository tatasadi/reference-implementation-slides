---
theme: default
background: '#0f0f23'
class: 'text-center'
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: slide-left
title: Azure RBAC Governance
fonts:
  sans: 'Inter'
  mono: 'Fira Code'
canvasWidth: 1080
aspectRatio: '1/1'
---

<style>
:root {
  --slidev-theme-primary: #a78bfa;
}

.slidev-layout {
  @apply bg-gradient-to-br from-[#0f0f23] via-[#1a1a3e] to-[#0f0f23];
  width: 1080px;
  height: 1080px;
  padding: 80px;
}

h1 {
  @apply text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 via-violet-400 to-purple-500 bg-clip-text text-transparent leading-tight;
}

h2 {
  @apply text-5xl font-semibold text-purple-300 mb-6;
}

p, li {
  @apply text-4xl leading-relaxed;
}

.subtitle {
  @apply text-4xl text-gray-300 font-light leading-relaxed;
}

.highlight {
  @apply text-purple-400 font-semibold;
}

.slide-counter {
  @apply absolute bottom-8 right-8 bg-purple-500/20 border-2 border-purple-400 rounded-full px-6 py-3 text-2xl font-semibold text-purple-300;
}
</style>

<!-- Slide 1 - Hook -->
<div class="flex flex-col justify-center items-center h-full text-center px-12">
  <!-- Top badge -->
  <div class="bg-purple-500/30 border-2 border-purple-400 rounded-full px-8 pb-4 mb-8">
    <p class="!text-3xl text-purple-300 font-bold !mb-0">🔐 Azure Security</p>
  </div>

  <!-- Attention-grabbing stat -->
  <div class="mb-6">
    <p class="!text-9xl font-black text-red-400 !mb-2 !leading-none">80%</p>
    <p class="!text-4xl text-gray-300 !mb-0">of Azure environments struggle with this</p>
  </div>

  <!-- Main title -->
  <h1 class="!text-8xl !mb-6 !mt-8">RBAC Governance</h1>
  <h2 class="!text-5xl !mb-10 text-gray-300 font-light">The enterprise access control challenge</h2>

  <!-- Value proposition -->
  <div class="bg-gradient-to-r from-purple-500/20 to-violet-500/20 border-l-4 border-purple-400 rounded-r-2xl px-10 py-6 mt-4">
    <p class="!text-4xl text-purple-200 !mb-0">Learn how to prevent privilege sprawl and unauthorized access at scale</p>
  </div>

  <!-- Swipe indicator -->
  <div class="mt-10">
    <p class="!text-3xl text-gray-400 !mb-0">👉 Swipe for the solution • 7 slides</p>
  </div>

  <div class="slide-counter">1/8</div>
</div>

---
layout: default
---

<!-- Slide 2 - The Problem -->
<div class="flex flex-col justify-center h-full">
  <h2 class="!text-6xl !mb-12">Why RBAC becomes difficult to manage</h2>
  <p class="!text-4xl text-gray-300 !mb-10 !leading-relaxed">As Azure environments grow, access governance often becomes chaotic.</p>

  <div class="space-y-6 !text-4xl text-gray-200">
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Direct user → Owner assignments</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Permanent privileged roles</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>RBAC changes done manually in the portal</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>No clear separation between teams</span>
    </div>
  </div>

  <p class="!text-4xl text-purple-300 mt-12 font-semibold">Over time this becomes difficult to control.</p>
  <div class="slide-counter">2/8</div>
</div>

---
layout: default
---

<!-- Slide 3 - The Risk -->
<div class="flex flex-col justify-center h-full">
  <h2 class="!text-6xl !mb-12">Why this becomes a real problem</h2>
  <p class="!text-4xl text-gray-300 !mb-10 !leading-relaxed">Unstructured RBAC creates serious risks.</p>

  <div class="space-y-6 !text-4xl text-gray-200">
    <div class="flex items-start gap-4">
      <span class="text-red-400 !text-5xl">•</span>
      <span>Privilege sprawl across subscriptions</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-red-400 !text-5xl">•</span>
      <span>Difficult access reviews</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-red-400 !text-5xl">•</span>
      <span>Large blast radius for compromised accounts</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-red-400 !text-5xl">•</span>
      <span>No audit trail for RBAC changes</span>
    </div>
  </div>

  <p class="!text-4xl text-purple-300 mt-12 font-semibold">This is where many Azure environments struggle.</p>
  <div class="slide-counter">3/8</div>
</div>

---
layout: default
---

<!-- Slide 4 - A Better Approach -->
<div class="flex flex-col justify-center h-full">
  <h2 class="!text-6xl !mb-12">Enterprise RBAC governance model</h2>
  <p class="!text-4xl text-gray-300 !mb-10 !leading-relaxed">A structured model usually includes:</p>

  <div class="space-y-6 !text-4xl text-gray-200">
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Group-based RBAC</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Management Group hierarchy</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Privileged Identity Management (PIM)</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Policy guardrails</span>
    </div>
  </div>

  <p class="!text-4xl text-purple-300 mt-12 font-semibold">This creates controlled and auditable access.</p>
  <div class="slide-counter">4/8</div>
</div>

---
layout: default
---

<!-- Slide 5 - Access Architecture -->
<div class="flex flex-col justify-center items-center h-full">
  <h2 class="!text-6xl !mb-10 text-center">Group-based access flow</h2>

  <div class="flex flex-col items-center gap-6 !text-4xl font-semibold">
    <div class="bg-purple-500/20 border-2 border-purple-400 rounded-2xl px-10 py-6 text-purple-300">
      User
    </div>
    <div class="text-purple-400 !text-5xl">↓</div>
    <div class="bg-purple-500/20 border-2 border-purple-400 rounded-2xl px-10 py-6 text-purple-300">
      Entra ID Security Group
    </div>
    <div class="text-purple-400 !text-5xl">↓</div>
    <div class="bg-purple-500/20 border-2 border-purple-400 rounded-2xl px-10 py-6 text-purple-300">
      RBAC Role Assignment
    </div>
    <div class="text-purple-400 !text-5xl">↓</div>
    <div class="bg-purple-500/20 border-2 border-purple-400 rounded-2xl px-10 py-6 text-purple-300">
      Azure Resource Scope
    </div>
  </div>

  <div class="mt-10 bg-purple-900/30 border-l-4 border-purple-400 px-8 py-5 rounded-r-xl">
    <p class="!text-3xl text-gray-200"><span class="text-purple-300 font-bold">Key rule:</span> No direct user → role assignments</p>
  </div>
  <div class="slide-counter">5/8</div>
</div>

---
layout: default
---

<!-- Slide 6 - Implementation Pattern -->
<div class="flex flex-col justify-center h-full">
  <h2 class="!text-6xl !mb-12">How this can be implemented</h2>
  <p class="!text-4xl text-gray-300 !mb-10 !leading-relaxed">Example approach:</p>

  <div class="space-y-6 !text-4xl text-gray-200">
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>RBAC defined via Terraform</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>PIM for privileged platform roles</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Custom roles for CI/CD pipelines</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Azure Policy preventing risky assignments</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>RBAC changes reviewed through CI/CD</span>
    </div>
  </div>

  <p class="!text-4xl text-purple-300 mt-12 font-semibold">This creates a controlled governance model.</p>
  <div class="slide-counter">6/8</div>
</div>

---
layout: default
---

<!-- Slide 7 - Soft Close -->
<div class="flex flex-col justify-center h-full">
  <h2 class="!text-6xl !mb-12">Reference implementation</h2>
  <p class="!text-4xl text-gray-300 !mb-10 !leading-relaxed">I recently built a small reference implementation exploring this model using:</p>

  <div class="space-y-6 !text-4xl text-gray-200 mb-12">
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Terraform</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Azure RBAC</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Privileged Identity Management</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>Azure Policy</span>
    </div>
    <div class="flex items-start gap-4">
      <span class="text-purple-400 !text-5xl">•</span>
      <span>CI/CD approval workflows</span>
    </div>
  </div>

  <p class="!text-4xl text-purple-400 font-semibold">Project details in the comments. 👇</p>
  <div class="slide-counter">7/8</div>
</div>

---
layout: default
---

<!-- Slide 8 - Final CTA Slide -->
<div class="flex flex-col justify-center items-center h-full text-center py-12">
  <div class="mb-6">
    <img src="https://stta.blob.core.windows.net/portfolio/ehsan.jpg" alt="Ehsan Tatasadi" class="w-56 h-56 rounded-full mx-auto border-8 border-purple-500 shadow-2xl object-cover">
  </div>

  <h1 class="!text-7xl !mb-4">Ehsan Tatasadi</h1>
  <p class="subtitle !text-4xl text-gray-300 !mb-12">Senior Azure Engineer (Platform & DevOps)</p>

  <div class="bg-purple-500/20 border-2 border-purple-400 rounded-3xl px-10 py-6 mb-10">
    <p class="!text-3xl text-gray-200">💬 What would you implement first in your environment?</p>
  </div>

  <div class="bg-purple-600 rounded-3xl px-14 py-6 mb-10">
    <p class="!text-4xl text-white font-bold">👉 Follow for more Azure tips</p>
  </div>

  <p class="!text-3xl text-gray-400 font-semibold">#Azure #DevOps #CloudEngineering</p>
  <div class="slide-counter">8/8</div>
</div>
