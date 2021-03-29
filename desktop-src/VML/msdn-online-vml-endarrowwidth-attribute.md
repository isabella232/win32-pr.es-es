---
title: Atributo EndArrowWidth de VML
description: Atributo EndArrowWidth de VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793767"
---
# <a name="vml-endarrowwidth-attribute"></a><span data-ttu-id="0ce60-103">Atributo EndArrowWidth de VML</span><span class="sxs-lookup"><span data-stu-id="0ce60-103">VML EndArrowWidth Attribute</span></span>

<span data-ttu-id="0ce60-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0ce60-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0ce60-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0ce60-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0ce60-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0ce60-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0ce60-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0ce60-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0ce60-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0ce60-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0ce60-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0ce60-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0ce60-110">Define un ancho de la punta de flecha para el final de una línea.</span><span class="sxs-lookup"><span data-stu-id="0ce60-110">Defines an arrowhead width for the end of a line.</span></span> <span data-ttu-id="0ce60-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0ce60-111">Read/write.</span></span> <span data-ttu-id="0ce60-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="0ce60-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="0ce60-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0ce60-113">**Applies To**</span></span>

[<span data-ttu-id="0ce60-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="0ce60-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0ce60-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0ce60-115">**Tag Syntax**</span></span>

<span data-ttu-id="0ce60-116"><v: *Element* endarrowwidth = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0ce60-116"><v: *element* endarrowwidth=" *expression* "></span></span>

<span data-ttu-id="0ce60-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0ce60-117">**Script Syntax**</span></span>

<span data-ttu-id="0ce60-118">*Element* . endarrowwidth = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="0ce60-118">*element* .endarrowwidth="*expression*"</span></span>

<span data-ttu-id="0ce60-119">*expresión* = de *elemento*. endarrowwidth</span><span class="sxs-lookup"><span data-stu-id="0ce60-119">*expression*=*element*.endarrowwidth</span></span>

<span data-ttu-id="0ce60-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0ce60-120">**Remarks**</span></span>

<span data-ttu-id="0ce60-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="0ce60-121">Values include:</span></span>

-   <span data-ttu-id="0ce60-122">Restrictiv</span><span class="sxs-lookup"><span data-stu-id="0ce60-122">Narrow</span></span>
-   <span data-ttu-id="0ce60-123">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="0ce60-123">Medium (default)</span></span>
-   <span data-ttu-id="0ce60-124">Ancho</span><span class="sxs-lookup"><span data-stu-id="0ce60-124">Wide</span></span>

<span data-ttu-id="0ce60-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0ce60-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="0ce60-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0ce60-126">**Example**</span></span>

<span data-ttu-id="0ce60-127">Una línea se dibuja con una punta de flecha clásica ancha en el extremo del trazo.</span><span class="sxs-lookup"><span data-stu-id="0ce60-127">A line is drawn with a wide classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 