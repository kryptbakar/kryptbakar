<!--
  ╔══════════════════════════════════════════════════════════════╗
  ║  kryptbakar · profile README                                   ║
  ║  Custom animated SVGs live in ./assets/  → commit that folder. ║
  ╚══════════════════════════════════════════════════════════════╝
-->

<div align="center">

<!-- ░░░ HERO: hand-authored animated CRT terminal (./assets/header.svg) ░░░ -->
<a href="https://creativefolio-nine.vercel.app/">
 alt="Muhammad Abubakar — Cyber Security Researcher" />
</a>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=3200&pause=800&color=27AE60&center=true&vCenter=true&width=720&lines=Don't+just+find+vulns+%E2%80%94+model+them%2C+own+them%2C+patch+them.;%2B0.299+bits%2Fs%2FHz+secrecy+gain+over+fixed+allocation.;Cyber-curious.+Ethically+dangerous." alt="tagline" />

<br/><br/>

<img src="https://komarev.com/ghpvc/?username=kryptbakar&label=Profile+Views&color=27ae60&style=for-the-badge" />
&nbsp;
<img src="https://img.shields.io/badge/Open%20to-Security%20Roles%20%26%20Collabs-27ae60?style=for-the-badge&logo=handshake&logoColor=white" />
&nbsp;
<img src="https://img.shields.io/badge/Dean's%20Honor%20List-GIKI%20Sem%205-27ae60?style=for-the-badge&logo=googlescholar&logoColor=white" />
&nbsp;
<img src="https://img.shields.io/badge/📍-Pakistan-0d1117?style=for-the-badge" />

</div>

> [!NOTE]
> **`mission`** → Build systems that are *mathematically* harder to compromise. I don't stop at finding the bug — I model it, reproduce it, and engineer it out of existence.

---

## `> whoami`

```bash
┌──(kryptbakar㉿giki)-[~]
└─$ cat about.txt

Name     : Muhammad Abubakar
Role     : Final-year Cyber Security Undergraduate
School   : Ghulam Ishaq Khan Institute (GIKI) — Class of 2027
CGPA     : 3.2 / 4.00   ★ Dean's Honor List (5th Semester)
Focus    : Physical-layer Wireless Security · AppSec · DevSecOps · ML-Security
Industry : 2× Intern @ Thingtrax — Security Testing & Secure Software Dev
```

<details>
<summary><b><code>$ ls ~/identity/</code></b> &nbsp;— expand the dossier</summary>

<br/>

| `field` | `value` |
|:--|:--|
| 🎯 **Specialty** | DQN-based artificial-noise allocation for MISO wiretap channels |
| 🧪 **Research result** | **+0.299 bits/s/Hz** secrecy gain over fixed allocation at low SNR |
| 🏭 **Experience** | Security Testing & Secure SW Dev — *Thingtrax* (2×) |
| 🛠️ **Mindset** | Offensive recon → defensive engineering → provable hardening |
| 🌱 **Now learning** | Malware analysis · reverse engineering · adversarial ML |

</details>

---

## `> cat research/featured.md` 🛰️

<div align="center">

<!-- ░░░ hand-authored animated result panel (./assets/secrecy.svg) ░░░ -->
<img src="secrecy.svg" width="860" alt="DQN artificial-noise allocation: +0.299 bits/s/Hz secrecy gain" />

</div>

I train a **Deep Q-Network** to adaptively split transmit power between the information beam and **artificial noise (AN)** on a MISO wiretap channel — under **Rayleigh fading** with **imperfect CSI** — to maximise the *secrecy rate*, the throughput an eavesdropper provably **cannot** decode.

**The quantity being maximised — secrecy capacity:**

$$
C_s \;=\; \Big[\,\log_2\!\big(1+\gamma_b\big)\;-\;\log_2\!\big(1+\gamma_e\big)\Big]^{+}
$$

**The transmitted signal** — information beam + artificial noise, with the power split $\phi$ chosen by the learned policy:

$$
\mathbf{x}\;=\;\sqrt{\phi P}\;\mathbf{w}\,s\;+\;\sqrt{(1-\phi)P}\;\mathbf{z},
\qquad
\phi^{\star}=\pi_\theta(\text{CSI})\in[0,1]
$$

**How the agent learns it — the DQN / Bellman update:**

$$
Q(s,a)\;\leftarrow\;Q(s,a)\;+\;\alpha\Big[\,r+\gamma\max_{a'}Q(s',a')-Q(s,a)\,\Big]
$$

<sub>where γ_b, γ_e are the legitimate / eavesdropper SINRs, <b>w</b> the beamformer, <b>z</b> the AN vector, φ ∈ [0,1] the power-split action, and [·]⁺ = max(·, 0).</sub>

**Closed control loop:**

```mermaid
%%{init: {"theme":"base","themeVariables":{"primaryColor":"#0d2818","primaryTextColor":"#9dffc0","primaryBorderColor":"#27ae60","lineColor":"#27ae60","secondaryColor":"#11261a","tertiaryColor":"#0d1117","fontFamily":"monospace"}}}%%
flowchart LR
    S["📡 CSI<br/>(state)"] --> AG(("🤖 DQN<br/>Agent"))
    AG -->|"action φ ∈ [0,1]"| ENV["🛰️ MISO Wiretap<br/>Environment"]
    ENV -->|"reward = secrecy rate"| AG
    ENV --> OUT["✅ Adaptive AN split<br/>+0.299 b/s/Hz"]
```

---

## `> tree ~/arsenal` ⚔️

> [!TIP]
> Mapped by intent — offense, defense, and the ML that powers both.

```mermaid
mindmap
  root((ARSENAL))
    Offensive
      Burp Suite
      Metasploit
      Nmap
      Wireshark
      Kali Linux
    AppSec / DevSecOps
      OWASP Top 10
      Bandit SAST
      pip-audit SCA
      GitHub Actions
      Secure SDLC
    ML Security
      TensorFlow
      PyTorch
      CatBoost
      scikit-learn
      LOF Anomaly
    Wireless / RF
      Secrecy Capacity
      Beamforming
      DQN Allocation
      Imperfect CSI
    Build
      Python
      C / C++
      Flask
      Docker
      SQL
```

<div align="center">

<img src="https://skillicons.dev/icons?i=python,cpp,js,ts,bash,sql&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=linux,kali,docker,github,githubactions&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=tensorflow,pytorch,flask,react,nextjs&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=mysql,postgres,mongodb&theme=dark" />

`#0D1117` &nbsp; `#27AE60` &nbsp; `#9DFFC0` &nbsp; <sub>← profile palette</sub>

</div>

---

## `> ./run operations/` 🎯

| Operation | What it does | Stack |
|:--|:--|:--|
| 🔬 **DQN Artificial-Noise Allocation** | RL agent splits power for max secrecy on a MISO wiretap channel — **+0.299 b/s/Hz** at low SNR. | `Python` `TensorFlow` `RL` |
| 🕵️ **Phantom Identity** | Manifest V3 extension spoofing Canvas / WebGL / Navigator / timezone fingerprints per session, with a live entropy dashboard. **Zero telemetry.** | `JavaScript` `MV3` `Privacy` |
| 🤖 **AI Intrusion Detection** | Hybrid **CatBoost + LOF** — supervised classifier *plus* unsupervised novelty detection. **1.6M samples in ~7.5 min**; catches unseen attack classes. | `CatBoost` `sklearn` |
| 🏦 **Bakri Pay** | Full-stack Flask MVC bank — Argon2/bcrypt, CSRF tokens, parameterised queries, authed REST. Full OWASP Top 10, validated in Burp. | `Flask` `OWASP` |
| ⚙️ **Secure CI/CD Pipeline** | Fail-fast security gates any repo can inherit *(diagram below)*. | `GitHub Actions` `SAST/SCA` |

<details>
<summary><b><code>$ cat operations/devsecops/pipeline.yml</code></b> &nbsp;— see the security gates</summary>

<br/>

```mermaid
%%{init: {"theme":"base","themeVariables":{"primaryColor":"#0d2818","primaryTextColor":"#9dffc0","primaryBorderColor":"#27ae60","lineColor":"#27ae60","secondaryColor":"#11261a","tertiaryColor":"#0d1117","fontFamily":"monospace"}}}%%
flowchart LR
    P["git push"] --> CI{"GitHub<br/>Actions"}
    CI --> B["Bandit<br/>SAST"]
    CI --> D["pip-audit<br/>SCA"]
    CI --> S["Secrets<br/>Scan"]
    B & D & S --> G{"Security<br/>Gate"}
    G -->|pass| OK["🚀 Deploy"]
    G -->|fail| NO["⛔ Block + Report"]
```

</details>

---

## `> git log --trajectory` 📈

```mermaid
timeline
    title Operation Timeline · 2023 → 2027
    2023 : Began B.S. Cyber Security @ GIKI
    2024 : Security Testing Intern @ Thingtrax : Shipped Bakri Pay (OWASP Top 10)
    2025 : Secure SW Dev Intern @ Thingtrax : DQN secrecy research (+0.299 b/s/Hz) : Dean's Honor List — Sem 5
    2026 : AI IDS · DevSecOps pipeline · Phantom Identity
    2027 : Graduate — open to security roles
```

---

## `> telemetry --github` 📊

<div align="center">

<img height="170em" src="https://github-readme-stats.vercel.app/api?username=kryptbakar&show_icons=true&theme=chartreuse-dark&hide_border=true&bg_color=0D1117&title_color=27AE60&icon_color=27AE60&text_color=c9d1d9" />
&nbsp;
<img height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kryptbakar&layout=compact&theme=chartreuse-dark&hide_border=true&bg_color=0D1117&title_color=27AE60&text_color=c9d1d9" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=kryptbakar&theme=dark&hide_border=true&background=0D1117&ring=27AE60&fire=27AE60&currStreakLabel=27AE60&sideLabels=27AE60&dates=6e7681" alt="Streak" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=kryptbakar&theme=github-compact&bg_color=0D1117&color=27AE60&line=27AE60&point=ffffff&area=true&area_color=27ae6033&hide_border=true" alt="Activity Graph" />

<br/>

<img src="https://github-profile-trophy.vercel.app/?username=kryptbakar&theme=matrix&no-frame=true&margin-w=10&column=7" />

</div>

---

## `> cat certs/*.crt` 🎓

<div align="center">

<img src="https://img.shields.io/badge/Google-Cybersecurity%20Professional-4285F4?style=for-the-badge&logo=google&logoColor=white" />
&nbsp;
<img src="https://img.shields.io/badge/Macquarie%20Uni-AI%20for%20Cyber%20Security-E63946?style=for-the-badge&logo=academia&logoColor=white" />
<br/><br/>
<img src="https://img.shields.io/badge/LPI-Linux%20Essentials-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
&nbsp;
<img src="https://img.shields.io/badge/Cisco-Networking%20Basics-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
&nbsp;
<img src="https://img.shields.io/badge/Cisco-Intro%20to%20Cybersecurity-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />

</div>

---

## `> ./connect` 🕸️

<div align="center">

<a href="https://linkedin.com/in/muhammadabubakar"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
&nbsp;
<a href="mailto:abubakaramirwork@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
&nbsp;
<a href="https://creativefolio-nine.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-27AE60?style=for-the-badge&logo=vercel&logoColor=white" /></a>
&nbsp;
<a href="https://instagram.com/dumbutthehe"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" /></a>

</div>

> [!IMPORTANT]
> 💬 **Ask me about** → OWASP Top 10 & secure SDLC · DevSecOps SAST/SCA gating · physical-layer secrecy capacity · XSS/SQLi/auth-bypass (and engineering them out) · CTFs, bug bounty & recon · ML for intrusion detection.

---

<!-- contribution snake (needs the snake GitHub Action — see setup notes) -->
<div align="center">
  <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake" />
</div>

> [!CAUTION]
> All offensive tooling and research here is for **authorized, educational, and defensive** purposes only. Stay ethical. Hack legally. 🔐
