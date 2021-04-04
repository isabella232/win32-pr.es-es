---
title: Atributo LineStyle de VML
description: Atributo LineStyle de VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791721"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="86dfe-103">Atributo LineStyle de VML</span><span class="sxs-lookup"><span data-stu-id="86dfe-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="86dfe-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="86dfe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86dfe-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="86dfe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86dfe-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="86dfe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86dfe-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="86dfe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86dfe-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="86dfe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86dfe-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="86dfe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86dfe-110">Define el estilo de línea del trazo.</span><span class="sxs-lookup"><span data-stu-id="86dfe-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="86dfe-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="86dfe-111">Read/write.</span></span> <span data-ttu-id="86dfe-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="86dfe-112">**String**.</span></span>

<span data-ttu-id="86dfe-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="86dfe-113">**Applies To**</span></span>

[<span data-ttu-id="86dfe-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="86dfe-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="86dfe-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="86dfe-115">**Tag Syntax**</span></span>

<span data-ttu-id="86dfe-116"><v: *elemento* LineStyle = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="86dfe-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="86dfe-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="86dfe-117">**Script Syntax**</span></span>

<span data-ttu-id="86dfe-118">*Element* . LineStyle = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="86dfe-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="86dfe-119">*expresión* = de *elemento*. lineStyle</span><span class="sxs-lookup"><span data-stu-id="86dfe-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="86dfe-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="86dfe-120">**Remarks**</span></span>

<span data-ttu-id="86dfe-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="86dfe-121">Values include:</span></span>

-   <span data-ttu-id="86dfe-122">Single (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="86dfe-122">Single (default)</span></span>
-   <span data-ttu-id="86dfe-123">ThinThin</span><span class="sxs-lookup"><span data-stu-id="86dfe-123">ThinThin</span></span>
-   <span data-ttu-id="86dfe-124">ThinThick</span><span class="sxs-lookup"><span data-stu-id="86dfe-124">ThinThick</span></span>
-   <span data-ttu-id="86dfe-125">ThickThin</span><span class="sxs-lookup"><span data-stu-id="86dfe-125">ThickThin</span></span>
-   <span data-ttu-id="86dfe-126">ThickBetweenThin</span><span class="sxs-lookup"><span data-stu-id="86dfe-126">ThickBetweenThin</span></span>

<span data-ttu-id="86dfe-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="86dfe-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="86dfe-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="86dfe-128">**Example**</span></span>

<span data-ttu-id="86dfe-129">Se dibuja una línea doble con dos trazos finos.</span><span class="sxs-lookup"><span data-stu-id="86dfe-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 