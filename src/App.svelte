



<script>
	import Svelvet from "svelvetcake";


	
	const initialNodes = [
	  {
		id: 1,
		position: { x: 100, y: 20 },
		data: { html: ` <video width="480" height="360" src="https://i.imgur.com/VoBl9wh.mp4" controls autoplay loop></video>` },
		// data: {html: `<h1> WE DEM BOIZ MONSTARZ </h1>` },
		width:  330,
		height: 220,
		bgColor: "white",
	  },
	  {
		id: 2,
		position: { x: 0, y: 330 },
		data: { label: "bezier" },
		width: 70,
		childNodes: [5],
		height: 40,
		bgColor: "white",

	  },
	  {
		id: 3,
		position: { x: 240, y: 510 },
		data: { html: `<button> Click Me! </button>` },
		width: 100,
		height: 40,
		bgColor: "blue",

	  },
	  {
		id: 4,
		position: { x: 670, y: 330 },
		data: { html: `<label for="lname">Message Box:</label>
<input type="text" id="lname" name="lname" form="form1">` },
		width: 200,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 5,
		position: { x: 30, y: 510 },
		data: { label: "no handle" },
		width: 80,
		parentNode: 2,
		height: 40,
		bgColor: "white",

	  },
	  {
		id: 6,
		position: { x: 450, y: 480 },
		data: { html: ` <ul><li>Coffee</li><li>Tea</li><li>Milk</li></ul> ` },
		width: 100,
		height: 50,
		bgColor: "white",

	  }
	];

	const initialEdges = [
	  { id: "e1-2", source: 1, target: 2, type: "bezier" },
	  { id: "e1-3", source: 1, target: 3, type: "straight" },
	  {
		id: "e1-4",
		source: 1,
		target: 4,
		type: "bezier",
		animate: true,
		label: "labeled"
	  },
	  {
		id: "e1-5",
		source: 1,
		target: 5,
		type: "bezier",
		noHandle: true
	  },
	  {
		id: "e1-6",
		source: 1,
		target: 6,
		type: "bezier",
		arrow: true
	  }
	];
</script>


<Svelvet nodes={initialNodes} movement={true} width={1200} height={900}  edges={initialEdges} background/>

<!-- <script>
	import Svelvet from "svelvetcake";

	const initialNodes = [
	  {
		id: 1,
		position: { x: 100, y: 20 },
		data: { label: "Input Node" },
		width: 175,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 2,
		position: { x: 10, y: 150 },
		data: { label: "bezier" },
		width: 70,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 3,
		position: { x: 152, y: 150 },
		data: { label: "straight" },
		width: 70,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 4,
		position: { x: 294, y: 150 },
		data: { label: "animated/labeled" },
		width: 140,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 5,
		position: { x: 80, y: 225 },
		data: { label: "no handle" },
		width: 80,
		height: 40,
		bgColor: "white"
	  },
	  {
		id: 6,
		position: { x: 250, y: 225 },
		data: { label: "arrow handle" },
		width: 100,
		height: 40,
		bgColor: "white"
	  }
	];

	const initialEdges = [
	  { id: "e1-2", source: 1, target: 2, type: "bezier" },
	  { id: "e1-3", source: 1, target: 3, type: "straight" },
	  {
		id: "e1-4",
		source: 1,
		target: 4,
		type: "bezier",
		animate: true,
		label: "labeled"
	  },
	  {
		id: "e1-5",
		source: 1,
		target: 5,
		type: "bezier",
		noHandle: true
	  },
	  {
		id: "e1-6",
		source: 1,
		target: 6,
		type: "bezier",
		arrow: true
	  }
	];
</script>

<Svelvet nodes={initialNodes} width={900} snap={true} height={900} edges={initialEdges} background/> -->