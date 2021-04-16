---
title: Atributo LockRotationCenter de VML
description: Atributo LockRotationCenter de VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676477"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="fe7a7-103">Atributo LockRotationCenter de VML</span><span class="sxs-lookup"><span data-stu-id="fe7a7-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="fe7a7-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fe7a7-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fe7a7-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fe7a7-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fe7a7-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fe7a7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fe7a7-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fe7a7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fe7a7-110">Determina si el atributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) especifica el giro del objeto extruido.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="fe7a7-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fe7a7-111">Read/write.</span></span> <span data-ttu-id="fe7a7-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-112">**VgTriState**.</span></span>

<span data-ttu-id="fe7a7-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="fe7a7-113">**Applies To**</span></span>

[<span data-ttu-id="fe7a7-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="fe7a7-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="fe7a7-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="fe7a7-115">**Tag Syntax**</span></span>

<span data-ttu-id="fe7a7-116"><o: *elemento* lockrotationcenter = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="fe7a7-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="fe7a7-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="fe7a7-117">**Script Syntax**</span></span>

<span data-ttu-id="fe7a7-118">*Element* . lockrotationcenter = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="fe7a7-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="fe7a7-119">*expresión* = de *elemento*. lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="fe7a7-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="fe7a7-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="fe7a7-120">**Remarks**</span></span>

<span data-ttu-id="fe7a7-121">Si es **false**, el atributo de [orientación](msdn-online-vml-orientation-attribute.md) especifica el giro.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="fe7a7-122">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="fe7a7-122">The default is **True**.</span></span>

<span data-ttu-id="fe7a7-123">Observe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fe7a7-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="fe7a7-124">es igual que:</span><span class="sxs-lookup"><span data-stu-id="fe7a7-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="fe7a7-125">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="fe7a7-125">*Microsoft Office Extensions Attribute*</span></span>

 

 