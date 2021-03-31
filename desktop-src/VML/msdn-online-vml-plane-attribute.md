---
title: Atributo de plano VML
description: Atributo de plano VML
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995355"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="21101-103">Atributo de plano VML</span><span class="sxs-lookup"><span data-stu-id="21101-103">VML Plane Attribute</span></span>

<span data-ttu-id="21101-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21101-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21101-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="21101-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21101-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="21101-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21101-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="21101-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21101-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21101-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21101-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21101-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21101-110">Especifica el plano que se encuentra en los ángulos rectos de la extrusión.</span><span class="sxs-lookup"><span data-stu-id="21101-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="21101-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="21101-111">Read/write.</span></span> <span data-ttu-id="21101-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="21101-112">**String**.</span></span>

<span data-ttu-id="21101-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="21101-113">**Applies To**</span></span>

[<span data-ttu-id="21101-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="21101-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="21101-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="21101-115">**Tag Syntax**</span></span>

<span data-ttu-id="21101-116"><o: *elemento* plano = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="21101-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="21101-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="21101-117">**Script Syntax**</span></span>

<span data-ttu-id="21101-118">*Element* . Plane = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="21101-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="21101-119">*expresión* = de *elemento*. plano</span><span class="sxs-lookup"><span data-stu-id="21101-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="21101-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="21101-120">**Remarks**</span></span>

<span data-ttu-id="21101-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="21101-121">Values include:</span></span>



| <span data-ttu-id="21101-122">Value</span><span class="sxs-lookup"><span data-stu-id="21101-122">Value</span></span> | <span data-ttu-id="21101-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="21101-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="21101-124">xy</span><span class="sxs-lookup"><span data-stu-id="21101-124">xy</span></span>    | <span data-ttu-id="21101-125">La extrusión está en los ángulos correctos para el plano XY.</span><span class="sxs-lookup"><span data-stu-id="21101-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="21101-126">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="21101-126">Default</span></span> |
| <span data-ttu-id="21101-127">ZX</span><span class="sxs-lookup"><span data-stu-id="21101-127">zx</span></span>    | <span data-ttu-id="21101-128">La extrusión está en ángulos rectos al plano ZX.</span><span class="sxs-lookup"><span data-stu-id="21101-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="21101-129">YZ</span><span class="sxs-lookup"><span data-stu-id="21101-129">yz</span></span>    | <span data-ttu-id="21101-130">La extrusión está en los ángulos correctos para el plano YZ.</span><span class="sxs-lookup"><span data-stu-id="21101-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="21101-131">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="21101-131">*Microsoft Office Extensions Attribute*</span></span>

 

 