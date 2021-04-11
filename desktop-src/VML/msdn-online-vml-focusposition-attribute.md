---
title: Atributo FocusPosition de VML
description: Atributo FocusPosition de VML
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149612"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="99370-103">Atributo FocusPosition de VML</span><span class="sxs-lookup"><span data-stu-id="99370-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="99370-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="99370-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="99370-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="99370-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="99370-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="99370-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="99370-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="99370-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="99370-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="99370-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="99370-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="99370-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="99370-110">Define el centro de un degradado radial.</span><span class="sxs-lookup"><span data-stu-id="99370-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="99370-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="99370-111">Read/write.</span></span> <span data-ttu-id="99370-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="99370-112">**VgVector2D**.</span></span>

<span data-ttu-id="99370-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="99370-113">**Applies To**</span></span>

[<span data-ttu-id="99370-114">Fill</span><span class="sxs-lookup"><span data-stu-id="99370-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="99370-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="99370-115">**Tag Syntax**</span></span>

<span data-ttu-id="99370-116"><v: *Element* focusposition = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="99370-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="99370-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="99370-117">**Script Syntax**</span></span>

<span data-ttu-id="99370-118">*Element* . focusposition = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="99370-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="99370-119">*expresión* = de *elemento*. focusposition</span><span class="sxs-lookup"><span data-stu-id="99370-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="99370-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="99370-120">**Remarks**</span></span>

<span data-ttu-id="99370-121">Especifica los degradados radiales del centro positionfor.</span><span class="sxs-lookup"><span data-stu-id="99370-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="99370-122">El vector es una fracción del ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="99370-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="99370-123">El primero es un porcentaje del relleno en el borde izquierdo; el segundo es un porcentaje del relleno en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="99370-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="99370-124">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="99370-124">The default value is 0,0.</span></span> <span data-ttu-id="99370-125">Para colocar un relleno radial en el centro de una forma, use el valor del 50%, 50%.</span><span class="sxs-lookup"><span data-stu-id="99370-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="99370-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="99370-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="99370-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="99370-127">**Example**</span></span>

<span data-ttu-id="99370-128">El relleno radial se centrará de modo que el azul se inicie en el centro y Radiate hacia afuera, cambiando gradualmente a rojo en el momento en que alcance los bordes y las esquinas exteriores.</span><span class="sxs-lookup"><span data-stu-id="99370-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 