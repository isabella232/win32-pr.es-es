---
title: En atributo (curva) (VML)
description: En atributo (curva) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904813"
---
# <a name="to-attribute-curvevml"></a><span data-ttu-id="3ca9f-103">En atributo (curva) (VML)</span><span class="sxs-lookup"><span data-stu-id="3ca9f-103">To Attribute (Curve)(VML)</span></span>

<span data-ttu-id="3ca9f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ca9f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ca9f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ca9f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ca9f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ca9f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ca9f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ca9f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ca9f-110">Define el punto final de una curva.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-110">Defines the ending point of a curve.</span></span> <span data-ttu-id="3ca9f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3ca9f-111">Read/write.</span></span> <span data-ttu-id="3ca9f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-112">**VgVector2D**.</span></span>

<span data-ttu-id="3ca9f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-113">**Applies To**</span></span>

[<span data-ttu-id="3ca9f-114">Sensible</span><span class="sxs-lookup"><span data-stu-id="3ca9f-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="3ca9f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ca9f-116"><v: *Element* a = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3ca9f-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="3ca9f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-117">**Script Syntax**</span></span>

<span data-ttu-id="3ca9f-118">*Element* . to = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3ca9f-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="3ca9f-119">*expresión* = de *elemento*. para</span><span class="sxs-lookup"><span data-stu-id="3ca9f-119">*expression*=*element*.to</span></span>

<span data-ttu-id="3ca9f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-120">**Remarks**</span></span>

<span data-ttu-id="3ca9f-121">Define el punto final de una curva Bézier cúbica en el espacio de coordenadas del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-121">Defines the ending point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="3ca9f-122">Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="3ca9f-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="3ca9f-123">El valor predeterminado es 30, 20.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-123">Default is 30,20.</span></span>

<span data-ttu-id="3ca9f-124">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-124">**VML Standard Attribute**</span></span>

<span data-ttu-id="3ca9f-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3ca9f-125">**Example**</span></span>

<span data-ttu-id="3ca9f-126">La curva es sonriente.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-126">The curve is smiling.</span></span> <span data-ttu-id="3ca9f-127">Comienza a la izquierda y termina a la derecha.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="3ca9f-128">Los dos puntos de control se sitúan a lo largo del modo de extraer la curva para dar la apariencia de una sonrisa.</span><span class="sxs-lookup"><span data-stu-id="3ca9f-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 