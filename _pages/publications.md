---
permalink: /publications/
layout: single
author_profile: true
title: Publications
classes: wide
---

<style>

  .arxiv-abstract {
  font-size: 0.85em;
  color: #fefaf5; /* warm marfil-like color */
  background-color: transparent;
  padding: 12px 16px;
  margin-top: 8px;
  border: 1px solid white;
  border-radius: 6px;
  max-width: 800px;
  line-height: 1.5;
  display: none;
  box-shadow: 0 1px 2px rgba(255, 255, 255, 0.1);
}

button {
  font-size: 0.85em;
  background-color: transparent;
  border: none;
  color: #7d5a5a; /* soft reddish-brown to match your theme */
  text-decoration: underline;
  cursor: pointer;
  margin-top: 5px;
  padding: 0;
}

button:hover {
  color: #5c3d3d;
}
</style>

<script>
  async function fetchAbstract(arxivId, container) {
    const url = `https://export.arxiv.org/api/query?id_list=${arxivId}`;
    try {
      const response = await fetch(url);
      const xml = await response.text();
      const abstract = new window.DOMParser()
        .parseFromString(xml, "text/xml")
        .querySelector("entry > summary").textContent;
      container.innerText = abstract.trim();
    } catch (error) {
      container.innerText = "Failed to load abstract.";
    }
  }

  function toggleAbstract(button) {
    const abstractDiv = button.nextElementSibling;
    const arxivId = abstractDiv.getAttribute("data-arxiv-id");

    if (abstractDiv.style.display === "none") {
      abstractDiv.style.display = "block";
      if (!abstractDiv.dataset.loaded) {
        fetchAbstract(arxivId, abstractDiv);
        abstractDiv.dataset.loaded = true;
      }
      button.innerText = "Hide abstract";
    } else {
      abstractDiv.style.display = "none";
      button.innerText = "Show abstract";
    }
  }
</script>

Titles link to the published version and <i class="ai ai-arxiv"></i> links to the arXiv version.<br>


#### Pre-prints:

<ol reversed="">

<li>
  <em>On Tensor-based Polynomial Hamiltonian Systems</em> <span><a href="https://arxiv.org/pdf/2503.21487" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with S. Cui, G Zhang, and M Cao)</small>
  <button onclick="toggleAbstract(this)">Show abstract</button>
  <div class="arxiv-abstract" data-arxiv-id="2503.21487" style="display:none;">
    <em>Loading abstract...</em>
  </div>
  </li>

<li>
  <em>Higher-order Laplacian dynamics on hypergraphs with cooperative and antagonistic interactions</em> <span><a href="https://arxiv.org/pdf/2502.08276" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with S. Cui, C Zhang, B Jiang, and M Cao)</small>
  </li>

<li>
  <em>On the Eigenvalues of Graphs with Mixed Algebraic Structure</em> <span><a href="https://arxiv.org/pdf/2408.00487" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with R. Bonetto) </small>
  </li>


<li>
  <em>Networks of Pendula with Diffusive Interactions</em> <span><a href="https://arxiv.org/pdf/2408.02352" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with R. Bonetto and C. Kuehn) </small>
  </li>

<li>
  <em>Strategic control for a Boltzmann like decision-making model</em> <span><a href="https://arxiv.org/pdf/2405.10915" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with L. Venegas-Pineda, M. Engel, J. Heitzig, M. Eser, and M. Cao)</small><br>
  </li> 

 <li>
  <em>On the analysis of a higher-order Lotka-Volterra model: an application of S-tensors and the polynomial complementarity problem</em> <span><a href="https://arxiv.org/pdf/2405.18333" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with S. Cui, Q, Zhao, G. Zhang, and M. Cao)</small><br>
    

  </li> 

  
  <li>
  <em>On network dynamical systems with a nilpotent singularity</em> <span><a href="https://arxiv.org/pdf/2310.08947" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with C. Kuehn) </small>
  </li>
  
  


 

</ol>


#### Journals:

<ol reversed="">

<li>
  <em>General SIS diffusion process with direct and indirect spreading on a hypergraph </em> <span><a href="https://arxiv.org/pdf/2306.00619" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with S. Cui, F. Liu, L. Liang and M. Cao)<br>
  Automatica, 2025
  </small>
  </li> 


<li>
  <a href="https://pubs.aip.org/aip/cha/article/35/3/033155/3340547/Co-evolutionary-control-of-a-class-of-coupled" target="_blank" rel="noopener noreferrer">
  <em>Co-evolutionary control of a class of coupled mixed-feedback systems</em></a> <span><a href="https://arxiv.org/pdf/2410.19857" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with L. Venegas and M. Cao)<br>
  Chaos, 2025
  </small>
  </li>

<li>
  <a href="https://www.sciencedirect.com/science/article/pii/S2590037425000226" target="_blank" rel="noopener noreferrer">
  <em>Singular bifurcations in a slow-fast modified Leslie-Gower model</em></a> <span><a href="https://arxiv.org/pdf/2411.18059" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with R. Albarrán-García and Martha Alvarez-Ramírez)<br>
  Results in Applied Mathematics, 2025
  </small>
  </li>


<li>
  <a href="https://ieeexplore.ieee.org/abstract/document/10910206" target="_blank" rel="noopener noreferrer">
  <em>On Metzler positive systems on hypergraphs </em></a> <span><a href="https://arxiv.org/pdf/2401.03652" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with S. Cui, G. Zhang, and M. Cao) <br>
  IEEE Transactions on Control of Network Systems, 2025
  </small>
  </li> 

  <li>
   <a href="https://epubs.siam.org/doi/10.1137/24M1651514" target="_blank" rel="noopener noreferrer">
  <em>Ergodicity in planar slow-fast systems through slow relation functions </em></a> <span><a href="https://arxiv.org/pdf/2402.16511" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with R. Huzak and C. Kuehn)<br>
SIAM Journal of Applied Dynamical Systems, 2025
     </small>
  </li> 

  <li>
    <a href="https://www.aimspress.com/article/doi/10.3934/nhm.2024058" target="_blank" rel="noopener noreferrer">
  <em>Nonlinear Diffusion on Networks: Perturbations and Consensus Dynamics
  </em></a> <span><a href="https://arxiv.org/pdf/2206.04442" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with R. Bonetto)<br> 
  Networks and Heterogeneous Media, 2024
  </small>
  </li>  

 <li>
 <a  href="https://iopscience.iop.org/article/10.1088/1361-6544/ad6bde" target="_blank" rel="noopener noreferrer"> <em>The hyperbolic umbilic singularity in fast-slow systems</em></a> <span><a href="https://arxiv.org/pdf/2202.01662" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with C. Kuehn and M. Steinert) <br>
  Nonlinearity, 2024
    </small>
  </li>

 <li>
  <a  href="https://ieeexplore-ieee-org.proxy-ub.rug.nl/document/10540364" target="_blank" rel="noopener noreferrer"><em>On discrete-time polynomial dynamical systems on hypergraphs</em></a> <span><a href="https://arxiv.org/pdf/2403.03416" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with S. Cui, G. Zhang, and M. Cao) <br>
IEEE L-CSS, 2024
</small>
  </li> 

<li>
  <a href="https://epubs.siam.org/doi/full/10.1137/23M1602024" target="_blank" rel="noopener noreferrer"><em>Persistent synchronization of heterogeneous networks with time-dependent linear diffusive coupling</em></a>
    <span><a href="http://arxiv.org/pdf/2305.05747" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span><br>
  <small>(with C. Kuehn and I. Longo) <br>
  SIAM Journal of Applied Dynamical Systems
  </small>
  </li>  

<li>
  <a href="https://www.sciencedirect.com/science/article/pii/S0005109823004673" target="_blank" rel="noopener noreferrer"><em>Discrete-time Layered-network Epidemics Model with Time-varying Transition Rates and Multiple Resources</em></a> 
     <span><a href="https://arxiv.org/pdf/2206.07425" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with S. Cui, F. Liu, and M. Cao) </small><br>
     <small> Automatica, 2024 </small>
  </li> 

<li>
  <a href="https://pubs.aip.org/aip/cha/article-abstract/33/11/113123/2921784/Stable-chimera-states-A-geometric-singular?redirectedFrom=fulltext" target="_blank" rel="noopener noreferrer"><em>Stable Chimera States: A Geometric Singular Perturbation Approach
  </em></a> 
  <span><a href="https://arxiv.org/pdf/2301.07071" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with L. Venegas and M. Cao) <br>
  Chaos, 2023
  </small>
  </li>  

<li>
<a href="https://pubmed.ncbi.nlm.nih.gov/37695774/" target="_blank" rel="noopener noreferrer"><em> Simulation-based Reconstructed Diffusion provides accurate values of mobility in confined spaces, unveiling the effect of aging in Escherichia coli</em></a> 
 <br>
<small>(with L. Mantovanelli, D. S. Linnik, M. Punter, W. M. Smigiel, and B. Poolman) <br>
PLoS Comput Biol. 2023 
</small>
</li>  

<li>  
  <a href="https://projecteuclid.org/journals/bulletin-of-the-belgian-mathematical-society-simon-stevin/volume-29/issue-3/Slow-fast-torus-knots/10.36045/j.bbms.220208.short" target="_blank" rel="noopener noreferrer"><em> Slow-fast torus knots</em></a> 
  <span><a href="http://arxiv.org/pdf/2103.05989" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span> <br>
<small>(with R. Huzak) </small>
<br>
<small>Bull. Belgian Math. Soc., 2022.</small>
</li>
  
  
<li>
<a href="https://link.springer.com/article/10.1007%2Fs00285-021-01664-5" target="_blank" rel="noopener noreferrer"><em> A geometric analysis of the SIRS epidemiological model on a homogeneous network</em></a>
<span> <a href="https://arxiv.org/pdf/2011.02169" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with C. Kuehn, A. Pugliese, and M. Sensi) </small><br>
<small>Journal of Theoretical Biology, 2021.</small>
</li>

<li>
<a href="https://link.springer.com/article/10.1007/s10883-021-09553-2" target="_blank" rel="noopener noreferrer"><em>Controlling canard cycles</em></a>
<span><a href="https://arxiv.org/pdf/1911.11861" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with C. Kuehn) </small><br>
<small>Journal of Dynamical and Control Systems, 2021.</small>
</li>

<li>
<a href="https://www.sciencedirect.com/science/article/pii/S1468121820301383?via%3Dihub" target="_blank" rel="noopener noreferrer"><em>A geometric analysis of the SIR, SIRS and SIRWS epidemiological models</em></a> <br>
<small>(with C. Kuehn,  A. Pugliese and M. Sensi)</small><br>
<small>Nonlinear Analysis: Real World Applications, 2021.</small>
</li>

<li>
<a href="https://www.sciencedirect.com/science/article/pii/S0022247X2030888X" target="_blank" rel="noopener noreferrer"><em>Geometric analysis of Oscillations in the Frzilator model</em></a> <span><a href="https://arxiv.org/pdf/1912.00659" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with H. Tafgvafarad, P. Szmolyan and M. Cao)</small><br>
<small>Journal of Mathematical Analysis and Applications, 2021.</small>
</li>

<li>
<a href="https://epubs.siam.org/doi/abs/10.1137/20M1313611" target="_blank" rel="noopener noreferrer"><em>Extended and symmetric loss of stability for canards in planar fast-slow maps</em></a> <span><a href="https://arxiv.org/pdf/1912.10286" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span><br>
<small>(with M. Engel)</small><br>
<small> SIAM Journal on Applied Dynamical Systems, 2020.</small>
</li>

<li>
<a href="https://link.springer.com/article/10.1007/s00332-020-09634-9" target="_blank" rel="noopener noreferrer">
<em>On Fast–Slow Consensus Networks with a Dynamic Weight</em></a> <span><a href="https://arxiv.org/pdf/1904.02690" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a></span> <br>
<small>(with C. Kuehn)</small><br>
<small>Journal of Nonlinear Science, 2020.</small>
</li>

<li>
<a href="https://doi.org/10.1016/j.automatica.2018.10.008" target="_blank" rel="noopener noreferrer">
<em>Stabilization of a class of slow-fast control systems at non-hyperbolic points</em></a>&nbsp;<br>
<small>(with J. M. A. Scherpen, and D. del Puerto-Flores)</small><br>
<small>Automatica, 2019.</small>
</li>

<li>
<em><a title="improving-region-attraction-2" href="https://ieeexplore.ieee.org/document/8353454/" target="_blank" rel="noopener noreferrer">Improving the region of attraction of a non-hyperbolic point in slow-fast systems with one fast direction</a> </em><br>
<small>(with J. M. A. Scherpen)</small><br>
<small>IEEE Control Systems Letters, 2018.</small>
</li>

<li>
<em><a href="http://rspa.royalsocietypublishing.org/content/474/2209/20170499" target="_blank" rel="noopener noreferrer">Parameter-robustness analysis for a biochemical oscillator model describing the social-behavior transition phase of myxobacteria</a></em><br>
<small>(with H. Tafgvafarad and M. Cao)</small><br>
<small>Proceedings of the Royal Society A, 2018.</small>
</li>

<li>
<em><a href="https://ieeexplore.ieee.org/document/7926328/" target="_blank" rel="noopener noreferrer">Model order reduction and composite control for a class of slow-fast systems around a non-hyperbolic point</a></em> <br>
<small>(with J. M. A. Scherpen)</small><br>
<small>IEEE Control Systems Letters, 2017.</small>
</li>

<li>
<em><a href="https://www.sciencedirect.com/science/article/pii/S0893965917300083" target="_blank" rel="noopener noreferrer">Limit sets within curves where trajectories converge to</a></em><br>
<small>(with P. Ramazi and M. Cao)</small><br>
<small>Applied Mathematics Letters, 2017.</small>
</li>

<li>
<em><a href="http://file.scirp.org/pdf/AM_2016102814120178.pdf" target="_blank" rel="noopener noreferrer">Vibrational Stabilization by Reshaping Arnold Tongues: A Numerical Approach</a></em>
<br><small>(with J. Collado)</small>.<br>
<small>Applied Mathematics, 2016.</small>
</li>

<li>
<em><a href="https://www.sciencedirect.com/science/article/pii/S0022039615005884" target="_blank" rel="noopener noreferrer">Analysis of a slow fast system near a cusp singularity</a></em> <a href="https://arxiv.org/pdf/1506.08679" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a><br>
<small>(with H. W. Broer and R. Roussarie)</small><br>
<small>Journal of Differential Equations, 2016.</small>
</li>

<li>
<em><a href="https://www.sciencedirect.com/science/article/pii/S1631073X15001739"  target="_blank" rel="noopener noreferrer">Formal normal form of Ak slow-fast systems</a></em>&nbsp;<a href="https://arxiv.org/pdf/1504.00122" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a><br>
<small>Comptes Rendus Mathematique, 2015.</small>
</li>

<li>
<em><a href="https://www.sciencedirect.com/science/article/abs/pii/S0096300314015987" target="_blank" rel="noopener noreferrer">Bifurcations of a non-gravitational interaction problem</a></em><br>
<small>(with X. Liu)</small><br>
<small>Applied Mathematics and Computation, 2015.</small>
</li>

<li>
<em><a href="https://www.sciencedirect.com/science/article/pii/S0022039614001739" target="_blank" rel="noopener noreferrer">Polynomial normal forms of Constrained Differential Equations with three parameters</a></em> <a href="https://arxiv.org/pdf/1401.3932" style="color:#000000;"><i class="ai ai-arxiv"></i></a><br>
<small>(with H. W. Broer)</small><br>
<small>Journal of Differential Equations, 2014.</small>
</li>

</ol>



#### Conference proceedings:

<ol reversed>

  <li>
  <span><a rel="noopener noreferrer" href="https://ieeexplore.ieee.org/document/10384227" target="_blank"><em>Species Coexistence and Extinction Resulting from Higher-order Lotka-Volterra Two-Faction Competition
  </em></a></span> <br>
  <small>(with S. Cui, Q. Zhao and M. Cao) </small><br>
  <small> 62nd IEEE Conference on Decision and Control, 2023 </small>
  </li>  
  
  <li>
  <em>A topological perspective on singular canards for critical sets with transverse intersections
  </em> <span><a href="https://arxiv.org/pdf/2304.10822" target="_blank" rel="noopener noreferrer"><i class="ai ai-arxiv"></i></a></span> <br>
  <small>(with R. Bonetto) </small>
  </li>  
  
  <li>
<span><a rel="noopener noreferrer" href="https://www.ams.org/books/conm/775/" target="_blank"><em>A survey on the blow-up method for fast-slow systems</em></a></span> <span style="color:#ff0000;"><span><a href="http://arxiv.org/pdf/1901.01402" target="_blank" rel="noopener noreferrer" style="color:#000000;"><i class="ai ai-arxiv"></i></a><span style="color:#000000;">,<br></span></span></span>
<small>(with C. Kuehn)</small>
<br><small>Contemporary Mathematics, 2021, 775, pp. 115–160.</small>
</li>
  
<li><a title="NonLinear2017" rel="noopener noreferrer" href="https://pure.rug.nl/ws/portalfiles/portal/50534300/07963319.pdf" target="_blank"><em>Nonlinear adaptive stabilization of a class of planar slow-fast systems at a non-hyperbolic point</em></a><br>
<small>(with J. M. A. Scherpen and D. del Puerto-Flores)</small><br><small>American Control Conference 2017.</small></li>
  
<li><a rel="noopener noreferrer" href="https://www.rug.nl/research/portal/files/35515263/0036.pdf" target="_blank"><em>Stabilization of a planar slow-fast system at a non-hyperbolic point</em></a><br>
<small>(with J. M. A. Scherpen)</small><br><small>Mathematical Theory of Networks and Systems 2016.</small></li>
  
<li><a rel="noopener noreferrer" href="https://www.sciencedirect.com/science/article/pii/S2405896316318493"><em>Model order reduction of a flexible-joint robot: a port-Hamiltonian approach</em></a><strong><br></strong>
<small>(with M. Munoz-Arias and J. M. A. Scherpen)</small><br><small>IFAC Symposium on Nonlinear Control Systems 2016.</small></li>
  
<li><em><a rel="noopener noreferrer" href="https://www.researchgate.net/publication/259693995_Estabilizacion_de_redes_complejas_fraccionarias_de_sistemas_de_Lorenz_modificados_y_sistemas_de_Chen?channel=doi&linkId=0f31752d5c1ba09be7000000&showFulltext=true" target="_blank" rel="noreferrer noopener">Estabilización de Redes Complejas Fraccionarias de Sistemas de Lorenz y Sistemas de Chen</a></em><strong><br></strong>
<small>(with R. Martínez-Martínez, J. A. León and G. Fernández-Anaya)</small><br><small>Congreso de la Asociación de México de Control Automático, 2009.</small></li></ol>

#### Editorial work:

<ol>
<li> <a rel="noopener noreferrer" href="https://www.ams.org/books/conm/806/"><em> Topics in Multiple Time Scale Dynamics</em></a><br>
  <small> Maximilian Engel, Hildeberto Jardón-Kojakhmetov, and Cinzia Soresina, Editors <br>
  Contemporary Mathematics<br>
Volume: 806; 2024; 209 pp
  </small>
</li>
</ol>
