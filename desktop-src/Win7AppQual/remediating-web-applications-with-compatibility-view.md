---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717363"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="6b384-103">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="6b384-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="6b384-104">En esta sección se describen los pasos básicos de mitigación y cómo planear la compatibilidad con aplicaciones futuras mientras se abordan los problemas ahora.</span><span class="sxs-lookup"><span data-stu-id="6b384-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="6b384-105">Windows Internet Explorer es compatible con los modelos heredados de Internet Explorer siempre que sea factible para que los sitios que desarrolle en ellos sigan comportándose de la manera esperada en las versiones más recientes de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6b384-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="6b384-106">A partir de Windows Internet Explorer 8, puede elegir admitir comportamientos heredados seleccionando el modo de representación página por página.</span><span class="sxs-lookup"><span data-stu-id="6b384-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="6b384-107">Internet Explorer 8 incluye los siguientes modos de representación que se pueden establecer mediante el encabezado X-UA-compatible.</span><span class="sxs-lookup"><span data-stu-id="6b384-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="6b384-108">Valor de content</span><span class="sxs-lookup"><span data-stu-id="6b384-108">Content value</span></span> | <span data-ttu-id="6b384-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b384-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b384-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="6b384-110">IE=5</span></span>          | <span data-ttu-id="6b384-111">Usar el modo no estándar.</span><span class="sxs-lookup"><span data-stu-id="6b384-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="6b384-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="6b384-112">IE=7</span></span>          | <span data-ttu-id="6b384-113">Use siempre el modo de Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="6b384-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="6b384-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="6b384-114">IE=EmulateIE7</span></span> | <span data-ttu-id="6b384-115">Mostrar en modo Internet Explorer 7 a menos que el sitio tenga el DOCTYPE no estándar.</span><span class="sxs-lookup"><span data-stu-id="6b384-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="6b384-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="6b384-116">IE=8</span></span>          | <span data-ttu-id="6b384-117">Use siempre el modo Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="6b384-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="6b384-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="6b384-118">IE=EmulateIE8</span></span> | <span data-ttu-id="6b384-119">Invalide la vista de compatibilidad en los equipos cliente y use el modo Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="6b384-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="6b384-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="6b384-120">IE=Edge</span></span>       | <span data-ttu-id="6b384-121">Mostrar en el modo más reciente.</span><span class="sxs-lookup"><span data-stu-id="6b384-121">Display in the latest mode.</span></span> <span data-ttu-id="6b384-122">En Internet Explorer 8, este valor es equivalente a IE = 8.</span><span class="sxs-lookup"><span data-stu-id="6b384-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="6b384-123">En los temas siguientes se describe cómo actualizar aplicaciones web mediante la vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b384-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="6b384-124">Tema</span><span class="sxs-lookup"><span data-stu-id="6b384-124">Topic</span></span>                                                                                                  | <span data-ttu-id="6b384-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b384-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6b384-126">Qué es la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="6b384-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="6b384-127">Describe la vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b384-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="6b384-128">¿Por qué necesita la vista de compatibilidad?</span><span class="sxs-lookup"><span data-stu-id="6b384-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="6b384-129">Describe por qué debe usar la vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b384-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="6b384-130">Usar la etiqueta meta para garantizar compatibilidad futura</span><span class="sxs-lookup"><span data-stu-id="6b384-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="6b384-131">Describe cómo se puede usar el elemento **meta** para garantizar la compatibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="6b384-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



