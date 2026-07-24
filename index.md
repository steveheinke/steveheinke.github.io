---
layout: default
title: Steve Heinke
---

<style>
  /* Grundlayout */
  header, footer { display: none !important; }
  section { 
    width: 100% !important; 
    max-width: 850px !important; 
    margin: 0 auto !important; 
    padding: 40px 20px !important; 
    position: relative; 
  }

  /* Der Button bekommt float, damit der Text daneben fließen kann, 
     bleibt aber sticky gegenüber der gesamten Sektion */
  .menu-dropdown {
    position: -webkit-sticky;
    position: sticky;
    top: 20px; 
    float: left;
    z-index: 9999;
    margin-right: 25px; /* Abstand zum Text */
    margin-bottom: 10px;
  }

  .menu-button {
    background-color: #000;
    color: white;
    padding: 10px 15px;
    font-size: 0.85em;
    font-weight: bold;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    border-radius: 4px;
    text-transform: uppercase;
    letter-spacing: 1px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.15);
  }

  .menu-content {
    display: none;
    position: absolute;
    left: 0;
    top: 100%;
    background-color: #fff;
    min-width: 220px;
    box-shadow: 0px 8px 16px rgba(0,0,0,0.1);
    border: 1px solid #eee;
    padding: 5px 0;
  }

  .menu-content::before {
    content: "";
    position: absolute;
    top: -10px;
    left: 0;
    right: 0;
    height: 10px;
  }

  .menu-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    font-size: 0.9em;
  }
  .menu-content a:hover { background-color: #f1f1f1; }

  .menu-dropdown:hover .menu-content { display: block; }
  .menu-dropdown.open .menu-content { display: block; }
  .menu-button:focus-visible { outline: 2px solid #fff; outline-offset: -4px; }

  /* Mobile layout */
  @media (max-width: 600px) {
    #about-me table, #about-me tbody, #about-me tr, #about-me td {
      display: block;
      width: 100% !important;
    }
    #about-me td:first-child {
      text-align: center;
      padding-right: 0 !important;
      margin-bottom: 15px;
    }
    #about-me img {
      max-width: 150px !important;
      margin: 0 auto;
    }
    .menu-dropdown {
      float: none !important;
      display: flex;
      justify-content: center;
      margin: 0 0 15px 0 !important;
    }
  }

  /* Back to Top Button */
  .back-to-top {
    position: fixed;
    bottom: 20px;
    left: 20px;
    background-color: #f1f1f1;
    color: #000;
    padding: 8px 12px;
    font-size: 0.75em;
    text-decoration: none;
    border-radius: 4px;
    border: 1px solid #ddd;
    z-index: 9999;
    font-weight: bold;
    opacity: 0.7;
  }
  

  /* Versteckt den Footer (Hosted on GitHub etc.) */
  footer { display: none !important; }
  
  /* Zentriert den Inhalt und nutzt die volle Breite */
  section { 
    width: 100% !important; 
    max-width: 850px !important; 
    margin: 0 auto !important; 
    padding: 40px 20px !important;
  }

  /* Verhindert, dass Markdown-Titel (h1) die Sidebar wieder triggern */
  #title { display: none; }
</style>


<div id="about-me"></div>
<table style="width:100%; border:none; border-collapse:collapse;">
  <tr>
    <td style="width:230px; vertical-align:top; border:none; padding-right:30px;">
      <img src="Steve_Heinke.jpg" alt="Steve Heinke" style="width:100%; max-width:210px; border-radius:2px;">
    </td>
    
    <td style="vertical-align:top; border:none;">
      <h1 style="margin-top:0; padding-top:0; font-size:2.2em; color:#111; border-bottom:none;">Steve Heinke</h1>
      <p style="font-size:1.15em; margin-bottom:15px; line-height:1.4;">
        Senior Researcher at the <strong><a href="https://www.unifr.ch/mobiliarcenter/en/" target="_blank">Mobiliar Center for Resilience</a> </strong>,<br>
       <a href="https://www.unifr.ch/directory/de/people/395662/1b522" target="_blank"> University of Fribourg</a>.
      </p>
       
      <p style="font-size:0.95em; line-height:1.6; color:#444;">
        <strong>Email:</strong> <a href="&#109;&#97;&#105;&#108;&#116;&#111;&#58;&#115;&#116;&#101;&#118;&#101;&#46;&#104;&#101;&#105;&#110;&#107;&#101;&#64;&#117;&#110;&#105;&#102;&#114;&#46;&#99;&#104;">
  &#115;&#116;&#101;&#118;&#101;&#46;&#104;&#101;&#105;&#110;&#107;&#101;&#32;&#91;&#97;&#116;&#93;&#32;&#117;&#110;&#105;&#102;&#114;&#46;&#99;&#104;
</a><br>
        <strong>Links:</strong> <a href="https://orcid.org/0000-0002-9000-5897" target="_blank">ORCID</a> | <a href="https://scholar.google.com/citations?user=odLtrdkAAAAJ&hl=en" target="_blank">Google Scholar</a> | <a href="https://www.linkedin.com/in/steve-heinke-7b9209153/" target="_blank">LinkedIN</a> |<a href="https://osf.io/knbse/" target="_blank">OSF</a>  |  <a href="https://github.com/steveheinke" target="_blank">GitHub</a>
      </p>
    <p style="margin-top: 15px;">
      <a href="CV_steveheinke.pdf" target="_blank" style="
        display: inline-block;
        background-color: #000;
        color: #fff;
        padding: 8px 16px;
        text-decoration: none;
        border-radius: 4px;
        font-size: 0.9em;
        font-weight: bold;
        transition: background-color 0.3s;
      " onmouseover="this.style.backgroundColor='#333'" onmouseout="this.style.backgroundColor='#000'">
        CV
      </a>
    </p>
    </td>
  </tr>
</table>
<div class="menu-dropdown" id="menu-dropdown">
  <button class="menu-button" id="menu-button" aria-haspopup="true" aria-expanded="false" aria-controls="menu-content">
    Menu
      <div class="hamburger">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </button>
    <div class="menu-content" id="menu-content" role="menu">
      <a href="#about-me" role="menuitem">About me</a>
      <a href="#publications" role="menuitem">Publications</a>
      <a href="#working-papers" role="menuitem">Working Papers</a>
      <a href="#research-in-progress-selected" role="menuitem">Research in Progress</a>
      <a href="#professional-services-selected" role="menuitem">Professional Services</a>
      <a href="#teaching-experience" role="menuitem">Teaching Experience</a>
    </div>
</div>
<script>
  (function () {
    var dropdown = document.getElementById('menu-dropdown');
    var button = document.getElementById('menu-button');

    function closeMenu() {
      dropdown.classList.remove('open');
      button.setAttribute('aria-expanded', 'false');
    }

    button.addEventListener('click', function (e) {
      e.stopPropagation();
      var isOpen = dropdown.classList.toggle('open');
      button.setAttribute('aria-expanded', isOpen ? 'true' : 'false');
    });

    document.addEventListener('click', function (e) {
      if (!dropdown.contains(e.target)) closeMenu();
    });

    document.addEventListener('keydown', function (e) {
      if (e.key === 'Escape') closeMenu();
    });

    dropdown.querySelectorAll('.menu-content a').forEach(function (link) {
      link.addEventListener('click', closeMenu);
    });
  })();
</script>
<hr style="margin: 30px 0; border: 0; border-top: 1px solid #eee; clear: both;">



<p style="font-size:1.15em; line-height:1.4; margin: 0;">
    As an experimental economist, I integrate the insights of cognitive psychology into economic decision-making under risk, focusing primarily on applications in finance.
    I study the cognitive drivers—mostly information processing—of people face complex financial decisions.
  <br><br>
  By examining how humans deploy their scarce attentional resources and how they update their beliefs, my work aims to provide a clearer, more unifying framework for the behavioral patterns we observe in the real world, ultimately helping to improve human decision-making.
</p>

<hr style="margin: 30px 0; border: 0; border-top: 1px solid #eee; clear: both;">


### Publications
<ol reversed start="8">
    <li style="margin-top: 15px;">
    <a href="https://academic.oup.com/jcr/advance-article/doi/10.1093/jcr/ucag022/8732294" target="_blank">The Robustness of Mental Accounting Across 21 Countries</a>, with G. Priolo (First Author), E. Rubaltelli (PI), et al., 2026. <em>Accepted at Journal of Consumer Research</em>.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
              <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
                First introduced four decades ago, the influential concept of mental accounting—how 
        people mentally organize, evaluate, and track financial activities—posits that consumers 
        often defy traditional economic rationality, treating money as non-fungible across discrete 
        mental accounts. In this research, we present the first large-scale test of the replicability and 
        generalizability of mental accounting effects, using a sample of 5,589 participants from 21 
        countries. Our results demonstrate that mental accounting effects are replicable, robust, and 
        generalizable. Hierarchical Bayesian meta-analyses revealed a 100% replication rate for all 
        tested scenarios, while unpooled analyses showed a 90.5% replication rate (133/147 effects). 
        Further analysis found that effects observed in higher-income countries may be weaker in 
        lower-income countries. Multidimensional scaling suggested that mental accounting effects 
        vary along three interpretable dimensions that reflect social context (individual vs interactive 
        decisions), decision perspective (deciding for self vs other), and role in price determination 
        (setting vs evaluating prices). Across a diverse population and controlling for multiple 
        factors, we show that consumers make decisions based on mentally-formed accounts that 
        consistently diverge from their objective financial value
      </p>
    </details>
  </li>

  <li>
    <a href="https://academic.oup.com/ej/article-abstract/135/671/2161/8087333" target="_blank">Mental Capabilities, Heterogeneous Trading Behaviour and Performance in an Experimental Asset Market</a>, with Andreas Hefti and Frédéric Schneider, <em>The Economic Journal</em>, 2025.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        We study how variations in two mental capabilities—analytical capability (quantitative reasoning) and mentalising (assessing others’ behaviour)—drive heterogeneity in evaluations of identical information about an asset’s fundamental value and past prices. Our mental framework aligns with regularities observed in experimental asset markets, providing a cognitive basis for heterogeneous trading behaviour. Applied to an experimental market, it predicts that trading, performance and bubble-crash patterns crucially depend on mental capability differences. Traders proficient in both capabilities succeed most, while performance is otherwise non-monotonic in capabilities. Experimental results support these predictions, highlighting the important role of mental capabilities in asset markets.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.sciencedirect.com/science/article/pii/S2214635024000546" target="_blank">Experiences, Demand for Risky Investments, and Implications for Price Dynamics</a>, with Sebastian Olschewski and Jörg Rieskamp, <em>Journal of Behavioral and Experimental Finance</em>, 2025.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Personal experiences can impact investors’ risk taking, and this can explain market phenomena such as time-varying risk premia, asset price bubbles or wage–price spirals. Establishing the link from individual experiences to market outcomes is challenging, as together with experiences, several decision-relevant factors simultaneously change. The present work investigates the impact of prior experiences on subsequent investments in a laboratory experiment without confounds, which allows for the control of various factors that usually are correlated with experience. The results show that high (low) previously experienced outcomes lead to more (less) investment in a risky asset, even in a condition where experiences do not provide new information and should be ignored. A reinforcement learning model captures the observed individual behavior and allows us to explain market price dynamics. The experience effect on risk taking informs behavioral theories of markets and provides a cognitive explanation for trend-following and self-enforcing market dynamics.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.sciencedirect.com/science/article/pii/S0165176524001009" target="_blank">Top–Down and Bottom–Up Information Acquisition: Applications to Financial Markets</a>, <em>Economics Letters</em>, 2024.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
       Recent studies confirm the main prediction of the rational inattention framework that the perceived value of information (top–down) as a key driver of attention. However, these investigations also report stimulus-driven salience effects (bottom–up) that counteract the framework’s predictions. In this manuscript, I propose an extension to the standard rational inattention model by incorporating bottom–up attention processes such as salience-effects through varying information processing costs. Applied to asset pricing with a representative agent a higher information salience generally reduces the cost of information processing (attention) needed for the same level of uncertainty reduction. Due to a substitution effect in the attention allocation across information, an attention-maximizing salience emerges. In general, a higher information salience consistently enhances asset price informativeness.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.tandfonline.com/doi/full/10.1080/15427560.2023.2228549" target="_blank">Degree of Personal Responsibility in Decisions and Investment Abandonment</a>, with Kevin Trutmann and Celine Rudin, <em>Journal of Behavioral Finance</em>, 2023.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        We study how the degree of personal responsibility in prior investment decisions affects the likelihood of changing an investment after experiencing a gain or loss. To this end we conduct a lab-in-the-field experiment with professional participants from the finance and controlling department of a large infrastructure company. Consistent with our hypothesis and prior findings from student samples we observe that lower personal responsibility in the decision is associated with a higher likelihood of changing the investment project after a loss. However, this effect disappears with age, which we interpret as experience in the professional career.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.sciencedirect.com/science/article/pii/S1544612322006195" target="_blank">Take Your Time: Delayed Information and Belief Formation</a>, with Kevin Trutmann and Jörg Rieskamp, <em>Finance Research Letters</em>, 2023.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Investors’ belief-updating is often influenced by factors such as the current investment position and whether information is subjectively favorable. Such motivated beliefs can lead to profit harming decisions. We argue that the degree of involvement with the development of an investment is a driver of such motivated beliefs. In a pre-registered experiment we aim to lower involvement by delaying information and committing participants to a portfolio. We show that this brings participants’ beliefs significantly closer to a Bayesian benchmark. Separating information processing and belief-updating from decisions thus appears as a promising and easy to implement intervention to improve financial decisions.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://link.springer.com/article/10.3758/s13423-021-02053-1" target="_blank">Cognitive Abilities Affect Decision Errors but not Risk Preferences: A Meta-Analysis</a>, with T. Mechera-Ostrovsky, S. Andraszewicz, and J. Rieskamp, <em>Psychonomic Bulletin & Review</em>, 2022.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
When making risky decisions, people should evaluate the consequences and the chances of the outcome occurring. We examine the risk-preference hypothesis, which states that people’s cognitive abilities affect their evaluation of choice options and consequently their risk-taking behavior. We compared the risk-preference hypothesis against a parsimonious error hypothesis, which states that lower cognitive abilities increase decision errors. Increased decision errors can be misinterpreted as more risk-seeking behavior because in most risk-taking tasks, random choice behavior is often misclassified as risk-seeking behavior. We tested these two competing hypotheses against each other with a systematic literature review and a Bayesian meta-analysis summarizing the empirical correlations. Results based on 30 studies and 62 effect sizes revealed no credible association between cognitive abilities and risk aversion. Apparent correlations between cognitive abilities and risk aversion can be explained by biased risk-preference-elicitation tasks, where more errors are misinterpreted as specific risk preferences. In sum, the reported associations between cognitive abilities and risk preferences are spurious and mediated by a misinterpretation of erroneous choice behavior. This result also has general implications for any research area in which treatment effects, such as decreased cognitive attention or motivation, could increase decision errors and be misinterpreted as specific preference changes.        

      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://journals.openedition.org/oeconomia/1104" target="_blank">On the Economics of Superabundant Information and Scarce Attention</a>, with Andreas Hefti, <em>Œconomia</em>, 2015.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        This article provides an introduction to the literature addressing the causes and consequences of limited attention in economics. We present a simple set-theoretic micro-structure describing the allocation of attention, and use this framework to explain the central notions of goal—and stimulus—driven attention mechanisms. After presenting empirical evidence on limited attention from psychology, marketing and internet research, we use our baseline setting to discuss a number of recent contributions featuring some form of limited attention or related phenomena, such as obfuscation.
      </p>
    </details>
  </li>

</ol>
---

### Working Papers 
<ul style="list-style-type: disc; padding-left: 20px;">
  <li>
    <a href="https://www.dropbox.com/scl/fi/p9y26uwnpzkq8licl67mc/ManScie_main.pdf?rlkey=oufmmfq3g4j2kmlu5xdiulqj5&dl=0" target="_blank">Avoiding Bad Risks: How Risk Aversion Is Beneficial for Financial Decision-Making</a>, with S. Maier, A. Ziegler, A. Bagaïni, I. Kooij, S. Nebe, 
N. Sidorenko, K. Trutmann, T. Hens, R. Mata, P. N. Tobler, and J.Rieskamp, 2026. <em></em>
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        hat investor behaviors and characteristics affect performance the most? The existing
literature is diverse and separately associates cognitive abilities, economic preferences, and
neural signals with trading behavior and outcomes. We advance the literature through a
comprehensive comparison of which of these trading behaviors and individual characteristics
matter most for investor performance. Using administrative trading records from 143,000
retail portfolios, linked to experimentally validated measures of cognitive abilities, economic
preferences, and neural signals for a subset, we implement a preregistered Bayesian model
averaging framework to evaluate the full model space without selective reporting. We find
that performance improves not through greater risk-taking, but primarily through consis-
tent avoidance of uncompensated idiosyncratic risk. Across all specifications, risk aver-
sion and self-control emerge as the only robust individual differences associated with better
risk-adjusted performance, primarily because they predict lower exposure to idiosyncratic
risk and more stable trading behavior. Moreover, investors who diversify, trade less and
avoid complex or lottery-like assets substantially reduce idiosyncratic volatility, which ac-
counts for the majority of cross-sectional variation in total portfolio risk. In contrast, widely
cited sources of heterogeneity—including overconfidence, cognitive ability, and theory of
mind—show little or no reliable association with investor trading behaviors and perfor-
mance once model uncertainty is taken into account. These findings clarify the behavioral
foundations of household portfolio choice and provide an empirical basis for a more unified
model of financial decision-making, with clear implications for theory, policy, and investor
support tools.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.biorxiv.org/content/10.1101/2025.08.18.670843v1.full.pdf" target="_blank">The Elusive Neural Signature of Emotion Regulation Capabilities: Evidence from a Large-Scale Consortium</a>, with C. Morawetz (First Author), M. Sicorello (PI), et al., 2026. <em>First revision invited at Nature</em>.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Cognitive reappraisal is a fundamental emotion regulation strategy for mental and
physical well-being, but how its neural mechanisms relate to individual differences remains
poorly understood. In a consortium effort analyzing 40 fMRI datasets (N=2,175), we examined
the relationship between neural activation during reappraisal tasks and three core individual
difference indices of reappraisal capabilities: (1) trait questionnaires, (2) task-based affective
ratings, and (3) amygdala down-regulation. Strikingly, there was no shared overlap across these
three common indices. Only a very weak correlation emerged between amygdala downregulation and task-based affective ratings. Whole-brain analyses revealed no reliable neural
associations with trait questionnaires, and associations with task-based affective ratings fell
outside canonical emotion regulation networks (e.g., prefrontal circuitry). Moreover, amygdala
down-regulation, often interpreted as a stable individual marker, was confounded by personspecific whole-brain responses — a limitation extending to fMRI research beyond the emotion
regulation domain. These findings challenge the assumption that an individual’s prefrontal
activity is a valid indicator of their reappraisal capabilities and suggest that common trait,
behavioral, and neural measures might capture distinct facets of emotion regulation. More
broadly, our results highlight concrete methodological challenges for fMRI research on
individual differences, with implications extending beyond emotion regulation to the
neuroscience of personality, psychopathology, and general well-being. 

      </p>
    </details>
  </li>

  

  <li style="margin-top: 15px;">
    <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7168338" target="_blank">What’s Important Under the Hood? Decomposing Sequential Risk Taking with Feedback through Behavioral Structural Modeling</a>, with M. Marti, S. Olschewski, K. Trutmann, and J. Rieskamp, 2026. <em>Under review at Journal of Finance</em>.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Understanding sequential risk-taking with feedback, and how people deviate from rational benchmarks, has led to many behavioral finance models, without converging on a unifying theory. We propose to first shift the analysis from models to their constituent parts, that is, mechanisms. Second, we systematically compare the most common mechanisms against each other. We find that they all improve predictive accuracy relative to a Bayesian benchmark, but inertia and asymmetric updating explain most of the variation, while risk or loss aversion contributes little once learning is modeled. Better trading performance is associated with greater risk tolerance and near-Bayesian learning rates.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://www.dropbox.com/scl/fi/p3fi1nj35wwdsr722hg4l/Energy_Mix_Choice_under_Cognitive_Constraints_main.pdf?rlkey=z2r6zv3t0s2ri14t82d7rqi68&dl=0" target="_blank">Too Much Choice? A Lab-in-the-Field Experiment on Choice Overload, Cognitive Constraints, and Consumer Welfare in Electricity Contracts Decisions</a>, with S. Olschewski and C. Roux, 2026. <em>Submitted to Journal of Economic Psychology</em>
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Standard economic theory assumes that more options improve welfare, whereas the
choice-overload literature suggests the opposite. Existing evidence is mixed, partly
due to heterogeneous outcome measures, limited experimental control, and a lack of
consensus on underlying mechanisms. We address these challenges in a pre-registered
lab-in-the-field experiment in which 284 German households make incentivized electri-
city contract choices. We contrast (i) choice-set size manipulation with a (ii) cognit-
ive load manipulation, a cognitively well-understood method to experimentally vary
information-processing capacity. While both manipulations lead to more dominated
choices, only cognitive load reduces choice consistency and welfare. In contrast, larger
choice sets lead to more dominated choices simply because they create more oppor-
tunities for random error. Structural estimates from a parsimonious stochastic choice
model motivated by rational inattention confirm that cognitive load increases decision
noise, whereas attribute weights remain stable across conditions. Despite a higher rate
of dominated choices, expanding the option set improves consumer welfare because
participants remain sufficiently consistent to identify better-matching contracts. Our
findings suggest that easing cognitive demands, rather than restricting choice options,
is more effective in improving consumer welfare.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://tinyurl.com/2v4sk3vz" target="_blank">How to Improve the Measurement Quality of Behavioral Tasks Eliciting Risk Preferences?</a>, with O. Schürmann, S. Andraszewicz, and J. Rieskamp, 2026. <em>R&amp;R at Scientific Reports</em>.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        Investigating the risk preferences of decision makers is important for researchers study-
ing decision making and practitioners (i.e., professionals in a variety of fields) who give
advice. Behavioral tasks, which infer a person’s risk preference from their observed risk-
taking behavior with real consequences, should be less susceptible to “cheap talk” than
self-report measures. Additionally, behavioral measures enable for objective characteriza-
tion of risk attributes between different choice options, thus allowing for a more rigorous
investigation compared to subjective surveys relying solely on language-based descriptions.
Finally, the objective nature of behavioral tasks is expected to facilitate generalization to
predict decision-making behavior in new situations. However, they often have low test–
retest reliability, meaning that a decision made at one time may not predict a decision
made at another time within the same task. We suggest that increasing the engagement
with tasks through changes in the choice architecture can improve the test–retest reliabil-
ity of behavioral tasks. We developed a new measure that includes features of self-report
measures, such as providing contextual background narratives for otherwise abstract de-
cisions, including both gains and losses, eliciting multiple decisions, and varying the size
of outcomes. We compared this task with other common behavioral tasks and self-report
measures. We found that the proposed task has a higher test–retest correlation, driven
by observing multiple decisions, providing context, and including gains and losses. We
discuss the challenges of eliciting risk preferences and propose new directions for doing
so.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3935798" target="_blank">Belief Updating and Investment Decisions: The Impact of Good or Bad News Varies with Prior Returns</a>, with K. Trutmann and J. Rieskamp, 2023.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        How individuals form expectations impacts decision-making and economic well-being.
Past research indicates deviations from normative belief updating. Based on cognitive mechanisms we argue that contradictory information relative to the performance of an investment has a larger impact on belief updating than confirmatory information. A pre-registered experimental investment task confirms the resulting hypothesis that for loosing investments belief updates are stronger for positive news than negative; for investment with gains negative news lead to stronger belief updates than positive news. A structural model, using context-sensitive learning-rates in a reinforcement-learning framework, captures this mechanism. The analysis shows that the added complexity by the model improves explanatory power over parsimonious models. This belief-updating pattern drives profit-harming investment decisions. Providing accurate information enhances belief updating and investment choices. Overall, our findings highlight that cognitive mechanisms offer a unifying explanation for regularly observed belief updating patterns and well-known profit-harming behaviors across professional and retail investors.
      </p>
    </details>
  </li>

  <li style="margin-top: 15px;">
    <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3691829" target="_blank">This Time Is Different: On Similarity and Risk Taking After Experienced Gains and Losses</a>, with A. Leuenberger and J. Rieskamp, 2021.
    <details style="margin-top: 5px; cursor: pointer;">
      <summary style="font-size: 0.85em; color: #666;">Abstract</summary>
      <p style="font-size: 0.9em; color: #444; padding: 10px; border-left: 2px solid #eee; margin-top: 5px;">
        How do past experiences of losses or gains affect risk taking? Research shows inconsistent effects of prior outcomes on risk taking. To resolve these inconsistencies we propose a similarity-based theory of how past outcomes could affect decisions: Only past situations similar to the current situation affect decisions. Consistent with the similarity theory, the results of a preregistered experiment show that the less similar a prior decision situation is on task-relevant dimensions, the weaker its effect on the current decision. In sum, incorporating similarity into decision-making theory provides a cognitively based explanation of how past experiences influence current decisions under risk.
      </p>
    </details>
  </li>
</ul>

---
### Research in Progress (selected)

<ul style="list-style-type: none; padding-left: 0;">
  <li>
    <a href="https://financialdecisions.psychologie.unibas.ch/en/" target="_blank">The Foundations of Successful Financial Decision Making</a>: Multi-arm interdisciplinary program combining brokerage data, experimental tasks, and neuroimaging.
  </li>

  <li style="margin-top: 15px;">
    Learn Your Limits, with Doron Cohen and Rudy de Winne. 
  </li>
</ul>

---
### Professional Services (selected)
<ul style="list-style-type: none; padding-left: 0; line-height: 1.6;">
  <li>
    <strong>Editorial Board:</strong> <em>Journal of Behavioral Decision Making</em> (2023–present)
  </li>
  
  <li style="margin-top: 15px;">
    <strong>Ad-hoc Reviewer:</strong> 
    <span style="font-size: 0.95em; color: #444;">
      Finance Research Letters, Information Sciences, Journal of Behavioral and Experimental Finance, 
      Journal of Behavioral Decision Making, Journal of Economic Behavior and Organization, 
      Journal of Economic Psychology, Management Science, Psychological Review, SAGE Open, 
      Spanish Journal of Accounting and Finance.
    </span>
  </li>
</ul>

---
### Teaching Experience
<ul style="list-style-type: none; padding-left: 0; line-height: 1.6;">
  <li>
    <strong>Lectures:</strong>
    <ul style="list-style-type: disc; padding-left: 20px; font-size: 0.95em; color: #444;">
      <li>Economic Psychology (Bachelor, Fall 2024, 2025)</li>
      <li>Risk in Modern Life (Bachelor, Spring 2022–2026)</li>
    </ul>
  </li>

  <li style="margin-top: 15px;">
    <strong>Seminars:</strong>
    <ul style="list-style-type: disc; padding-left: 20px; font-size: 0.95em; color: #444;">
      <li>Behavioral and Experimental Finance (Master, 2017–2023)</li>
      <li>Empirical Projectseminar (Bachelor, 2017, 2018)</li>
      <li>Economic History (Bachelor, Spring 2015)</li>
      <li>Contract Theory and Information Economics (Master, 2011, 2012)</li>
      <li>Writing & Presentation Skills for Economists (Bachelor, 2007, 2008)</li>
    </ul>
  </li>

  <li style="margin-top: 15px;">
    <strong>Tutorials:</strong>
    <ul style="list-style-type: disc; padding-left: 20px; font-size: 0.95em; color: #444;">
      <li>Microeconomics I (Bachelor, 2014, 2015)</li>
      <li>Contract and Information Economics (Bachelor, 2011–2013)</li>
      <li>Macroeconomics (Bachelor, 2009, 2010)</li>
    </ul>
  </li>

  <li style="margin-top: 15px;">
    <strong>Supervision:</strong> 
    <span style="font-size: 0.95em; color: #444;">Master Theses (8x), Bachelor Theses (34x)</span>
  </li>
</ul>


---
### Academic Appointments
* **2024–** Senior Researcher, University of Fribourg
* **2017–2024** Post-Doc, University of Basel
* **2011–2017** Research & Teaching Assistant, University of Zurich

### Education
* **PhD in Economics**: University of Zurich (2016)
* **MA in Economics**: University of Munich (2009)
* **BA Philosophy & Economics**: University of Bayreuth (2008)

---


