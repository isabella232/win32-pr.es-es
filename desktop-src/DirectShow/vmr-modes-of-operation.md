---
description: Modos de funcionamiento de VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modos de funcionamiento de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666770"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="35197-103">Modos de funcionamiento de VMR</span><span class="sxs-lookup"><span data-stu-id="35197-103">VMR Modes of Operation</span></span>

<span data-ttu-id="35197-104">La arquitectura de componentes de VMR permite a las aplicaciones configurarlo de varias maneras, dependiendo de cómo se realice la representación.</span><span class="sxs-lookup"><span data-stu-id="35197-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="35197-105">En la tabla siguiente se muestran los tres modos de presentación y los dos modos de combinación, y los componentes que están presentes para cada configuración.</span><span class="sxs-lookup"><span data-stu-id="35197-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="35197-106">Mode</span><span class="sxs-lookup"><span data-stu-id="35197-106">Mode</span></span>       | <span data-ttu-id="35197-107">Flujo único</span><span class="sxs-lookup"><span data-stu-id="35197-107">Single Stream</span></span>                                                                     | <span data-ttu-id="35197-108">Varias secuencias (modo de combinación)</span><span class="sxs-lookup"><span data-stu-id="35197-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35197-109">Ventanas</span><span class="sxs-lookup"><span data-stu-id="35197-109">Windowed</span></span>   | <span data-ttu-id="35197-110">Allocator: unidad de sincronización presenterCore</span><span class="sxs-lookup"><span data-stu-id="35197-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="35197-111">Administrador de ventanas</span><span class="sxs-lookup"><span data-stu-id="35197-111">Window Manager</span></span><br/> | <span data-ttu-id="35197-112">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="35197-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="35197-113">Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="35197-113">Allocator-presenter</span></span><br/> <span data-ttu-id="35197-114">Unidad de sincronización básica</span><span class="sxs-lookup"><span data-stu-id="35197-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="35197-115">Administrador de ventanas</span><span class="sxs-lookup"><span data-stu-id="35197-115">Window Manager</span></span><br/> |
| <span data-ttu-id="35197-116">Sin ventana</span><span class="sxs-lookup"><span data-stu-id="35197-116">Windowless</span></span> | <span data-ttu-id="35197-117">Allocator: unidad de sincronización presenterCore</span><span class="sxs-lookup"><span data-stu-id="35197-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="35197-118">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="35197-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="35197-119">Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="35197-119">Allocator-presenter</span></span><br/> <span data-ttu-id="35197-120">Unidad de sincronización básica</span><span class="sxs-lookup"><span data-stu-id="35197-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="35197-121">No rendered</span><span class="sxs-lookup"><span data-stu-id="35197-121">Renderless</span></span> | <span data-ttu-id="35197-122">Allocator-Presenter (proporcionado por la aplicación) unidad de sincronización principal</span><span class="sxs-lookup"><span data-stu-id="35197-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="35197-123">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="35197-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="35197-124">Allocator: presentador (proporcionado por la aplicación)</span><span class="sxs-lookup"><span data-stu-id="35197-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="35197-125">Unidad de sincronización básica</span><span class="sxs-lookup"><span data-stu-id="35197-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="35197-126">\* Indica que la aplicación tiene la opción de proporcionar un componente personalizado o usar el componente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35197-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="35197-127">En todas las configuraciones, el punto principal a recordar al crear gráficos de filtros con la VMR es que debe configurar la VMR antes de conectarla.</span><span class="sxs-lookup"><span data-stu-id="35197-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="35197-128">Para todas las configuraciones, los PIN no se pueden agregar ni quitar dinámicamente después de que el VMR esté conectado al filtro de nivel superior, pero se pueden conectar y desconectar.</span><span class="sxs-lookup"><span data-stu-id="35197-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="35197-129">Si la aplicación no está seguro de cuántos PIN serán necesarios, debe configurar la VMR para el número máximo que podría ser necesario.</span><span class="sxs-lookup"><span data-stu-id="35197-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="35197-130">La presencia de clavijas de entrada sin usar en el filtro no degrada el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="35197-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="35197-131">A diferencia del mezclador de superposición anterior, VMR no tiene ningún PIN de salida porque no requiere un filtro independiente para la administración de ventanas.</span><span class="sxs-lookup"><span data-stu-id="35197-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="35197-132">En las secciones siguientes se describe cómo configurar la VMR para un modo determinado:</span><span class="sxs-lookup"><span data-stu-id="35197-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="35197-133">Modo de ventana de VMR (compatibilidad)</span><span class="sxs-lookup"><span data-stu-id="35197-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="35197-134">Modo sin ventana de VMR</span><span class="sxs-lookup"><span data-stu-id="35197-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="35197-135">VMR con varias secuencias (modo de combinación)</span><span class="sxs-lookup"><span data-stu-id="35197-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="35197-136">Modo de mezcla YUV</span><span class="sxs-lookup"><span data-stu-id="35197-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="35197-137">Colocar y mover rectángulos de vídeo en el espacio de composición</span><span class="sxs-lookup"><span data-stu-id="35197-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="35197-138">Modo de reproducción no representativo de VMR (asignador personalizado)</span><span class="sxs-lookup"><span data-stu-id="35197-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="35197-139">Modo exclusivo de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="35197-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




