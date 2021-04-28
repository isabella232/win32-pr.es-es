---
description: Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116363"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="d6ce2-103">Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="d6ce2-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="d6ce2-104">En esta sección se describen los pasos básicos de mitigación y cómo planear la compatibilidad futura de las aplicaciones mientras se abordan los problemas.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="d6ce2-105">Windows Internet Explorer admite los modelos de Internet Explorer heredados siempre que sea factible para que los sitios que desarrolle para ellos sigan comportándose según lo previsto en las versiones más recientes de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="d6ce2-106">A partir de Windows Internet Explorer 8, puede optar por admitir comportamientos heredados seleccionando el modo de representación en función de la página.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="d6ce2-107">Internet Explorer 8 incluye los siguientes modos de representación que puede establecer mediante el encabezado X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="d6ce2-108">Valor de content</span><span class="sxs-lookup"><span data-stu-id="d6ce2-108">Content value</span></span> | <span data-ttu-id="d6ce2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6ce2-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ce2-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="d6ce2-110">IE=5</span></span>          | <span data-ttu-id="d6ce2-111">Use el modo de quirks.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="d6ce2-112">IE=7</span><span class="sxs-lookup"><span data-stu-id="d6ce2-112">IE=7</span></span>          | <span data-ttu-id="d6ce2-113">Use siempre windows Internet Explorer modo 7.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="d6ce2-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="d6ce2-114">IE=EmulateIE7</span></span> | <span data-ttu-id="d6ce2-115">Se muestra Internet Explorer modo 7 a menos que el sitio tenga las peculiaridades DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="d6ce2-116">IE=8</span><span class="sxs-lookup"><span data-stu-id="d6ce2-116">IE=8</span></span>          | <span data-ttu-id="d6ce2-117">Use siempre Internet Explorer modo 8.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="d6ce2-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="d6ce2-118">IE=EmulateIE8</span></span> | <span data-ttu-id="d6ce2-119">Invalide Vista de compatibilidad en las máquinas cliente y use Internet Explorer modo 8.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="d6ce2-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="d6ce2-120">IE=Edge</span></span>       | <span data-ttu-id="d6ce2-121">Mostrar en el modo más reciente.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-121">Display in the latest mode.</span></span> <span data-ttu-id="d6ce2-122">En Internet Explorer 8, este valor es equivalente a IE=8.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="d6ce2-123">En los temas siguientes se describe cómo actualizar aplicaciones web mediante Vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="d6ce2-124">Tema</span><span class="sxs-lookup"><span data-stu-id="d6ce2-124">Topic</span></span>                                                                                                  | <span data-ttu-id="d6ce2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6ce2-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="d6ce2-126">¿Qué es Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="d6ce2-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="d6ce2-127">Describe Vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="d6ce2-128">¿Por qué necesita Vista de compatibilidad?</span><span class="sxs-lookup"><span data-stu-id="d6ce2-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="d6ce2-129">Describe por qué debe usar Vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="d6ce2-130">Uso de la etiqueta meta para garantizar la compatibilidad futura</span><span class="sxs-lookup"><span data-stu-id="d6ce2-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="d6ce2-131">Describe cómo puede usar el **meta** elemento para garantizar la compatibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="d6ce2-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



