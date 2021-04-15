---
title: Atributo de la interseción de VML
description: Atributo de la interseción de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695674"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="70388-103">Atributo de la interseción de VML</span><span class="sxs-lookup"><span data-stu-id="70388-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="70388-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70388-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70388-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="70388-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70388-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="70388-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70388-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="70388-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70388-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="70388-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70388-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="70388-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70388-110">Define la cantidad de redondeo de un rectángulo redondeado.</span><span class="sxs-lookup"><span data-stu-id="70388-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="70388-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="70388-111">Read/write.</span></span> <span data-ttu-id="70388-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="70388-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="70388-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="70388-113">**Applies To**</span></span>

[<span data-ttu-id="70388-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="70388-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="70388-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="70388-115">**Tag Syntax**</span></span>

<span data-ttu-id="70388-116"><v: *elemento* -arcos = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="70388-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="70388-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="70388-117">**Script Syntax**</span></span>

<span data-ttu-id="70388-118">*Element* . arcos = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="70388-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="70388-119">*expresión* = de *elemento*. arcos</span><span class="sxs-lookup"><span data-stu-id="70388-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="70388-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="70388-120">**Remarks**</span></span>

<span data-ttu-id="70388-121">Define las esquinas redondeadas de un rectángulo redondeado como un porcentaje de la mitad de la dimensión más pequeña de la longitud y el ancho de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="70388-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="70388-122">0% tendría esquinas cuadradas y el 100% formaría esquinas circulares.</span><span class="sxs-lookup"><span data-stu-id="70388-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="70388-123">Un cuadrado con un **valor de** un valor de entre valores 1,0 sería un círculo.</span><span class="sxs-lookup"><span data-stu-id="70388-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="70388-124">El valor predeterminado es 0,2 (20%).</span><span class="sxs-lookup"><span data-stu-id="70388-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="70388-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="70388-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="70388-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="70388-126">**Example**</span></span>

<span data-ttu-id="70388-127">El rectángulo redondeado se dibuja con esquinas estrechas pero redondeadas.</span><span class="sxs-lookup"><span data-stu-id="70388-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 