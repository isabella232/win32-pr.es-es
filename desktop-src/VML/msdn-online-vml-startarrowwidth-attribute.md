---
title: Atributo StartArrowWidth de VML
description: Atributo StartArrowWidth de VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792555"
---
# <a name="vml-startarrowwidth-attribute"></a><span data-ttu-id="fb19d-103">Atributo StartArrowWidth de VML</span><span class="sxs-lookup"><span data-stu-id="fb19d-103">VML StartArrowWidth Attribute</span></span>

<span data-ttu-id="fb19d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fb19d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fb19d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="fb19d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fb19d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="fb19d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fb19d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="fb19d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fb19d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fb19d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fb19d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fb19d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fb19d-110">Define el ancho de la punta de flecha para el inicio de una línea.</span><span class="sxs-lookup"><span data-stu-id="fb19d-110">Defines the arrowhead width for the start of a line.</span></span> <span data-ttu-id="fb19d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fb19d-111">Read/write.</span></span> <span data-ttu-id="fb19d-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="fb19d-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="fb19d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="fb19d-113">**Applies To**</span></span>

[<span data-ttu-id="fb19d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="fb19d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="fb19d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="fb19d-115">**Tag Syntax**</span></span>

<span data-ttu-id="fb19d-116"><v: *Element* startarrowwidth = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="fb19d-116"><v: *element* startarrowwidth=" *expression* "></span></span>

<span data-ttu-id="fb19d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="fb19d-117">**Script Syntax**</span></span>

<span data-ttu-id="fb19d-118">*Element* . startarrowwidth = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="fb19d-118">*element* .startarrowwidth="*expression*"</span></span>

<span data-ttu-id="fb19d-119">*expresión* = de *elemento*. startarrowwidth</span><span class="sxs-lookup"><span data-stu-id="fb19d-119">*expression*=*element*.startarrowwidth</span></span>

<span data-ttu-id="fb19d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="fb19d-120">**Remarks**</span></span>

<span data-ttu-id="fb19d-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="fb19d-121">Values include:</span></span>

-   <span data-ttu-id="fb19d-122">Restrictiv</span><span class="sxs-lookup"><span data-stu-id="fb19d-122">Narrow</span></span>
-   <span data-ttu-id="fb19d-123">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="fb19d-123">Medium (default)</span></span>
-   <span data-ttu-id="fb19d-124">Ancho</span><span class="sxs-lookup"><span data-stu-id="fb19d-124">Wide</span></span>

<span data-ttu-id="fb19d-125">Atributo estándar de VML</span><span class="sxs-lookup"><span data-stu-id="fb19d-125">VML Standard Attribute</span></span>

<span data-ttu-id="fb19d-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="fb19d-126">**Example**</span></span>

<span data-ttu-id="fb19d-127">Una línea se dibuja con una punta de flecha clásica ancha en el inicio del trazo.</span><span class="sxs-lookup"><span data-stu-id="fb19d-127">A line is drawn with a wide classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 