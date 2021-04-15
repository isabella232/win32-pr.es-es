---
description: La escala de tiempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: La escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688739"
---
# <a name="the-timeline"></a><span data-ttu-id="8fcb9-103">La escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="8fcb9-103">The Timeline</span></span>

<span data-ttu-id="8fcb9-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8fcb9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8fcb9-105">La escala de tiempo expone la interfaz [**IAMTimeline**](iamtimeline.md) .</span><span class="sxs-lookup"><span data-stu-id="8fcb9-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="8fcb9-106">Esta interfaz contiene métodos para establecer las propiedades de la escala de tiempo; para agregar grupos a la escala de tiempo; y para crear objetos timeline, como grupos, pistas y orígenes.</span><span class="sxs-lookup"><span data-stu-id="8fcb9-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="8fcb9-107">Para crear una nueva escala de tiempo, llame a la función **CoCreateInstance** estándar como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8fcb9-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="8fcb9-108">La nueva escala de tiempo está vacía.</span><span class="sxs-lookup"><span data-stu-id="8fcb9-108">The new timeline is empty.</span></span> <span data-ttu-id="8fcb9-109">En este momento, puede cargar un archivo de proyecto existente (vea [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md)) o crear la escala de tiempo creando e insertando objetos nuevos (vea [construir una escala de tiempo](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="8fcb9-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fcb9-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fcb9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fcb9-111">Información general de los componentes de la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="8fcb9-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



