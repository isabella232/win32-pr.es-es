---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078345"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="dc65a-103">Atributo FocusSize de VML</span><span class="sxs-lookup"><span data-stu-id="dc65a-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="dc65a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dc65a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dc65a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="dc65a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dc65a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="dc65a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dc65a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="dc65a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dc65a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dc65a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dc65a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dc65a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dc65a-110">Define el tamaño del foco para los rellenos radiales.</span><span class="sxs-lookup"><span data-stu-id="dc65a-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="dc65a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc65a-111">Read/write.</span></span> <span data-ttu-id="dc65a-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="dc65a-112">**VgVector2D**.</span></span>

<span data-ttu-id="dc65a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="dc65a-113">**Applies To**</span></span>

[<span data-ttu-id="dc65a-114">Fill</span><span class="sxs-lookup"><span data-stu-id="dc65a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="dc65a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="dc65a-115">**Tag Syntax**</span></span>

<span data-ttu-id="dc65a-116"><v: *Element* focussize = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="dc65a-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="dc65a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="dc65a-117">**Script Syntax**</span></span>

<span data-ttu-id="dc65a-118">*Element* . focussize = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="dc65a-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="dc65a-119">*expresión* = de *elemento*. focussize</span><span class="sxs-lookup"><span data-stu-id="dc65a-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="dc65a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="dc65a-120">**Remarks**</span></span>

<span data-ttu-id="dc65a-121">Los valores son fracciones del ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="dc65a-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="dc65a-122">El primero es un porcentaje del relleno en el borde derecho de la forma y el segundo es un porcentaje del relleno en la parte inferior de la forma.</span><span class="sxs-lookup"><span data-stu-id="dc65a-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="dc65a-123">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="dc65a-123">The default value is 0,0.</span></span> <span data-ttu-id="dc65a-124">Un valor **FocusSize** de 100%, 100% y un **FocusPosition** de 0, 0 haría que el color2 dominara por completo la combinación.</span><span class="sxs-lookup"><span data-stu-id="dc65a-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="dc65a-125">Se recomiendan valores pequeños de aproximadamente el 10%, 10% para las combinaciones equilibradas.</span><span class="sxs-lookup"><span data-stu-id="dc65a-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="dc65a-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="dc65a-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="dc65a-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="dc65a-127">**Example**</span></span>

<span data-ttu-id="dc65a-128">El relleno radial creará una mezcla empezando en el centro como azul y se convertirá en rojo en los cuatro bordes.</span><span class="sxs-lookup"><span data-stu-id="dc65a-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="dc65a-129">El centro de la mezcla está definido por **FocusPosition** y el tamaño del color inicial interior viene determinado por **FocusSize**.</span><span class="sxs-lookup"><span data-stu-id="dc65a-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 