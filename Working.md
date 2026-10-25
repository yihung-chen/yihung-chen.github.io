---
layout: page
title: "Working Papers"
permalink: /working-papers/
---

<style>
/* =========================================================
   1. ARTICLE TITLE AND TEXT STYLES
   調整論文標題、研究領域、作者及摘要的外觀
   ========================================================= */

/* 論文標題：字體大小、行距、上下間距及粗細 */
.working-papers h2 {
  font-size: 1.35rem;
  line-height: 1.45;
  margin-top: 2rem;
  margin-bottom: 0.35rem;
  font-weight: 600;
}

/* 論文的研究領域標籤 */
.working-papers .research-fields {
  font-size: 0.9rem;
  color: #777;
  margin: 0.25rem 0 0.5rem;
}

/* 共同作者文字 */
.working-papers .coauthor {
  font-size: 0.92rem;
  margin-top: -0.15rem;
  margin-bottom: 0.35rem;
}

/* 論文之間的分隔線 */
.working-papers hr {
  margin: 1.4rem 0;
  border: 0;
  border-top: 1px solid #e5e5e5;
}


/* =========================================================
   2. ABSTRACT DROPDOWN
   控制摘要展開／收合的外觀
   ========================================================= */

/* 摘要區塊的上下間距 */
.working-papers details {
  margin: 0.4rem 0 1.2rem;
}

/* Show Abstract 按鈕的外觀 */
.working-papers details summary {
  cursor: pointer;
  color: #555;
  font-size: 0.9rem;
  list-style: none;
  display: inline-block;
  border-bottom: 1px solid #ccc;
  padding-bottom: 2px;
}

/* 隱藏部分瀏覽器預設的三角形圖示 */
.working-papers details summary::-webkit-details-marker {
  display: none;
}

/* 摘要收合時顯示 + */
.working-papers details summary::after {
  content: " +";
  color: #999;
}

/* 摘要展開時改為 − */
.working-papers details[open] summary::after {
  content: " −";
}

/* 摘要文字的行距與對齊 */
.working-papers details p {
  text-align: justify;
  text-justify: inter-word;
  line-height: 1.75;
  margin-top: 0.8rem;
  margin-bottom: 0.8rem;
}


/* =========================================================
   3. RESEARCH FILTER BUTTONS
   控制頁面最上方的研究領域篩選按鈕
   ========================================================= */

/* 篩選按鈕的排列方式及與論文列表的距離 */
.working-papers .research-filters {
  margin: 1.25rem 0 2rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

/* 所有篩選按鈕的基本樣式 */
.working-papers .research-filters button {
  cursor: pointer;
  padding: 0.35rem 0.8rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  background: transparent;
  color: inherit;
  font: inherit;
  font-size: 0.85rem;
  transition: background-color 0.15s ease,
              color 0.15s ease,
              border-color 0.15s ease;
}

/* 滑鼠移到按鈕上時的效果 */
.working-papers .research-filters button:hover {
  border-color: #777;
}

/* 目前選中的篩選按鈕
   可修改 background 和 border-color 改變按鈕顏色 */
.working-papers .research-filters button.active {
  background: #555;
  border-color: #555;
  color: #fff;
}

/* 被篩選隱藏的論文不佔據版面 */
.working-papers .paper-item[hidden] {
  display: none !important;
}

/* 顯示目前篩選結果數量的文字 */
.working-papers .filter-status {
  font-size: 0.85rem;
  color: #777;
  margin: -1rem 0 1.5rem;
}
</style>


<div class="working-papers">

<!-- =======================================================
     4. FILTER BAR
     新增、刪除或修改研究領域篩選按鈕的位置

     data-filter 是分類代碼，必須與下方論文的 data-tags
     完全一致。All 是顯示全部論文的特殊選項。
     ======================================================= -->

<p>Filter by research area:</p>

<div class="research-filters" aria-label="Filter papers by research area">

  <!-- 顯示全部論文；預設為選取狀態 -->
  <button type="button"
          class="active"
          data-filter="all"
          aria-pressed="true">All</button>

  <!-- 政黨政治 -->
  <button type="button"
          data-filter="political-parties"
          aria-pressed="false">Political Parties</button>

  <!-- 選舉政治 -->
  <button type="button"
          data-filter="electoral-politics"
          aria-pressed="false">Electoral Politics</button>

  <!-- 政治行為 -->
  <button type="button"
          data-filter="political-behavior"
          aria-pressed="false">Political Behavior</button>

  <!-- 公眾意見 -->
  <button type="button"
          data-filter="public-opinion"
          aria-pressed="false">Public Opinion</button>

  <!-- 政治經濟 -->
  <button type="button"
          data-filter="political-economy"
          aria-pressed="false">Political Economy</button>

  <!-- 外國經濟脅迫 -->
  <button type="button"
          data-filter="foreign-economic-coercion"
          aria-pressed="false">Foreign Economic Coercion</button>

</div>

<!-- 篩選結果數量；由 JavaScript 自動更新 -->
<p class="filter-status" id="filter-status" aria-live="polite">
  Showing all 5 papers
</p>


<!-- =======================================================
     5. PAPER 1
     新增論文時，可複製整個 article 區塊。
     data-tags 決定這篇論文會出現在哪些篩選結果中。
     多個分類以空格分隔，不要使用逗號。
     ======================================================= -->

<article class="paper-item"
         data-tags="political-parties electoral-politics">

<h2>A Party-Made Ladder: Intra-Party Nomination Rules and the Institutionalization of Level-Hopping</h2>

<!-- 文章下方顯示的研究領域標籤 -->
<p class="research-fields"><em>Political Parties · Electoral Politics</em></p>

<!-- 摘要內容：修改摘要時，只需要更改這個區塊 -->
<details>
<summary>Show Abstract</summary>

<p>When legislators can run for executive office without giving up their seats, what restrains cross-level ambition, and why do voters accept it? This article argues that, where parties control nominations, intra-party rules both ration access to higher office and legitimate those who obtain it. Because a mid-term candidacy shifts its risks from the individual to the party, the party decides who may climb, where, and by which route. Evidence from Taiwan, combining original data on all legislators elected 2008–2020, a survey experiment, and elite interviews, supports this argument. Legislators seek executive office almost only in races their party leaves open, party rules shape where they compete in primaries, and those with a strong existing base are drafted. Voters judge such moves through partisanship: co-partisans tolerate them, out-partisans condemn them, and primaries raise support only among co-partisans. Accountability for mid-term departures thus shifts from constituents to parties.</p>

</details>

<hr>
</article>


<!-- =======================================================
     6. PAPER 2
     若修改研究領域，請同步更新：
     (1) data-tags
     (2) research-fields 顯示文字
     ======================================================= -->

<article class="paper-item"
         data-tags="political-behavior electoral-politics">

<h2>Ambition, Horizontal Coordination, and the Reverse Coattail Effect: Evidence from Taiwan</h2>

<p class="research-fields"><em>Political Behavior · Electoral Politics</em></p>

<details>
<summary>Show Abstract</summary>

<p>How do multiple ambitious local elites within the same party coordinate—or fail to coordinate—when mobilizing for a higher-tier objective? The reverse coattail literature has developed largely within single-member district contexts, leaving the horizontal interdependence among co-partisans in multi-member districts underexplored. This study argues that whether multiple ambitious local elites amplify or undermine mobilization depends on the excludability of the party’s electoral objective: non-excludable defensive goals invite free-riding, whereas excludable offensive prizes fuel a tournament that escalates with peer density. Using the 2025 Taiwan legislative recall as a quasi-experiment, propensity score matching reveals a behavioral asymmetry. Defending star councilors produce a protective effect that fails to scale under multi-agent crowding, while challenging star agents suppress the same margin, amplifying as more challengers compete. The study offers a portable identification strategy for contexts combining multi-member lower-tier institutions, single-member upper-tier objectives, and non-concurrent electoral cycles.</p>

</details>

<hr>
</article>


<!-- =======================================================
     7. PAPER 3
     共同作者請填在 coauthor 段落。
     沒有共同作者時，可刪除整個 coauthor 段落。
     ======================================================= -->

<article class="paper-item"
         data-tags="political-behavior public-opinion">

<h2>When the Signal Breaks: Origin-Country Elite Conflict and Vaccine Acceptance in Taiwan</h2>

<p class="coauthor">(with Jason Kuo)</p>

<p class="research-fields"><em>Political Behavior · Public Opinion</em></p>

<details>
<summary>Show Abstract</summary>

<p>When a country’s own political leadership publicly contests the credibility of its pharmaceutical exports, does the country-of-origin (COO) premium that makes those products internationally preferred erode? Existing research consistently finds that vaccine origin countries shape public willingness to receive vaccination, with American-origin vaccines occupying a particularly favorable position in public evaluations. Yet this literature rests on an unexamined assumption that origin-country credibility is stable and internally consistent. The political developments of early 2025 placed this assumption under direct pressure. We examine how U.S. elite conflict over mRNA technology affects Taiwanese support and vaccination intention for U.S.-developed mRNA vaccines, arguing that political conflict within the origin country attenuates the COO premium and introduces a previously overlooked source of vaccination hesitancy among foreign publics.</p>

<p>Across two pre-registered survey experiments conducted in Taiwan, we find that both an administrative opposition message and a contested debate juxtaposing opposing elite views significantly reduced procurement support and vaccination intention, whereas affirming information had only a marginal effect. Causal mediation analyses reveal distinct mechanisms. Administrative opposition operated through perceived protection, while contested debate operated through perceived safety. These findings show the COO premium is politically contingent; elite conflict in the origin country can erode an advantage long treated as fixed, translating domestic disputes into consequences for global health attitudes.</p>

</details>

<hr>
</article>


<!-- =======================================================
     8. PAPER 4
     本文同時屬於政治行為、公眾意見、政治經濟、
     外國經濟脅迫，因此 data-tags 包含四個分類。
     ======================================================= -->

<article class="paper-item"
         data-tags="political-behavior public-opinion political-economy foreign-economic-coercion">

<h2>Backlash to Weaponized Non-Tariff Trade Barriers: Evidence from the Chinese Mango Ban in the 2024 Taiwan Presidential Election</h2>

<p class="coauthor">(with Jason Kuo)</p>

<p class="research-fields"><em>Political Behavior · Public Opinion · Political Economy · Foreign Economic Coercion</em></p>

<details>
<summary>Show Abstract</summary>

<p>On August 21, 2023, the mainland Chinese government unilaterally declared a ban on the sale of Taiwanese mangoes to mainland China, citing quarantine non-compliance as the reason. The incumbent Democratic Progressive Party (DPP) believed that this incident was a malicious attempt by the mainland Chinese government to intervene in Taiwan's presidential election through foreign economic coercion. However, the existing literature has not assessed the electoral impact of the weaponized non-tariff barriers (NTBs) to trade as a Chinese coercive foreign economic policy intervention in a small open economy, such as Taiwan. To fill this gap, this study systematically collected administrative data from 368 townships in Taiwan and used a difference-in-differences research design to estimate the average causal effect of the Chinese mango ban as a trade coercion through NTBs on the 2024 Taiwanese presidential election. This study found that the Chinese mango ban significantly increased political support for the incumbent DPP vote share in the presidential election by 2.6 percentage points in the nine southern townships materially hurt by the ban. In other words, the Chinese use of NTBs as a foreign policy tool of economic coercion backfired, causing a political backlash among citizens residing in the neighborhoods of the coerced Taiwanese mango farmers. This study also attributed the pattern to the strategic prevention of the anticipated economic pain of export diversification by the ruling DPP government. Despite the increasing use of foreign trade policy for economic coercion by China and the other great powers around the world in recent years, this study reveals serious limitations of foreign trade coercion to intervene in democratic elections.</p>

</details>

<hr>
</article>


<!-- =======================================================
     9. PAPER 5
     若新增或修改研究分類，請同步修改 data-tags
     和 research-fields。
     ======================================================= -->

<article class="paper-item"
         data-tags="political-behavior public-opinion political-economy">

<h2>From Rally to Rupture: Trump’s Tariffs in Taiwan</h2>

<p class="coauthor">(with Jason Kuo)</p>

<p class="research-fields"><em>Political Behavior · Public Opinion · Political Economy</em></p>

<details>
<summary>Show Abstract</summary>

<p>How does explicit economic pressure by a security patron affect domestic politics in a dependent ally? We examine Taiwan’s response to Trump’s “Liberation Day” tariffs and the ensuing U.S.–Taiwan Agreement on Reciprocal Trade (ART). Although sudden, dramatic, international events are expected to induce rally-around-the-flag effects, we argue that economic pressure from a security patron need not produce a rally but instead deepens preexisting partisan cleavages by weakening public confidence in the incumbent and favorability toward the patron among opposition but not ruling party supporters. We conduct two original surveys to test this claim. A survey, fielded after the first reduction in the negotiated tariffs in August 2025, finds no rally. Instead, respondents viewed the tariffs as harmful to the national economy, were dissatisfied with the trade negotiations, and expressed limited confidence in the government.</p>

<p>Responses also significantly diverged by partisan camp. We then exploit the ART’s unexpected January 2026 announcement during our follow-up survey to identify causal effects of the ART concession. Among opposition supporters, U.S. favorability fell by 16 percent of its range immediately after the announcement; yet ruling-party supporters showed no significant change. Aggregated interrupted time-series analyses of the ART concession further show that this erosion in U.S. favorability among opposition supporters remained stable throughout the observed post-announcement period. Our results broadly suggest that economic pressure from a security patron, the U.S. in this case, cannot rally a dependent ally’s public behind its incumbent. More generally, it can deepen domestic partisan divisions and erode cross-partisan support for the security patron.</p>

</details>

<hr>
</article>

</div>


<!-- =======================================================
     10. FILTER FUNCTION
     控制篩選按鈕的互動邏輯。

     新增分類按鈕時，必須確保：
     1. 按鈕的 data-filter 使用分類代碼。
     2. 論文的 data-tags 包含相同的分類代碼。
     3. 分類代碼使用英文小寫與連字號。
     4. All 顯示所有論文。
     ======================================================= -->

<script>
document.addEventListener("DOMContentLoaded", function () {

  // 取得論文頁面容器；其他頁面的元素不受影響
  const container = document.querySelector(".working-papers");
  if (!container) return;

  // 取得篩選按鈕、論文及結果數量文字
  const buttons = container.querySelectorAll(".research-filters button");
  const papers = container.querySelectorAll(".paper-item");
  const status = container.querySelector("#filter-status");

  // 執行篩選：只顯示包含指定分類的論文
  function applyFilter(filter) {
    let visibleCount = 0;

    papers.forEach(function (paper) {

      // 以空格分隔每篇論文的分類代碼
      const tags = (paper.dataset.tags || "")
        .split(/\s+/)
        .filter(Boolean);

      // All 顯示全部；其他按鈕依分類代碼篩選
      const visible =
        filter === "all" || tags.includes(filter);

      paper.hidden = !visible;

      if (visible) visibleCount++;
    });

    // 更新按鈕的選取狀態
    buttons.forEach(function (button) {
      const active = button.dataset.filter === filter;

      button.classList.toggle("active", active);
      button.setAttribute("aria-pressed", String(active));
    });

    // 更新目前的篩選結果說明
    const selectedButton = Array.from(buttons).find(
      button => button.dataset.filter === filter
    );

    const label = selectedButton
      ? selectedButton.textContent.trim()
      : "All";

    if (status) {
      status.textContent = filter === "all"
        ? "Showing all " + visibleCount + " papers"
        : "Showing " + visibleCount + " papers in " + label;
    }
  }

  // 為每個按鈕加入點擊事件
  buttons.forEach(function (button) {
    button.addEventListener("click", function () {
      applyFilter(button.dataset.filter);
    });
  });

});
</script>
