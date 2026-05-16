<!--
  ██████╗████████╗██████╗  █████╗ ████████╗███████╗ █████╗
 ██╔════╝╚══██╔══╝██╔══██╗██╔══██╗╚══██╔══╝╚══███╔╝██╔══██╗
 ╚█████╗    ██║   ██████╔╝███████║   ██║     ███╔╝ ███████║
  ╚═══██╗   ██║   ██╔══██╗██╔══██║   ██║    ███╔╝  ██╔══██║
 ██████╔╝   ██║   ██║  ██║██║  ██║   ██║   ███████╗██║  ██║
 ╚═════╝    ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚══════╝╚═╝  ╚═╝
  Engineering real-world systems. Zero compromises.
-->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=_0D1117,_161B22&height=280&section=header&text=STRATZA&fontSize=130&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=ENGINEERING%20REAL-WORLD%20SYSTEMS&descSize=20&descColor=8B949E&descAlignY=62" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=18&duration=2000&pause=700&color=ffffff&center=true&vCenter=true&width=900&lines=Infrastructure+tooling+for+production+environments;Async-native+%7C+Secure+by+default+%7C+Zero+legacy+debt;Built+for+the+3am+incident%2C+not+the+conference+talk;No+unnecessary+abstractions.+No+hidden+behavior.;Systems+that+behave+correctly+under+real+load." alt="Typing SVG" />

<br/>

</div>

<div align="center">

<img src="https://img.shields.io/badge/-%E2%96%A0%20INFRASTRUCTURE-0D1117?style=for-the-badge&labelColor=0D1117&color=58A6FF&logo=github&logoColor=58A6FF" />
<img src="https://img.shields.io/badge/-%E2%96%A0%20PERFORMANCE-0D1117?style=for-the-badge&labelColor=0D1117&color=3FB950&logo=rocket&logoColor=3FB950" />
<img src="https://img.shields.io/badge/-%E2%96%A0%20SECURITY%20FIRST-0D1117?style=for-the-badge&labelColor=0D1117&color=F78166&logo=letsencrypt&logoColor=F78166" />
<img src="https://img.shields.io/badge/-%E2%96%A0%20ASYNC%20NATIVE-0D1117?style=for-the-badge&labelColor=0D1117&color=D2A8FF&logo=python&logoColor=D2A8FF" />

<br/><br/>

<a href="https://github.com/Di3Z1E/spindlex/stargazers"><img src="https://img.shields.io/github/stars/stratza/spindlex?style=for-the-badge&labelColor=161B22&color=58A6FF&logo=github&label=SpindleX+Stars" /></a>
<a href="https://github.com/Di3Z1E/spindlex/commits"><img src="https://img.shields.io/github/commit-activity/m/stratza/spindlex?style=for-the-badge&labelColor=161B22&color=3FB950&label=Monthly+Commits" /></a>
<a href="https://github.com/Di3Z1E/spindlex/issues"><img src="https://img.shields.io/github/issues/stratza/spindlex?style=for-the-badge&labelColor=161B22&color=F78166&label=Open+Issues" /></a>
<a href="https://github.com/Di3Z1E/spindlex/pulls"><img src="https://img.shields.io/github/issues-pr/stratza/spindlex?style=for-the-badge&labelColor=161B22&color=D2A8FF&label=Open+PRs" /></a>
<a href="https://github.com/Di3Z1E/spindlex/blob/main/LICENSE"><img src="https://img.shields.io/github/license/stratza/spindlex?style=for-the-badge&labelColor=161B22&color=8957E5" /></a>

</div>

<br/>

<div align="center">

```
  downtime  ──  direct cost       latency  ──  your users notice       complexity  ──  operational risk
```

</div>

> We build infrastructure tooling for environments where those three lines aren't philosophy - they're the spec.
> Not DevOps blogging. Not abstractions that demo well and break at 2x load.
> **Every tool we ship is designed to behave correctly at 3am, during the incident, when no one has time to read docs.**

<br/>

---

<br/>

<div align="center">

## 〈 ACTIVE SYSTEMS 〉

</div>

<br/>

<table>
<tr>
<td width="55%">

### ⚡ [SpindleX](https://github.com/Di3Z1E/spindlex)

**Async-first SSH stack - built to replace legacy Python SSH tooling**

A pure-Python SSH library designed for the modern developer. `asyncio` at its core - not bolted on afterward. Ed25519 only. Modern ciphers only. No SSHv1 ghosts in the codebase.

```python
async with SpindleX(
    host="prod-01",
    key=Ed25519Key.from_file("~/.ssh/id_ed25519")
) as ssh:
    result = await ssh.run("systemctl status api")
    # non-blocking. concurrent. secure by default.
```

</td>
<td width="45%" valign="top">

<br/>

| | |
|---|---|
| **Architecture** | `asyncio`-native from day one |
| **Security** | Ed25519 + modern ciphers only |
| **Performance** | Streamlined connection lifecycle |
| **API** | Clean, explicit, developer-first |
| **Philosophy** | Zero legacy shims - ever |

<br/>

<div align="center">
<a href="https://github.com/Di3Z1E/spindlex"><img src="https://img.shields.io/badge/View%20SpindleX-58A6FF?style=for-the-badge&logo=github&logoColor=white" /></a>
&nbsp;
<a href="https://github.com/Di3Z1E/spindlex/stargazers"><img src="https://img.shields.io/badge/Star%20It-F0C040?style=for-the-badge&logo=github&logoColor=black" /></a>
</div>

</td>
</tr>
</table>

<br/>

---

<br/>

<div align="center">

## 〈 ENGINEERING CONSTRAINTS 〉

*These are not guidelines. They are load-bearing rules on every decision.*

<br/>

<table>
<tr>
<th align="center" width="50%">❌ &nbsp; Never</th>
<th align="center" width="50%">✅ &nbsp; Always</th>
</tr>
<tr>
<td align="center">Unnecessary abstractions</td>
<td align="center">Explicit over implicit</td>
</tr>
<tr>
<td align="center">Legacy compatibility layers</td>
<td align="center">Everything is measurable</td>
</tr>
<tr>
<td align="center">Hidden behavior or implicit magic</td>
<td align="center">Every component is replaceable</td>
</tr>
<tr>
<td align="center">Complexity that doesn't earn its place</td>
<td align="center">Security defaults that never need overriding</td>
</tr>
</table>

</div>

<br/>

---

<br/>

<div align="center">

## 〈 TECHNOLOGY FOUNDATION 〉

<br/>

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white" />
<img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
<img src="https://img.shields.io/badge/Rust-CE422B?style=for-the-badge&logo=rust&logoColor=white" />

<br/>

<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />

<br/>

<img src="https://img.shields.io/badge/SSH%20%2F%20Ed25519-F78166?style=for-the-badge&logo=gnupg&logoColor=white" />
<img src="https://img.shields.io/badge/TLS%20Modern%20Only-58A6FF?style=for-the-badge&logo=letsencrypt&logoColor=white" />
<img src="https://img.shields.io/badge/asyncio%20Native-3FB950?style=for-the-badge&logo=python&logoColor=white" />

</div>

<br/>

---

<br/>

<div align="center">

## 〈 ACTIVITY 〉

<br/>

<table width="100%">
<tr>
<td align="center" width="50%">

<img src="https://img.shields.io/badge/David%20Azani-@Di3Z1E-58A6FF?style=flat-square&logo=github&logoColor=white&labelColor=161B22" />

<img src="https://streak-stats.demolab.com/?user=Di3Z1E&theme=github-dark-blue&hide_border=true&background=0D1117&stroke=58A6FF&ring=3FB950&fire=F78166&currStreakLabel=58A6FF&sideLabels=C9D1D9&dates=8B949E" width="100%" />

</td>
<td align="center" width="50%">

<img src="https://img.shields.io/badge/Adi%20Roth-@adirothbuilds-3FB950?style=flat-square&logo=github&logoColor=white&labelColor=161B22" />

<img src="https://streak-stats.demolab.com/?user=adirothbuilds&theme=github-dark-blue&hide_border=true&background=0D1117&stroke=3FB950&ring=58A6FF&fire=F78166&currStreakLabel=3FB950&sideLabels=C9D1D9&dates=8B949E" width="100%" />

</td>
</tr>
</table>

<br/>

<img src="https://img.shields.io/badge/David%20Azani-@Di3Z1E-58A6FF?style=flat-square&logo=github&logoColor=white&labelColor=161B22" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Di3Z1E&theme=react-dark&hide_border=true&color=58A6FF&line=3FB950&point=F78166&bg_color=0D1117&area=true&area_color=58A6FF" width="100%" />

<img src="https://img.shields.io/badge/Adi%20Roth-@adirothbuilds-3FB950?style=flat-square&logo=github&logoColor=white&labelColor=161B22" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=adirothbuilds&theme=react-dark&hide_border=true&color=3FB950&line=58A6FF&point=F78166&bg_color=0D1117&area=true&area_color=3FB950" width="100%" />

</div>

<br/>

---

<br/>

<div align="center">

## 〈 THE BUILDERS 〉

<br/>

<table>
<tr>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/u/209997463?v=4" width="120" style="border-radius:50%;border:3px solid #3FB950;" />

<h3>Adi Roth</h3>

<img src="https://img.shields.io/badge/DevOps%20%2F%20Systems%20Engineering-161B22?style=flat-square&labelColor=161B22&color=3FB950&logoColor=white" />

<br/><br/>

<a href="https://github.com/adirothbuilds"><img src="https://img.shields.io/badge/@adirothbuilds-181717?style=flat-square&logo=github&logoColor=white" /></a>
<a href="https://linkedin.com/in/adi-roth-4496a0162"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
<a href="https://www.youtube.com/@adiroth_builds"><img src="https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white" /></a>
<a href="https://x.com/adiroth_builds"><img src="https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white" /></a>

<br/><br/>

<img src="https://img.shields.io/badge/DevOps-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=58A6FF" />
<img src="https://img.shields.io/badge/Automation-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=3FB950" />
<img src="https://img.shields.io/badge/AI%20Tooling-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=D2A8FF" />
<img src="https://img.shields.io/badge/Scalable%20Systems-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=F78166" />

</td>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/u/100869868?v=4" width="120" style="border-radius:50%;border:3px solid #58A6FF;" />

<h3>David Azani</h3>

<img src="https://img.shields.io/badge/Cloud%20Infrastructure%20%2F%20SpindleX%20Author-161B22?style=flat-square&labelColor=161B22&color=58A6FF&logoColor=white" />

<br/><br/>

<a href="https://github.com/Di3Z1E"><img src="https://img.shields.io/badge/@Di3Z1E-181717?style=flat-square&logo=github&logoColor=white" /></a>

<br/><br/>

<img src="https://img.shields.io/badge/Cloud%20Infrastructure-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=58A6FF" />
<img src="https://img.shields.io/badge/Python-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=python&logoColor=3FB950" />
<img src="https://img.shields.io/badge/SSH-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=gnupg&logoColor=D2A8FF" />
<img src="https://img.shields.io/badge/Protocol%20Engineering-161B22?style=flat-square&labelColor=161B22&color=161B22&logo=github&logoColor=F78166" />

</td>
</tr>
</table>

</div>

<br/>

---

<br/>

<div align="center">

## 〈 ROADMAP 〉

<br/>

<table>
<tr>
<th align="center" width="50%">🔨 &nbsp; Now</th>
<th align="center" width="50%">🔭 &nbsp; Next</th>
</tr>
<tr>
<td align="center">SpindleX v1 stable release</td>
<td align="center">Infrastructure runtime layer</td>
</tr>
<tr>
<td align="center">Expanded key/cipher support</td>
<td align="center">Automation framework suite</td>
</tr>
<tr>
<td align="center">Performance benchmarking suite</td>
<td align="center">Protocol-level tooling library</td>
</tr>
<tr>
<td align="center">Public contribution guidelines</td>
<td align="center">High-performance system primitives</td>
</tr>
</table>

</div>

<br/>

---

<br/>

<div align="center">

## 〈 CONTRIBUTING 〉

<br/>

We ship with intent. Before contributing:

<br/>

<table>
<tr>
<th align="center">#</th>
<th align="center">Rule</th>
</tr>
<tr>
<td align="center">1</td>
<td align="center"><b>Read the constraints</b> - no exceptions, no "just this once"</td>
</tr>
<tr>
<td align="center">2</td>
<td align="center"><b>Open an issue first</b> - discuss before building anything non-trivial</td>
</tr>
<tr>
<td align="center">3</td>
<td align="center"><b>Performance is a hard gate</b> - regressions block merge, always</td>
</tr>
<tr>
<td align="center">4</td>
<td align="center"><b>Security improvements</b> - always welcome, always reviewed carefully</td>
</tr>
</table>

<br/>

<a href="https://github.com/Di3Z1E/spindlex/blob/main/CONTRIBUTING.md"><img src="https://img.shields.io/badge/Contribute%20to%20SpindleX-3FB950?style=for-the-badge&logo=github&logoColor=white" /></a>
&nbsp;
<a href="https://github.com/Di3Z1E/spindlex/issues/new"><img src="https://img.shields.io/badge/Open%20an%20Issue-F78166?style=for-the-badge&logo=github&logoColor=white" /></a>
&nbsp;
<a href="https://github.com/Di3Z1E/spindlex/discussions"><img src="https://img.shields.io/badge/Discussions-58A6FF?style=for-the-badge&logo=github&logoColor=white" /></a>

</div>

<br/>

---

<br/>

<div align="center">

<img src="https://komarev.com/ghpvc/?username=Di3Z1E&style=flat-square&color=8B949E&label=Views" />

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=_0D1117,_161B22&height=140&section=footer" width="100%" />

</div>
