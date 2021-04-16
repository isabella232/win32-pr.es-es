---
description: Administrar proyectos de edición de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Administrar proyectos de edición de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666111"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="88d77-103">Administrar proyectos de edición de vídeo</span><span class="sxs-lookup"><span data-stu-id="88d77-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="88d77-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="88d77-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="88d77-105">Las siguientes sugerencias le ayudarán a administrar los proyectos de los [servicios de edición de DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="88d77-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="88d77-106">Cambios en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="88d77-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="88d77-107">Si cambia la escala de tiempo después de compilar el gráfico de filtros, llame de nuevo a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para recompilar el front-end.</span><span class="sxs-lookup"><span data-stu-id="88d77-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="88d77-108">Normalmente, esto no afecta al resto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="88d77-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="88d77-109">Sin embargo, en ocasiones, el motor de representación debe eliminar todo el gráfico antes de recompilar el front-end.</span><span class="sxs-lookup"><span data-stu-id="88d77-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="88d77-110">(Por ejemplo, esto sucede si agrega o quita un grupo). El método **ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET para indicar que ha eliminado el gráfico.</span><span class="sxs-lookup"><span data-stu-id="88d77-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="88d77-111">Si esto ocurre, la aplicación debe volver a generar la sección de representación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="88d77-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="88d77-112">Para quitar todos los objetos completamente de la escala de tiempo, llame al método [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="88d77-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="88d77-113">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="88d77-113">**Cleanup**</span></span>

-   <span data-ttu-id="88d77-114">Cuando haya terminado de usar un motor de representación, llame al método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="88d77-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="88d77-115">Al igual que con cualquier objeto COM, asegúrese de liberar todos los punteros de interfaz cuando haya terminado de usarlo.</span><span class="sxs-lookup"><span data-stu-id="88d77-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="88d77-116">El motor de representación no mantiene un recuento de referencias en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="88d77-117">No libere la escala de tiempo antes de que haya terminado de usarla y llame primero a **ScrapIt** en el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="88d77-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="88d77-118">Si libera todas las referencias a una escala de tiempo, no utilice ninguno de los objetos de esa escala de tiempo, incluso si contiene recuentos de referencias en ellos.</span><span class="sxs-lookup"><span data-stu-id="88d77-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="88d77-119">**Varias instancias de escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="88d77-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="88d77-120">No mueva los objetos Timeline entre las escalas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="88d77-121">Cada objeto de una escala de tiempo debe crearse en esa escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="88d77-122">La escala de tiempo contiene una memoria caché interna con información sobre los objetos que crea; mover objetos de escala de tiempo puede interrumpir la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="88d77-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="88d77-123">Nunca utilice la misma instancia de un motor de representación con más de una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="88d77-124">El motor de representación contiene una memoria caché con información sobre la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="88d77-125">Varias escalas de tiempo interrumpirán la memoria caché y provocarán resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="88d77-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="88d77-126">Si necesita dos escalas de tiempo activas, cree instancias independientes de motores de representación para cada escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="88d77-127">Una escala de tiempo puede usar más de un motor de representación, pero no al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d77-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="88d77-128">Elimine el antiguo motor de representación antes de usar otro motor de representación.</span><span class="sxs-lookup"><span data-stu-id="88d77-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="88d77-129">(Normalmente, esto se haría al pasar de usar el motor de representación básico para la vista previa al motor de representación inteligente para la escritura de archivos).</span><span class="sxs-lookup"><span data-stu-id="88d77-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="88d77-130">**Persistencia**</span><span class="sxs-lookup"><span data-stu-id="88d77-130">**Persistence**</span></span>

-   <span data-ttu-id="88d77-131">El gráfico de filtro no es persistente cuando guarda el proyecto en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="88d77-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="88d77-132">Por lo tanto, se pierde toda la información relacionada con la recompresión inteligente, el formato de compresión o los parámetros de compresión.</span><span class="sxs-lookup"><span data-stu-id="88d77-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="88d77-133">Depende de la aplicación restaurar estos parámetros después de cargar un proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d77-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88d77-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88d77-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88d77-135">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="88d77-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



