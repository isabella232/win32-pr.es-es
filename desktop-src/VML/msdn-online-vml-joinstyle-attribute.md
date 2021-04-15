---
title: Atributo JoinStyle de VML
description: Atributo JoinStyle de VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695668"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="7ec0b-103">Atributo JoinStyle de VML</span><span class="sxs-lookup"><span data-stu-id="7ec0b-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="7ec0b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7ec0b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7ec0b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7ec0b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7ec0b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7ec0b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7ec0b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7ec0b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7ec0b-110">Define el estilo de combinación de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="7ec0b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7ec0b-111">Read/write.</span></span> <span data-ttu-id="7ec0b-112">String.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-112">String.</span></span>

<span data-ttu-id="7ec0b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="7ec0b-113">**Applies To**</span></span>

[<span data-ttu-id="7ec0b-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7ec0b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7ec0b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="7ec0b-115">**Tag Syntax**</span></span>

<span data-ttu-id="7ec0b-116"><v: *Element* joinstyle = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="7ec0b-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="7ec0b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="7ec0b-117">**Script Syntax**</span></span>

<span data-ttu-id="7ec0b-118">*Element* . joinstyle = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="7ec0b-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="7ec0b-119">*expresión* = de *elemento*. joinstyle</span><span class="sxs-lookup"><span data-stu-id="7ec0b-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="7ec0b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="7ec0b-120">**Remarks**</span></span>

<span data-ttu-id="7ec0b-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="7ec0b-121">Values include:</span></span>

-   <span data-ttu-id="7ec0b-122">Round (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="7ec0b-122">round (default)</span></span>
-   <span data-ttu-id="7ec0b-123">parezca</span><span class="sxs-lookup"><span data-stu-id="7ec0b-123">bevel</span></span>
-   <span data-ttu-id="7ec0b-124">ángulo</span><span class="sxs-lookup"><span data-stu-id="7ec0b-124">miter</span></span>

<span data-ttu-id="7ec0b-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="7ec0b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="7ec0b-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="7ec0b-126">**Example**</span></span>

<span data-ttu-id="7ec0b-127">Los empalmes de la polilínea están biselados.</span><span class="sxs-lookup"><span data-stu-id="7ec0b-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 