---
title: Atributo FillType de VML
description: Atributo FillType de VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995606"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="23c61-103">Atributo FillType de VML</span><span class="sxs-lookup"><span data-stu-id="23c61-103">VML FillType Attribute</span></span>

<span data-ttu-id="23c61-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="23c61-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="23c61-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="23c61-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="23c61-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="23c61-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="23c61-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="23c61-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="23c61-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="23c61-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="23c61-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="23c61-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="23c61-110">Define el tipo de relleno utilizado para el fondo de un trazo.</span><span class="sxs-lookup"><span data-stu-id="23c61-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="23c61-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="23c61-111">Read/write.</span></span> <span data-ttu-id="23c61-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="23c61-112">**VgFillType**.</span></span>

<span data-ttu-id="23c61-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="23c61-113">**Applies To**</span></span>

[<span data-ttu-id="23c61-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="23c61-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="23c61-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="23c61-115">**Tag Syntax**</span></span>

<span data-ttu-id="23c61-116"><v: *Element* filltype = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="23c61-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="23c61-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="23c61-117">**Script Syntax**</span></span>

<span data-ttu-id="23c61-118">*Element* . filltype = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="23c61-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="23c61-119">*expresión* = de *elemento*. filltype</span><span class="sxs-lookup"><span data-stu-id="23c61-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="23c61-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="23c61-120">**Remarks**</span></span>

<span data-ttu-id="23c61-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="23c61-121">Values include:</span></span>



| <span data-ttu-id="23c61-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="23c61-122">DashStyle</span></span> | <span data-ttu-id="23c61-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="23c61-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="23c61-124">Sólido</span><span class="sxs-lookup"><span data-stu-id="23c61-124">Solid</span></span>     | <span data-ttu-id="23c61-125">El patrón de relleno es sólido.</span><span class="sxs-lookup"><span data-stu-id="23c61-125">The fill pattern is solid.</span></span> <span data-ttu-id="23c61-126">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="23c61-126">Default value.</span></span>      |
| <span data-ttu-id="23c61-127">Tile</span><span class="sxs-lookup"><span data-stu-id="23c61-127">Tile</span></span>      | <span data-ttu-id="23c61-128">La imagen de relleno está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="23c61-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="23c61-129">Patrón</span><span class="sxs-lookup"><span data-stu-id="23c61-129">Pattern</span></span>   | <span data-ttu-id="23c61-130">La imagen de relleno se ajusta para formar un patrón.</span><span class="sxs-lookup"><span data-stu-id="23c61-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="23c61-131">Fotograma</span><span class="sxs-lookup"><span data-stu-id="23c61-131">Frame</span></span>     | <span data-ttu-id="23c61-132">La imagen de relleno se convierte en un borde para la forma.</span><span class="sxs-lookup"><span data-stu-id="23c61-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="23c61-133">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="23c61-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="23c61-134">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="23c61-134">**Example**</span></span>

<span data-ttu-id="23c61-135">El trazo de la forma tiene una textura en mosaico creada a partir de la imagen de cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="23c61-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 