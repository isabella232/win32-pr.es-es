---
title: Atributo StrokeColor de VML
description: Atributo StrokeColor de VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077912"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="79f12-103">Atributo StrokeColor de VML</span><span class="sxs-lookup"><span data-stu-id="79f12-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="79f12-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="79f12-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="79f12-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="79f12-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="79f12-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="79f12-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="79f12-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="79f12-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="79f12-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="79f12-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="79f12-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="79f12-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="79f12-110">Define el color del pincel que traza el trazado de una forma.</span><span class="sxs-lookup"><span data-stu-id="79f12-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="79f12-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79f12-111">Read/write.</span></span> <span data-ttu-id="79f12-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="79f12-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="79f12-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="79f12-113">**Applies To**</span></span>

[<span data-ttu-id="79f12-114">Forma</span><span class="sxs-lookup"><span data-stu-id="79f12-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="79f12-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="79f12-115">**Tag Syntax**</span></span>

<span data-ttu-id="79f12-116"><v: *Element* StrokeColor = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="79f12-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="79f12-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="79f12-117">**Script Syntax**</span></span>

<span data-ttu-id="79f12-118">*Element* . StrokeColor = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="79f12-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="79f12-119">*expresión* = de *elemento*. StrokeColor</span><span class="sxs-lookup"><span data-stu-id="79f12-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="79f12-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="79f12-120">**Remarks**</span></span>

<span data-ttu-id="79f12-121">El valor se duplica desde el atributo **color** del elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="79f12-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="79f12-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="79f12-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="79f12-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="79f12-123">**Example**</span></span>

<span data-ttu-id="79f12-124">El color del trazo del rectángulo es rojo.</span><span class="sxs-lookup"><span data-stu-id="79f12-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="79f12-125">[Ejemplo del atributo StrokeColor](/previous-versions/bb264093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79f12-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="79f12-126">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="79f12-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 