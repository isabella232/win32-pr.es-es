---
description: Acerca de los motores de representación
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Acerca de los motores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537828"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="b388d-103">Acerca de los motores de representación</span><span class="sxs-lookup"><span data-stu-id="b388d-103">About the Render Engines</span></span>

<span data-ttu-id="b388d-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="b388d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b388d-105">En este artículo se describe cómo los [servicios de edición de DirectShow](directshow-editing-services.md) (des) representan un proyecto de edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b388d-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="b388d-106">En DES, un proyecto se representa como una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b388d-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="b388d-107">La escala de tiempo es útil porque simplifica las tareas más comunes en la edición de vídeo, como la reorganización de clips de origen y la adición de efectos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b388d-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="b388d-108">La arquitectura de la secuencia de DirectShow, por otro lado, requiere un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b388d-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="b388d-109">Por lo tanto, para representar el proyecto, debe traducir una escala de tiempo en un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="b388d-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="b388d-110">El componente que lo lleva a cabo se denomina *motor de representación*.</span><span class="sxs-lookup"><span data-stu-id="b388d-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="b388d-111">DirectShow proporciona dos motores de representación:</span><span class="sxs-lookup"><span data-stu-id="b388d-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="b388d-112">Motor de representación básico: crea un gráfico de filtro que proporciona una salida sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b388d-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="b388d-113">Smart Render Engine: crea un gráfico de filtro que entrega la salida comprimida.</span><span class="sxs-lookup"><span data-stu-id="b388d-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="b388d-114">El motor de representación inteligente utiliza la recompresión inteligente para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b388d-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="b388d-115">Con la recompresión inteligente, los archivos de origen se vuelven a comprimir solo cuando el formato de archivo original difiere del formato de salida final.</span><span class="sxs-lookup"><span data-stu-id="b388d-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="b388d-116">Si los formatos coinciden, el origen nunca se descomprimirá.</span><span class="sxs-lookup"><span data-stu-id="b388d-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="b388d-117">La recompresión inteligente solo se admite para la compresión de vídeo, no para la compresión de audio.</span><span class="sxs-lookup"><span data-stu-id="b388d-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="b388d-118">Para la versión preliminar, use el motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="b388d-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="b388d-119">El motor de representación inteligente también puede obtener una vista previa, pero es menos eficaz porque tiene que descomprimir el flujo comprimido.</span><span class="sxs-lookup"><span data-stu-id="b388d-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="b388d-120">Para escribir archivos, use el motor de representación inteligente si desea volver a comprimir inteligente.</span><span class="sxs-lookup"><span data-stu-id="b388d-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="b388d-121">De lo contrario, use el motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="b388d-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="b388d-122">La recompresión inteligente puede reducir en gran medida el tiempo que se tarda en escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="b388d-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b388d-123">No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b388d-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="b388d-124">Ambos motores de representación crean una ventana invisible que procesa los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b388d-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="b388d-125">El subproceso que crea el motor de representación debe tener un bucle de mensajes para enviar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b388d-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="b388d-126">Además, ese subproceso no debe salir hasta que se liberen el motor de representación y el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="b388d-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="b388d-127">De lo contrario, la aplicación podría bloquearse.</span><span class="sxs-lookup"><span data-stu-id="b388d-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="b388d-128">Construir el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="b388d-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="b388d-129">El gráfico de filtro se crea en dos fases.</span><span class="sxs-lookup"><span data-stu-id="b388d-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="b388d-130">En la primera fase, el motor de representación construye un "front-end", que es un gráfico de filtro parcial.</span><span class="sxs-lookup"><span data-stu-id="b388d-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="b388d-131">En el diagrama siguiente se muestra un front-end típico:</span><span class="sxs-lookup"><span data-stu-id="b388d-131">The following diagram illustrates a typical front end:</span></span>

![Front-end de gráfico de filtro](images/rendeng1.png)

<span data-ttu-id="b388d-133">Los subsistemas contienen varios filtros especializados, que el motor de representación ensambla automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b388d-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="b388d-134">El front-end contiene un PIN de salida para cada grupo de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b388d-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="b388d-135">Los pin de salida proporcionan datos sin comprimir si usa el motor de representación básico o datos comprimidos si usa el motor de representación inteligente.</span><span class="sxs-lookup"><span data-stu-id="b388d-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="b388d-136">En el segundo paso, los pin de salida se conectan a los filtros de representación.</span><span class="sxs-lookup"><span data-stu-id="b388d-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="b388d-137">En la versión preliminar, los filtros de representación son representadores de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="b388d-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="b388d-138">En el caso de la escritura de archivos, los filtros de representación son filtros de multiplexor (MUX) y filtros de escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="b388d-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![finalización del gráfico de filtros](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="b388d-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b388d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b388d-141">Obtener una vista previa de un proyecto</span><span class="sxs-lookup"><span data-stu-id="b388d-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="b388d-142">Escribir un proyecto en un archivo</span><span class="sxs-lookup"><span data-stu-id="b388d-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



