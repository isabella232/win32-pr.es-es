---
title: Atributo de trazado VML
description: Atributo de trazado VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149590"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="86cb9-103">Atributo de trazado VML</span><span class="sxs-lookup"><span data-stu-id="86cb9-103">VML Stroked Attribute</span></span>

<span data-ttu-id="86cb9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="86cb9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86cb9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="86cb9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86cb9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="86cb9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86cb9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="86cb9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86cb9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="86cb9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86cb9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="86cb9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86cb9-110">Define si se va a trazar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="86cb9-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="86cb9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="86cb9-111">Read/write.</span></span> <span data-ttu-id="86cb9-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="86cb9-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="86cb9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="86cb9-113">**Applies To**</span></span>

[<span data-ttu-id="86cb9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="86cb9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="86cb9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="86cb9-115">**Tag Syntax**</span></span>

<span data-ttu-id="86cb9-116"><v: *elemento* stroked = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="86cb9-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="86cb9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="86cb9-117">**Script Syntax**</span></span>

<span data-ttu-id="86cb9-118">*Element* . stroked = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="86cb9-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="86cb9-119">*expresión* = de *elemento*. stroked</span><span class="sxs-lookup"><span data-stu-id="86cb9-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="86cb9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="86cb9-120">**Remarks**</span></span>

<span data-ttu-id="86cb9-121">El valor se duplica desde el atributo **on** del elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="86cb9-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="86cb9-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="86cb9-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="86cb9-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="86cb9-123">**Example**</span></span>

<span data-ttu-id="86cb9-124">La ruta de acceso de la forma se traza.</span><span class="sxs-lookup"><span data-stu-id="86cb9-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="86cb9-125">[Ejemplo de atributo de trazo](/previous-versions/bb264094(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86cb9-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="86cb9-126">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="86cb9-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 