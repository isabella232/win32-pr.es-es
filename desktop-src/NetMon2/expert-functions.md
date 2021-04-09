---
description: Los expertos que exportan la función ejecutar o configurar solo pueden llamar a las siguientes funciones auxiliares.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funciones de experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907679"
---
# <a name="expert-functions"></a><span data-ttu-id="61c49-103">Funciones de experto</span><span class="sxs-lookup"><span data-stu-id="61c49-103">Expert Functions</span></span>

<span data-ttu-id="61c49-104">Los expertos que exportan la función [Ejecutar](run.md) o [configurar](configure.md) solo pueden llamar a las siguientes funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="61c49-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="61c49-105">Función</span><span class="sxs-lookup"><span data-stu-id="61c49-105">Function</span></span>                                         | <span data-ttu-id="61c49-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="61c49-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="61c49-107">ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="61c49-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="61c49-108">Recupera un fotograma determinado de la captura.</span><span class="sxs-lookup"><span data-stu-id="61c49-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="61c49-109">ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="61c49-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="61c49-110">Indica el porcentaje de finalización del análisis de captura del experto.</span><span class="sxs-lookup"><span data-stu-id="61c49-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="61c49-111">ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="61c49-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="61c49-112">Recupera la información de inicio del experto.</span><span class="sxs-lookup"><span data-stu-id="61c49-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="61c49-113">ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="61c49-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="61c49-114">Recupera el tamaño de la memoria asignada por una llamada a la función **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="61c49-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="61c49-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="61c49-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="61c49-116">Indica un problema y recupera información sobre el problema si existe uno.</span><span class="sxs-lookup"><span data-stu-id="61c49-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="61c49-117">ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="61c49-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="61c49-118">Asigna memoria para el experto.</span><span class="sxs-lookup"><span data-stu-id="61c49-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="61c49-119">ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="61c49-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="61c49-120">Cambia el tamaño de la memoria asignada por la función **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="61c49-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="61c49-121">ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="61c49-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="61c49-122">Libera la memoria asignada por el experto.</span><span class="sxs-lookup"><span data-stu-id="61c49-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="61c49-123">Para obtener información sobre las funciones de exportación, las funciones auxiliares a las que pueden llamar expertos y analizadores, estructuras y enumeraciones, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="61c49-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="61c49-124">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="61c49-124">For information about</span></span>                                             | <span data-ttu-id="61c49-125">Vea</span><span class="sxs-lookup"><span data-stu-id="61c49-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="61c49-126">Funciones exportadas por expertos</span><span class="sxs-lookup"><span data-stu-id="61c49-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="61c49-127">Funciones de exportación de archivos DLL de experto</span><span class="sxs-lookup"><span data-stu-id="61c49-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="61c49-128">Estructuras usadas por las funciones de expertos</span><span class="sxs-lookup"><span data-stu-id="61c49-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="61c49-129">Estructuras expertas</span><span class="sxs-lookup"><span data-stu-id="61c49-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="61c49-130">Enumeraciones usadas por las estructuras y funciones de expertos</span><span class="sxs-lookup"><span data-stu-id="61c49-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="61c49-131">Enumeraciones de experto</span><span class="sxs-lookup"><span data-stu-id="61c49-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="61c49-132">Funciones auxiliares comunes a las que pueden llamar expertos y analizadores</span><span class="sxs-lookup"><span data-stu-id="61c49-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="61c49-133">Funciones comunes de experto y analizador</span><span class="sxs-lookup"><span data-stu-id="61c49-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



