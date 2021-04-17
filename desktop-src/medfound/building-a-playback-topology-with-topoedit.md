---
description: Creación de una topología de reproducción con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Creación de una topología de reproducción con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105697900"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="ea3e1-103">Creación de una topología de reproducción con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ea3e1-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="ea3e1-104">TopoEdit puede crear una topología de reproducción para un archivo multimedia local mediante la adición y conexión automática de los nodos de origen, transformación y salida.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="ea3e1-105">TopoEdit no resuelve automáticamente la topología.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="ea3e1-106">Para reproducir la topología, resuélvalos y, a continuación, use los controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="ea3e1-107">Para compilar y reproducir una topología para un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="ea3e1-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="ea3e1-108">En el menú **archivo** , haga clic en **archivo de representación**.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="ea3e1-109">Se abrirá el cuadro de diálogo **Seleccionar origen de medios** .</span><span class="sxs-lookup"><span data-stu-id="ea3e1-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="ea3e1-110">Navegue hasta la carpeta donde se encuentra el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="ea3e1-111">En el campo **nombre de archivo:** , escriba el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="ea3e1-112">Haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-112">Click **Open**.</span></span>

    <span data-ttu-id="ea3e1-113">En el **Panel de topología** se muestra la topología conectada.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="ea3e1-114">Internamente, TopoEdit realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="ea3e1-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="ea3e1-115">Enumera las secuencias del archivo multimedia y crea los nodos de origen.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="ea3e1-116">En función del tipo de medio de los nodos de origen, agrega nodos de transformación, como descodificadores.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="ea3e1-117">Agrega el receptor del representador de audio de streaming (SAR) para el flujo de audio y el receptor de representador de vídeo mejorado (EVR) para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="ea3e1-118">Conecta las entradas de nodo y las salidas de nodo.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="ea3e1-119">En el menú **topología** , haga clic en **resolver topología**.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="ea3e1-120">Haga clic en el botón **reproducir** de la barra de herramientas para reproducir la topología.</span><span class="sxs-lookup"><span data-stu-id="ea3e1-120">Click the **Play** button on the toolbar to play the topology.</span></span> En la imagen siguiente se muestra el botón **reproducir** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="ea3e1-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea3e1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea3e1-123">Controles de reproducción en TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ea3e1-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="ea3e1-124">Resolver una topología con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ea3e1-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="ea3e1-125">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="ea3e1-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



