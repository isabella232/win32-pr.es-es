---
title: Del atributo (línea) (VML)
description: Del atributo (línea) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793654"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="7ad09-103">Del atributo (línea) (VML)</span><span class="sxs-lookup"><span data-stu-id="7ad09-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="7ad09-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7ad09-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7ad09-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7ad09-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7ad09-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7ad09-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7ad09-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7ad09-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7ad09-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7ad09-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7ad09-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7ad09-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7ad09-110">Define el punto inicial de una línea.</span><span class="sxs-lookup"><span data-stu-id="7ad09-110">Defines the starting point of a line.</span></span> <span data-ttu-id="7ad09-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7ad09-111">Read/write.</span></span> <span data-ttu-id="7ad09-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7ad09-112">**VgVector2D**.</span></span>

<span data-ttu-id="7ad09-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="7ad09-113">**Applies To**</span></span>

[<span data-ttu-id="7ad09-114">Line</span><span class="sxs-lookup"><span data-stu-id="7ad09-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="7ad09-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="7ad09-115">**Tag Syntax**</span></span>

<span data-ttu-id="7ad09-116"><v: *Element* from = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="7ad09-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="7ad09-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="7ad09-117">**Script Syntax**</span></span>

<span data-ttu-id="7ad09-118">*Element* . from = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="7ad09-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="7ad09-119">*expresión* = de *elemento*. from</span><span class="sxs-lookup"><span data-stu-id="7ad09-119">*expression*=*element*.from</span></span>

<span data-ttu-id="7ad09-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="7ad09-120">**Remarks**</span></span>

<span data-ttu-id="7ad09-121">Define el punto inicial de la línea en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="7ad09-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="7ad09-122">El valor predeterminado es 0, 0.</span><span class="sxs-lookup"><span data-stu-id="7ad09-122">Default is 0,0.</span></span>

<span data-ttu-id="7ad09-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="7ad09-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7ad09-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="7ad09-124">**Example**</span></span>

<span data-ttu-id="7ad09-125">La línea comienza en una ubicación de 10 puntos hacia abajo y 10 puntos a la derecha de la esquina superior izquierda del espacio primario.</span><span class="sxs-lookup"><span data-stu-id="7ad09-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 