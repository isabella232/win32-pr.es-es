---
title: Atributo de colores VML
description: Atributo de colores VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533351"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="5cff2-103">Atributo de colores VML</span><span class="sxs-lookup"><span data-stu-id="5cff2-103">VML Colors Attribute</span></span>

<span data-ttu-id="5cff2-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5cff2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5cff2-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="5cff2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5cff2-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="5cff2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5cff2-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5cff2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5cff2-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5cff2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5cff2-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5cff2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5cff2-110">Define varios colores para un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="5cff2-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="5cff2-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5cff2-111">Read/write.</span></span> <span data-ttu-id="5cff2-112">**IVgGradientColorArray**.</span><span class="sxs-lookup"><span data-stu-id="5cff2-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="5cff2-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="5cff2-113">**Applies To**</span></span>

[<span data-ttu-id="5cff2-114">Fill</span><span class="sxs-lookup"><span data-stu-id="5cff2-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="5cff2-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="5cff2-115">**Tag Syntax**</span></span>

<span data-ttu-id="5cff2-116"><v: color de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="5cff2-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="5cff2-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="5cff2-117">**Script Syntax**</span></span>

<span data-ttu-id="5cff2-118">*Element* . Colors = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="5cff2-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="5cff2-119">*expresión* = de *Element*. Colors</span><span class="sxs-lookup"><span data-stu-id="5cff2-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="5cff2-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="5cff2-120">**Remarks**</span></span>

<span data-ttu-id="5cff2-121">Se usa para definir una matriz formada por valores emparejados de porcentajes ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) y color ([VgColor](msdn-online-vml-ivgcolor.md)).</span><span class="sxs-lookup"><span data-stu-id="5cff2-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="5cff2-122">La matriz crea un relleno mezclado usando cada punto de la matriz, empezando en 0% (definido por el **color**) y terminando en 100% (definido por el **color2**).</span><span class="sxs-lookup"><span data-stu-id="5cff2-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="5cff2-123">Los colores intermedios a lo largo del proceso se pueden definir asignando un valor de color a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5cff2-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="5cff2-124">El par de porcentaje y de color no está separado por una coma, pero los pares se separan entre sí mediante comas.</span><span class="sxs-lookup"><span data-stu-id="5cff2-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="5cff2-125">Atributo estándar de VML</span><span class="sxs-lookup"><span data-stu-id="5cff2-125">VML Standard Attribute</span></span>

<span data-ttu-id="5cff2-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5cff2-126">**Example**</span></span>

<span data-ttu-id="5cff2-127">La forma tiene un relleno de degradado que consta de cuatro colores, empezando por rojo, mezclado con amarillo, verde y finallyblue.</span><span class="sxs-lookup"><span data-stu-id="5cff2-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 