<script lang="ts">
</script>

<h1>Totally fake survey results of smiley preferences.</h1>
<figure aria-hidden="true">
	<div class="graph">
		<span class="graphRowLabel">100</span>
		<span class="graphRowLabel">90</span>
		<span class="graphRowLabel">80</span>
		<span class="graphRowLabel">70</span>
		<span class="graphRowLabel">60</span>
		<span class="graphRowLabel">50</span>
		<span class="graphRowLabel">40</span>
		<span class="graphRowLabel">30</span>
		<span class="graphRowLabel">20</span>
		<span class="graphRowLabel">10</span>
		<div class="graphBar" />
		<div class="graphBar" />
		<div class="graphBar" />
		<div class="graphBar" />
		<div class="graphBar" />
		<span><sup>Y </sup>&frasl;<sub> X</sub></span>
		<span class="graphColumnLabel">π</span>
		<span class="graphColumnLabel">π</span>
		<span class="graphColumnLabel">βΊοΈ</span>
		<span class="graphColumnLabel">π</span>
		<span class="graphColumnLabel">π</span>
	</div>
	<figcaption>Made with CSS Grid π</figcaption>
</figure>
<span class="screenreader-text"
	>Smiling face with squinting eyes: 10%, grinning face with squinting eyes: 65%, smiling face: 52%,
	grinning face with smiling eyes: 100%, and grinning face: 92%.</span
>

<style lang="scss">
	.graph {
  display: grid;
  grid: repeat(10, auto) max-content / max-content repeat(5, auto);
  height: 100%;
}
/* graph bars */
.graphBar {
  grid-row: 1 / -2;
  border-radius: 0 0 50% 50% / 0 0 10px 10px;
  background: palegoldenrod
    linear-gradient(to top, gold var(--h), transparent var(--h));
  justify-self: center;
  width: 45px;
  height: 100%;
  box-shadow: 0 0 3px lightgrey;
}
.graphBar:nth-of-type(1) {
  grid-column: 2;
  --h: 10%;
}
.graphBar:nth-of-type(2) {
  grid-column: 3;
  --h: 65%;
}
.graphBar:nth-of-type(3) {
  grid-column: 4;
  --h: 52%;
}
.graphBar:nth-of-type(4) {
  grid-column: 5;
  --h: 100%;
}
.graphBar:nth-of-type(5) {
  grid-column: 6;
  --h: 92%;
}
/* graph bar edges */
.graphBar::before,
.graphBar::after {
  display: block;
  content: "";
  height: 20px;
  border-radius: 50% / 10px;
}
.graphBar::before {
  margin-top: -10px;
  background-color: darkkhaki;
}
.graphBar::after {
  background-color: darkgoldenrod;
  position: relative;
  top: calc(100% - var(--h) - 20px);
}
/* graph  labels */
.graphRowLabel {
  margin-top: -0.5em;
}
.graphColumnLabel {
  justify-self: center;
  margin-top: 6px;
  text-shadow: 0 0 2px palegoldenrod;
  font-size: 14pt;
}
.graphRowLabel::after {
  display: inline-block;
  content: "\2000\2000\2014";
}
.graphRowLabel:nth-of-type(1)::after {
  content: "\2000\2014";
}
body {
  font-family: "crimson text";
  background: linear-gradient(to top right, dodgerblue, deepskyblue);
  color: cornsilk;
  height: 100vh;
  font-weight: bold;
  overflow: hidden;
  text-shadow: 0 0 1px grey;
}
figure {
  width: 98vw;
  max-width: 600px;
  height: 420px;
  margin: 60px auto auto auto;
}
figcaption {
  text-align: center;
  margin-top: 30px;
}
h1 {
  text-align: center;
  font-size: 14pt;
  margin-bottom: 0;
}
.screenreader-text {
  display: block;
  height: 1px;
  width: 1px;
  overflow: hidden;
}
</style>
