---
title: Atributo AutoRotationCenter de VML
description: Atributo AutoRotationCenter de VML
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792388"
---
# <a name="vml-autorotationcenter-attribute"></a><span data-ttu-id="a6ae9-103">Atributo AutoRotationCenter de VML</span><span class="sxs-lookup"><span data-stu-id="a6ae9-103">VML AutoRotationCenter Attribute</span></span>

<span data-ttu-id="a6ae9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6ae9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6ae9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6ae9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6ae9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6ae9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6ae9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6ae9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6ae9-110">Determina si el centro de rotación será el centro geométrico de la extrusión.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-110">Determines whether the center of rotation will be the geometric center of the extrusion.</span></span> <span data-ttu-id="a6ae9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a6ae9-111">Read/write.</span></span> <span data-ttu-id="a6ae9-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-112">**VgTriState**.</span></span>

<span data-ttu-id="a6ae9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a6ae9-113">**Applies To**</span></span>

[<span data-ttu-id="a6ae9-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="a6ae9-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="a6ae9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a6ae9-115">**Tag Syntax**</span></span>

<span data-ttu-id="a6ae9-116"><o: *elemento* autorotationcenter = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a6ae9-116"><o: *element* autorotationcenter=" *expression* "></span></span>

<span data-ttu-id="a6ae9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a6ae9-117">**Script Syntax**</span></span>

<span data-ttu-id="a6ae9-118">*Element* . autorotationcenter = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a6ae9-118">*element* .autorotationcenter="*expression*"</span></span>

<span data-ttu-id="a6ae9-119">*expresión* = de *elemento*. autorotationcenter</span><span class="sxs-lookup"><span data-stu-id="a6ae9-119">*expression*=*element*.autorotationcenter</span></span>

<span data-ttu-id="a6ae9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a6ae9-120">**Remarks**</span></span>

<span data-ttu-id="a6ae9-121">El centro geométrico de una forma extruida es 0, 0,0.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-121">The geometric center of an extruded shape is 0,0,0.</span></span> <span data-ttu-id="a6ae9-122">Si el valor de este atributo es **false**, el centro de rotación viene determinado por el atributo [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ae9-122">If the value of this attribute is **False**, the center of rotation is determined by the [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) attribute.</span></span> <span data-ttu-id="a6ae9-123">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-123">The default is **False**.</span></span>

<span data-ttu-id="a6ae9-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="a6ae9-124">*Microsoft Office Extensions Attribute*</span></span>

 

 