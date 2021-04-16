---
description: Agregar nodos de salida con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Agregar nodos de salida con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705561"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="a3307-103">Agregar nodos de salida con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a3307-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="a3307-104">En una topología, un nodo de salida representa un receptor de medios que recibe los datos multimedia de un nodo de transformación y los presenta para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a3307-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="a3307-105">El tipo de nodo de salida depende del tipo de medio del nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="a3307-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="a3307-106">En la tabla siguiente se muestra el comando de menú/barra de herramientas para agregar un nodo de salida a la topología.</span><span class="sxs-lookup"><span data-stu-id="a3307-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3307-107">Tipo de medio de origen</span><span class="sxs-lookup"><span data-stu-id="a3307-107">Source media type</span></span></th>
<th><span data-ttu-id="a3307-108">Comando de menú/barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="a3307-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="a3307-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3307-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3307-110">Secuencia de audio</span><span class="sxs-lookup"><span data-stu-id="a3307-110">Audio stream</span></span></td>
<td><span data-ttu-id="a3307-111">En el menú <strong>topología</strong> , haga clic en <strong>Agregar SAR</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3307-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="a3307-112">Crea un nodo de salida para el representador de audio de streaming (SAR) que reproduce una secuencia de audio a través de un dispositivo de audio, como una tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="a3307-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3307-113">Secuencia de vídeo</span><span class="sxs-lookup"><span data-stu-id="a3307-113">Video stream</span></span></td>
<td><span data-ttu-id="a3307-114">En el menú de <strong>topología</strong> , haga clic en <strong>Agregar EVR</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3307-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="a3307-115">Crea un nodo de salida para el representador de vídeo mejorado (EVR) que muestra los fotogramas de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3307-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3307-116">Receptor de multimedia personalizado</span><span class="sxs-lookup"><span data-stu-id="a3307-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="a3307-117">En el menú <strong>topología</strong> , haga clic en <strong>Agregar receptor personalizado</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3307-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="a3307-118">Se abre el cuadro de diálogo <strong>GUID personalizado de entrada</strong> .</span><span class="sxs-lookup"><span data-stu-id="a3307-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="a3307-119">En el campo <strong>GUID:</strong> , escriba el GUID del receptor personalizado que desee agregar a la topología.</span><span class="sxs-lookup"><span data-stu-id="a3307-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="a3307-120">TopoEdit espera el GUID con el formato &quot; {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} &quot; .</span><span class="sxs-lookup"><span data-stu-id="a3307-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="a3307-121">De lo contrario, no se puede Agregar el nodo y se muestra un &quot; mensaje de error GUID no válido &quot; .</span><span class="sxs-lookup"><span data-stu-id="a3307-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="a3307-122">Haga clic en <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3307-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="a3307-123">Crea un nodo de salida para el receptor de flujo para un origen de multimedia personalizado.</span><span class="sxs-lookup"><span data-stu-id="a3307-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="a3307-124">El receptor personalizado debe admitir <strong>CoCreateInstance</strong> para que el receptor pueda especificarse con un CLSID.</span><span class="sxs-lookup"><span data-stu-id="a3307-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a3307-125">TopoEdit crea el nodo de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="a3307-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="a3307-126">En el **Panel de topología** se muestra el nodo de salida como un cuadro verde que muestra el nombre del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a3307-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="a3307-127">Para obtener información sobre cómo agregar nodos de salida mediante programación usando Media Foundation API, vea [crear nodos de salida](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="a3307-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3307-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3307-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3307-129">Compilar topologías mediante TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a3307-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="a3307-130">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="a3307-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="a3307-131">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="a3307-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="a3307-132">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a3307-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




