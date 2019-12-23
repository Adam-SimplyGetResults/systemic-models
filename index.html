<html lang="en">
<head>
<title>Systemic Model</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<script src="//unpkg.com/3d-force-graph"></script>
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

/* Style the side navigation */
.sidenav {
  height: 100vh;
  width: 15vw;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #ffffff;
  overflow-x: hidden;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 1vh;
}

/* Change color on hover */
.sidenav a:hover {
  background-color: #ffffff;
  color: black;
}

/* Style the content */
.content {
  margin-left: 200px;
  padding-left: 20px;
  overflow: auto;
}

/*the container must be positioned relative:*/
.autocomplete {
  position: relative;
  display: inline-block;
  width: 15vw;
}

input {
  border: 1px solid transparent;
  background-color: #f1f1f1;
  padding: 10px;
  font-size: 16px;
}

input[type=text] {
  background-color: #f1f1f1;
  width: 15vw;
  resize: both;
}

button[type=button] {
  background-color: DodgerBlue;
  color: #ffffff;
  cursor: pointer;
  position: relative;
  font-size: 16px;
  padding: 10px;
  width: 100px;
  margin-top: 10px;
}


.autocomplete-items {
  position: absolute;
  border: 1px solid #d4d4d4;
  border-bottom: none;
  border-top: none;
  z-index: 99;
  /*position the autocomplete items to be the same width as the container:*/
  top: 100%;
  left: 0;
  right: 0;
  width: 15vw;
}

.autocomplete-items div {
  padding: 10px;
  cursor: pointer;
  background-color: #fff;
  border-bottom: 1px solid #d4d4d4;
}

/*when hovering an item:*/
.autocomplete-items div:hover {
  background-color: #e9e9e9;
}

/*when navigating through the items using the arrow keys:*/
.autocomplete-active {
  background-color: DodgerBlue !important;
  color: #ffffff;
}


</style>
</head>
<body onresize="windowResize()">

<div class="sidenav">

    <!--Make sure the form has the autocomplete function switched off:-->
  <form autocomplete="off">
    <div class="autocomplete" style="width:300px;">
      <input id="myInput" type="text" name="myInputText" placeholder="Search for a node here...">
    </div>
  </form>
    <div>
      <button type="button" class="findButton" onclick="onSearchSubmit()">Search</button>
    </div>

    <div>
    <p id="selectedNodeP">No node selected</p>
    </div>

    <div>
      <button type="button" class="showInfluencers" onclick="colourInfluencers()">Show influencers</button>
      <button type="button" class="showInfluenced"  onclick="colourInfluenced()">Show influenced</button>
    </div>

    <div>
      <button type="button" class="showInfluencers" onclick="Graph.nodeColor(node => (simplyColours[node.group]))">Reset</button>
    </div>

</div>

<div id="3d-graph" class="content"></div>

<script src='./search-autocomplete.js'></script>

<script>
const gData = {
              "nodes": [
                {"id": "Profit","val": "3","group": "0" ,"size":10},
                {"id": "Revenue","val": "1","group": "1" },
                {"id": "Cost","val": "1","group": "1" },
                {"id": "Customer Satisfaction","val": "1","group": "2" },
                {"id": "Sales","val": "1","group": "2" },
                {"id": "Share Price","val": "1","group": "2" },
                {"id": "Dividend","val": "1","group": "2" },
                {"id": "Market Cap","val": "1","group": "2" },
                {"id": "CAPEX","val": "1","group": "2" },
                {"id": "OPEX","val": "1","group": "2" },
                {"id": "Other OPEX","val": "1","group": "2" },
                {"id": "Asset Value","val": "1","group": "3" },
                {"id": "Depreciation","val": "1","group": "3" },
                {"id": "People Cost","val": "1","group": "3" },
                {"id": "Compensation","val": "1","group": "4" },
                {"id": "Attrition","val": "1","group": "4" },
                {"id": "Recruitment","val": "1","group": "4" },
                {"id": "Workforce Mix","val": "1","group": "4" },
                {"id": "Organisational Efficiency","val": "1","group": "4" },
                {"id": "Performance","val": "1","group": "4" },
                {"id": "Capability","val": "1","group": "5" },
                {"id": "Training/Learning","val": "1","group": "5" },
                {"id": "Culture","val": "1","group": "5" },
                {"id": "Engagement","val": "1","group": "5" },
                {"id": "HiPo","val": "1","group": "5" }
              ],
              "links": [
                {"source": "Revenue","target": "Profit" },
                {"source": "Cost","target": "Profit" },
                {"source": "Sales","target": "Revenue" },
                {"source": "Customer Satisfaction","target": "Profit" },
                {"source": "Profit","target": "Share Price" },
                {"source": "Profit","target": "Dividend" },
                {"source": "Share Price","target": "Market Cap" },
                {"source": "CAPEX","target": "Cost" },
                {"source": "OPEX","target": "Cost" },
                {"source": "CAPEX","target": "Asset Value" },
                {"source": "Depreciation","target": "Profit" },
                {"source": "Depreciation","target": "Asset Value" },
                {"source": "People Cost","target": "OPEX" },
                {"source": "Other OPEX","target": "OPEX" },
                {"source": "Compensation","target": "People Cost" },
                {"source": "Recruitment","target": "People Cost" },
                {"source": "Recruitment","target": "Organisational Efficiency" },
                {"source": "Recruitment","target": "Capability" },
                {"source": "Capability","target": "Performance" },
                {"source": "Performance","target": "Sales" },
                {"source": "Recruitment","target": "Workforce Mix" },
                {"source": "Attrition","target": "Recruitment" },
                {"source": "Compensation","target": "Performance" },
                {"source": "Performance","target": "Compensation" },
                {"source": "Workforce Mix","target": "Organisational Efficiency" },
                {"source": "Engagement","target": "Performance" },
                {"source": "Culture","target": "Engagement" },
                {"source": "Training/Learning","target": "Capability" },
                {"source": "Recruitment","target": "HiPo" },
                {"source": "HiPo","target": "Performance" },
                {"source": "Organisational Efficiency","target": "People Cost" }
              ]
          };

nodes=[]
for(const item of gData.nodes){
  nodes.push(item.id)
}


/*initiate the autocomplete function on the "myInput" element, and pass along the nodes array as possible autocomplete values:*/
autocomplete(document.getElementById("myInput"), nodes);

/*##############################################################################


###############################################################################*/

const simplyColours = [10472261,7191373,4150947,8204431,11353235,14034486,14842669,15383580]
const simplyHexColours = simplyColours.map((x)=>{
    let y=x.toString(16)
    let z="#"+y
    return z
  })

const hiddenColour=16645886;

//Display the graph
const Graph = ForceGraph3D()
  (document.getElementById('3d-graph'))
    .nodeColor(node => (simplyColours[node.group]))
    .nodeLabel(node => "<font size=\"6\", color=\"black\">"+ node.id+"</font>")
    .linkOpacity(0.5)
    .nodeOpacity(1)
    .nodeRelSize(8)
    //.linkDirectionalParticles(10)
    .linkDirectionalParticleWidth(2)
    .linkWidth(3)
    //.linkAutoColorBy(d => gData.nodes[d.source].group)
    .backgroundColor('#ffffff')
    .width(window.innerWidth*0.85)
    .height(window.innerHeight)
    .showNavInfo(false)
    .graphData(gData);

/*##############################################################################


###############################################################################*/

var selectedNodeId;
var searchedNodeId;

function onSearchSubmit(){
  var searchTerm = document.getElementById('myInput').value;
  //Check the gData object to see if it contains the term being searched for
  try{
    searchedNodeId=gData.nodes.find(node => node.id.toLowerCase()===searchTerm.toLowerCase()).id;
    console.log(searchedNodeId)
  }
  catch(err){
    alert("No valid search input")
  }
  //Change the html message to show the node that has been searched for as selected
  if(searchedNodeId){
    selectedNodeId=searchedNodeId;
    document.getElementById('selectedNodeP').innerHTML = `Node Selcted: ${selectedNodeId}`
  }

  //Colour the node that you have selected
  Graph.nodeColor(node=> selectedNodeId.indexOf(node.id) ? hiddenColour : simplyColours[node.group])

  //Move the camera to view the node you want
  moveToNode(selectedNodeId);
}

function colourInfluencers(){
  showInfluencers=true;
  showInfluenced=false;
  colourNeighbours();
}

function colourInfluenced(){
  showInfluencers=false;
  showInfluenced=true;
  colourNeighbours();
}

function colourNeighbours(){
    //for now, colour the whole graph grey
    //Graph.nodeColor(node=> node.id==selectedNodeId ? simplyColours[node.group] : hiddenColour);
    console.log('Entering function')
    let neighboursIds=[selectedNodeId];
    let influencedIds=[];
    let influencersIds=[];

    //find influencers
    if(showInfluenced){
      //console.log("showInfluenced loop")
      for(i=0,numberOfLinks=gData.links.length;i<numberOfLinks;i++){
        if(gData.links[i].source.id==selectedNodeId){
          //console.log(gData.links[i].target);
          influencedIds.push(gData.links[i].target.id)
        }
      }
    }
    console.log(influencedIds)

    //find influencers
    if(showInfluencers){
      //console.log("showInfluencers loop")
      for(i=0,numberOfLinks=gData.links.length;i<numberOfLinks;i++){
        //console.log(gData.links[i])
        if(gData.links[i].target.id==selectedNodeId){
          //console.log("Find influencers loop")
          //console.log(gData.links[i]);
          //console.log(gData.links[i].source);
          influencersIds.push(gData.links[i].source.id)
        }
      }
    }
    console.log(influencersIds)

    neighboursIds=neighboursIds.concat(influencersIds).concat(influencedIds);

    //colour in neighbours, hide everything else
    Graph.nodeColor(node=> neighboursIds.includes(node.id) ? simplyColours[node.group] : hiddenColour)
    //could make this a more complicated if statement to change the colour depending on whether they are influencers or influenced
  }

function moveToNode(){

}

function windowResize(){
  Graph.width(window.innerWidth*0.9).height(window.innerHeight)
}

</script>
</body>
</html>
