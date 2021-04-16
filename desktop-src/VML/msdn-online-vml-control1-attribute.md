---
title: Atributo Control1 de VML
description: Atributo Control1 de VML
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676381"
---
# <a name="vml-control1-attribute"></a><span data-ttu-id="db98b-103">Atributo Control1 de VML</span><span class="sxs-lookup"><span data-stu-id="db98b-103">VML Control1 Attribute</span></span>

<span data-ttu-id="db98b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="db98b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="db98b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="db98b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="db98b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="db98b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="db98b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="db98b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="db98b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="db98b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="db98b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="db98b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="db98b-110">Define el primer punto de control de una curva Bézier.</span><span class="sxs-lookup"><span data-stu-id="db98b-110">Defines the first control point of a bezier curve.</span></span> <span data-ttu-id="db98b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="db98b-111">Read/write.</span></span> <span data-ttu-id="db98b-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="db98b-112">**VgVector2D**.</span></span>

<span data-ttu-id="db98b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="db98b-113">**Applies To**</span></span>

[<span data-ttu-id="db98b-114">Sensible</span><span class="sxs-lookup"><span data-stu-id="db98b-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="db98b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="db98b-115">**Tag Syntax**</span></span>

<span data-ttu-id="db98b-116"><v: *Element* Control1 = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="db98b-116"><v: *element* control1=" *expression* "></span></span>

<span data-ttu-id="db98b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="db98b-117">**Script Syntax**</span></span>

<span data-ttu-id="db98b-118">*Element* . Control1 = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="db98b-118">*element* .control1="*expression*"</span></span>

<span data-ttu-id="db98b-119">*expresión* = de *elemento*. Control1</span><span class="sxs-lookup"><span data-stu-id="db98b-119">*expression*=*element*.control1</span></span>

<span data-ttu-id="db98b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="db98b-120">**Remarks**</span></span>

<span data-ttu-id="db98b-121">Define el primer punto de control de una curva Bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="db98b-121">Defines the first control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="db98b-122">El valor predeterminado es 10, 10.</span><span class="sxs-lookup"><span data-stu-id="db98b-122">Default is 10,10.</span></span>

<span data-ttu-id="db98b-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="db98b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="db98b-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="db98b-124">**Example**</span></span>

<span data-ttu-id="db98b-125">La curva es sonriente.</span><span class="sxs-lookup"><span data-stu-id="db98b-125">The curve is smiling.</span></span> <span data-ttu-id="db98b-126">Comienza a la izquierda y termina a la derecha.</span><span class="sxs-lookup"><span data-stu-id="db98b-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="db98b-127">Los dos puntos de control se sitúan a lo largo del modo de extraer la curva para dar la apariencia de una sonrisa.</span><span class="sxs-lookup"><span data-stu-id="db98b-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 