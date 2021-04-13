---
title: Atributo rellenado de VML
description: Atributo rellenado de VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488255"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="cd71b-103">Atributo rellenado de VML</span><span class="sxs-lookup"><span data-stu-id="cd71b-103">VML Filled Attribute</span></span>

<span data-ttu-id="cd71b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cd71b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cd71b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="cd71b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cd71b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="cd71b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cd71b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="cd71b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cd71b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cd71b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cd71b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cd71b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cd71b-110">Determina si la ruta de acceso cerrada se rellenará.</span><span class="sxs-lookup"><span data-stu-id="cd71b-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="cd71b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cd71b-111">Read/write.</span></span> <span data-ttu-id="cd71b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="cd71b-112">**VgTriState**.</span></span>

<span data-ttu-id="cd71b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="cd71b-113">**Applies To**</span></span>

[<span data-ttu-id="cd71b-114">Forma</span><span class="sxs-lookup"><span data-stu-id="cd71b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cd71b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="cd71b-115">**Tag Syntax**</span></span>

<span data-ttu-id="cd71b-116"><v: *elemento* filled = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="cd71b-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="cd71b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="cd71b-117">**Script Syntax**</span></span>

<span data-ttu-id="cd71b-118">*Element* . filled = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="cd71b-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="cd71b-119">*expresión* = de *elemento*. filled</span><span class="sxs-lookup"><span data-stu-id="cd71b-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="cd71b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="cd71b-120">**Remarks**</span></span>

<span data-ttu-id="cd71b-121">El valor se duplica desde el atributo **on** del elemento [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cd71b-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="cd71b-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="cd71b-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="cd71b-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="cd71b-123">**Example**</span></span>

<span data-ttu-id="cd71b-124">Se rellena la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="cd71b-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="cd71b-125">[Ejemplo de atributo rellenado](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd71b-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="cd71b-126">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="cd71b-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 