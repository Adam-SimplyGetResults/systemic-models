<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="autocomplete-styles.css">
<script src="//unpkg.com/3d-force-graph"></script>
</head>
<body>

<!--Make sure the form has the autocomplete function switched off:-->
<form autocomplete="off">
  <div class="autocomplete" style="width:300px;">
    <input id="myInput" type="text" name="myInputText" placeholder="Search for a node here...">
  </div>
  <button type="button" onclick="onSearchSubmit()">Search</button>
</form>

<p id="selectedNodeP">No node selected</p>

<div id="3d-graph"></div>

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
    alert("That's not a valid node, jeez")
  }
  //Change the html message to show the node that has been searched for as selected
  if(searchedNodeId){
    selectedNodeId=searchedNodeId;
    document.getElementById('selectedNodeP').innerHTML = `Node Selcted: ${selectedNodeId}`
  }

  //Colour the node that you have selected
  Graph.nodeColor(node=> selectedNodeId.includes(node.id) ? simplyColours[node.group] : hiddenColour)

  //Move the camera to view the node you want
  moveToNode(selectedNodeId);
}


function moveToNode(){

}

</script>
</body>
