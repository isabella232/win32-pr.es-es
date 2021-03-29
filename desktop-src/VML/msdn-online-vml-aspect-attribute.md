---
title: Atributo de aspecto VML
description: Atributo de aspecto VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792400"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="b1c3f-103">Atributo de aspecto VML</span><span class="sxs-lookup"><span data-stu-id="b1c3f-103">VML Aspect Attribute</span></span>

<span data-ttu-id="b1c3f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1c3f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1c3f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1c3f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1c3f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1c3f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1c3f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1c3f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1c3f-110">Especifica cómo se conservará la relación de aspecto de la imagen de relleno.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="b1c3f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b1c3f-111">Read/write.</span></span> <span data-ttu-id="b1c3f-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-112">**String**.</span></span>

<span data-ttu-id="b1c3f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b1c3f-113">**Applies To**</span></span>

[<span data-ttu-id="b1c3f-114">Fill</span><span class="sxs-lookup"><span data-stu-id="b1c3f-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b1c3f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b1c3f-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1c3f-116"><v: *Element* Aspect = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b1c3f-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="b1c3f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b1c3f-117">**Script Syntax**</span></span>

<span data-ttu-id="b1c3f-118">*Element* . Aspect = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b1c3f-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="b1c3f-119">*expresión* = de *elemento*. Aspect</span><span class="sxs-lookup"><span data-stu-id="b1c3f-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="b1c3f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b1c3f-120">**Remarks**</span></span>

<span data-ttu-id="b1c3f-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="b1c3f-121">Values include:</span></span>



| <span data-ttu-id="b1c3f-122">Value</span><span class="sxs-lookup"><span data-stu-id="b1c3f-122">Value</span></span>   | <span data-ttu-id="b1c3f-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1c3f-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="b1c3f-124">ignore</span><span class="sxs-lookup"><span data-stu-id="b1c3f-124">ignore</span></span>  | <span data-ttu-id="b1c3f-125">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-125">Ignore aspect issues.</span></span> <span data-ttu-id="b1c3f-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-126">Default.</span></span>        |
| <span data-ttu-id="b1c3f-127">al menos</span><span class="sxs-lookup"><span data-stu-id="b1c3f-127">atleast</span></span> | <span data-ttu-id="b1c3f-128">La imagen es al menos tan grande como **el tamaño**.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="b1c3f-129">Atmos</span><span class="sxs-lookup"><span data-stu-id="b1c3f-129">atmost</span></span>  | <span data-ttu-id="b1c3f-130">La imagen no es más grande que **el tamaño**.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="b1c3f-131">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b1c3f-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="b1c3f-132">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b1c3f-132">**Example**</span></span>

<span data-ttu-id="b1c3f-133">La imagen que constituye el relleno es mayor o igual que un tamaño de 10 puntos en 10 puntos.</span><span class="sxs-lookup"><span data-stu-id="b1c3f-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 