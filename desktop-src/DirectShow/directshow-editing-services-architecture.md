---
description: Arquitectura de servicios de edición de DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Arquitectura de servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652311"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="d24ed-103">Arquitectura de servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d24ed-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="d24ed-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="d24ed-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d24ed-105">En la ilustración siguiente se muestra la arquitectura de los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="d24ed-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![arquitectura de servicios de edición de DirectShow](images/architecture.png)

-   <span data-ttu-id="d24ed-107">Timeline: representa una producción de vídeo como una colección de clips, transiciones y efectos de origen, organizada en un conjunto de pistas anidadas.</span><span class="sxs-lookup"><span data-stu-id="d24ed-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="d24ed-108">Para obtener más información, vea [el modelo Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="d24ed-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="d24ed-109">Analizador XML: analiza la escala de tiempo y genera un archivo de salida, o lee un archivo de entrada y genera una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="d24ed-110">DES admite un formato de persistencia basado en XML.</span><span class="sxs-lookup"><span data-stu-id="d24ed-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="d24ed-111">Motor de representación: traduce la escala de tiempo a un formato que se puede representar como un medio de streaming.</span><span class="sxs-lookup"><span data-stu-id="d24ed-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="d24ed-112">De forma predeterminada, el motor de representación genera un gráfico de filtros de DirectShow (consulte la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="d24ed-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="d24ed-113">Localizador de medios: mantiene una memoria caché de las ubicaciones de los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d24ed-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="d24ed-114">Cuando se produce un error al intentar abrir un elemento multimedia, DES usa la memoria caché para buscar el elemento, en función de un historial de aperturas correctas.</span><span class="sxs-lookup"><span data-stu-id="d24ed-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="d24ed-115">La escala de tiempo es una descripción abstracta de un proyecto de edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="d24ed-116">Especifica los clips de origen usados en el proyecto, las horas de inicio y de finalización, los efectos y las transiciones, etc.</span><span class="sxs-lookup"><span data-stu-id="d24ed-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="d24ed-117">Sin embargo, la escala de tiempo no representa las secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="d24ed-118">En su lugar, el motor de representación traduce la escala de tiempo en un gráfico de filtros, para la vista previa o la salida del archivo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="d24ed-119">Una aplicación manipula la escala de tiempo en lugar de manipular directamente el gráfico de filtro, lo que sería engorroso y propenso a errores.</span><span class="sxs-lookup"><span data-stu-id="d24ed-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="d24ed-120">En la tabla siguiente se enumeran las tareas principales que realiza una aplicación de edición de vídeo típica, junto con las interfaces que admiten cada tarea.</span><span class="sxs-lookup"><span data-stu-id="d24ed-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="d24ed-121">En secciones posteriores se describen con más detalle estas tareas y las interfaces.</span><span class="sxs-lookup"><span data-stu-id="d24ed-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="d24ed-122">Tarea</span><span class="sxs-lookup"><span data-stu-id="d24ed-122">Task</span></span>                                     | <span data-ttu-id="d24ed-123">Interfaz (s)</span><span class="sxs-lookup"><span data-stu-id="d24ed-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24ed-124">Construya o modifique una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="d24ed-125">[**IAMTimeline**](iamtimeline.md) y las otras interfaces de **IAMTimelineXXXX**</span><span class="sxs-lookup"><span data-stu-id="d24ed-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="d24ed-126">Guardar y cargar archivos de proyecto.</span><span class="sxs-lookup"><span data-stu-id="d24ed-126">Save and load project files.</span></span>             | [<span data-ttu-id="d24ed-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="d24ed-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="d24ed-128">Obtenga una vista previa de un proyecto o escríbalo en un archivo.</span><span class="sxs-lookup"><span data-stu-id="d24ed-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="d24ed-129">[**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="d24ed-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="d24ed-130">Además, una aplicación puede realizar algunas o todas las tareas secundarias siguientes.</span><span class="sxs-lookup"><span data-stu-id="d24ed-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="d24ed-131">Tarea</span><span class="sxs-lookup"><span data-stu-id="d24ed-131">Task</span></span>                                                                                           | <span data-ttu-id="d24ed-132">Interfaz (s)</span><span class="sxs-lookup"><span data-stu-id="d24ed-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d24ed-133">Obtener información acerca de los archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d24ed-133">Obtain information about media files.</span></span> <span data-ttu-id="d24ed-134">(Número de secuencias; formato y duración de cada secuencia).</span><span class="sxs-lookup"><span data-stu-id="d24ed-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="d24ed-135">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="d24ed-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="d24ed-136">Establezca las propiedades en las transiciones y los efectos.</span><span class="sxs-lookup"><span data-stu-id="d24ed-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="d24ed-137">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="d24ed-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="d24ed-138">Recibir una notificación cuando se produzcan errores durante la representación.</span><span class="sxs-lookup"><span data-stu-id="d24ed-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="d24ed-139">[**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="d24ed-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="d24ed-140">Recuperar fotogramas de póster.</span><span class="sxs-lookup"><span data-stu-id="d24ed-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="d24ed-141">[**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="d24ed-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="d24ed-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d24ed-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24ed-143">Introducción con servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d24ed-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



