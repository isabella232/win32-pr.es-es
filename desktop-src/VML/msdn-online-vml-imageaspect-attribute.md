---
title: Atributo ImageAspect de VML
description: Atributo ImageAspect de VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359134"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="6225d-103">Atributo ImageAspect de VML</span><span class="sxs-lookup"><span data-stu-id="6225d-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="6225d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6225d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6225d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6225d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6225d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6225d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6225d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6225d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6225d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6225d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6225d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6225d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6225d-110">Define cómo se conservará la relación de aspecto de la imagen del trazo.</span><span class="sxs-lookup"><span data-stu-id="6225d-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="6225d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6225d-111">Read/write.</span></span> <span data-ttu-id="6225d-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="6225d-112">**String**.</span></span>

<span data-ttu-id="6225d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6225d-113">**Applies To**</span></span>

[<span data-ttu-id="6225d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="6225d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="6225d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6225d-115">**Tag Syntax**</span></span>

<span data-ttu-id="6225d-116"><v:</span><span class="sxs-lookup"><span data-stu-id="6225d-116"><v:</span></span>

<span data-ttu-id="6225d-117">Element *imageaspect = "* expresión *" >*</span><span class="sxs-lookup"><span data-stu-id="6225d-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="6225d-118">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="6225d-118">**Script Syntax**</span></span>

<span data-ttu-id="6225d-119">Element *. imageaspect = "* expresión *"*</span><span class="sxs-lookup"><span data-stu-id="6225d-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="6225d-120">*=* elemento Expression *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="6225d-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="6225d-121">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6225d-121">**Remarks**</span></span>

<span data-ttu-id="6225d-122">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="6225d-122">Values include:</span></span>



| <span data-ttu-id="6225d-123">Value</span><span class="sxs-lookup"><span data-stu-id="6225d-123">Value</span></span>   | <span data-ttu-id="6225d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6225d-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="6225d-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6225d-125">Ignore</span></span>  | <span data-ttu-id="6225d-126">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="6225d-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="6225d-127">Al menos</span><span class="sxs-lookup"><span data-stu-id="6225d-127">AtLeast</span></span> | <span data-ttu-id="6225d-128">La imagen es al menos tan grande como **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="6225d-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="6225d-129">AtMos</span><span class="sxs-lookup"><span data-stu-id="6225d-129">AtMost</span></span>  | <span data-ttu-id="6225d-130">La imagen no es mayor que **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="6225d-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="6225d-131">En cada caso, el atributo **ImageSize** se ajustará para conservar el aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6225d-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="6225d-132">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="6225d-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="6225d-133">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6225d-133">**Example**</span></span>

<span data-ttu-id="6225d-134">La imagen del trazo será al menos tan grande como el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6225d-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 