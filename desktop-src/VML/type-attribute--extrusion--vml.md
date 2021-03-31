---
title: Atributo de tipo (extrusión) (VML)
description: Atributo de tipo (extrusión) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904709"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="cad8e-103">Atributo de tipo (extrusión) (VML)</span><span class="sxs-lookup"><span data-stu-id="cad8e-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="cad8e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cad8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cad8e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="cad8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cad8e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="cad8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cad8e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="cad8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cad8e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cad8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cad8e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cad8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cad8e-110">Define la manera en que se extrude la forma.</span><span class="sxs-lookup"><span data-stu-id="cad8e-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="cad8e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cad8e-111">Read/write.</span></span> <span data-ttu-id="cad8e-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="cad8e-112">**String**.</span></span>

<span data-ttu-id="cad8e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="cad8e-113">**Applies To**</span></span>

[<span data-ttu-id="cad8e-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="cad8e-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="cad8e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="cad8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="cad8e-116"><o: tipo de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="cad8e-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="cad8e-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="cad8e-117">**Script Syntax**</span></span>

<span data-ttu-id="cad8e-118">*Element* . Type = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="cad8e-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="cad8e-119">*expresión* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="cad8e-119">*expression*=*element*.type</span></span>

<span data-ttu-id="cad8e-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="cad8e-120">**Remarks**</span></span>

<span data-ttu-id="cad8e-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="cad8e-121">Values include:</span></span>



| <span data-ttu-id="cad8e-122">Value</span><span class="sxs-lookup"><span data-stu-id="cad8e-122">Value</span></span>       | <span data-ttu-id="cad8e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cad8e-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad8e-124">parallel</span><span class="sxs-lookup"><span data-stu-id="cad8e-124">parallel</span></span>    | <span data-ttu-id="cad8e-125">La extrusión se representa para que el centro de proyección esté indefinidamente lejos; es decir, las líneas de extrusión no convergen (a diferencia de las proyecciones de perspectiva).</span><span class="sxs-lookup"><span data-stu-id="cad8e-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="cad8e-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cad8e-126">Default.</span></span> |
| <span data-ttu-id="cad8e-127">perspectiva</span><span class="sxs-lookup"><span data-stu-id="cad8e-127">perspective</span></span> | <span data-ttu-id="cad8e-128">La extrusión se representa en un centro de proyección, que es igual que el punto de desvanecimiento para los objetos no girados.</span><span class="sxs-lookup"><span data-stu-id="cad8e-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="cad8e-129">**Microsoft Office atributo Extensions**</span><span class="sxs-lookup"><span data-stu-id="cad8e-129">**Microsoft Office Extensions Attribute**</span></span>

 

 