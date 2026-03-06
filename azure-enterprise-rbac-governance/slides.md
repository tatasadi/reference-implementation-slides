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
</style>

<!-- Slide 1 - Hook -->
<div class="flex flex-col justify-center items-center h-full text-center px-12">
  <h1 class="!text-8xl !mb-12">Azure RBAC Governance</h1>
  <h2 class="!text-6xl !mb-8">for Enterprise Environments</h2>
  <p class="subtitle !text-5xl mt-8">A simple architecture model for controlling access in Azure</p>
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
</div>
