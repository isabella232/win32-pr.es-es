---
title: En atributo (línea) (VML)
description: En atributo (línea) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793749"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="61a4f-103">En atributo (línea) (VML)</span><span class="sxs-lookup"><span data-stu-id="61a4f-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="61a4f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="61a4f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="61a4f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="61a4f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="61a4f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="61a4f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="61a4f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="61a4f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="61a4f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="61a4f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="61a4f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="61a4f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="61a4f-110">Define el punto final de una línea.</span><span class="sxs-lookup"><span data-stu-id="61a4f-110">Defines the ending point of a line.</span></span> <span data-ttu-id="61a4f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="61a4f-111">Read/write.</span></span> <span data-ttu-id="61a4f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="61a4f-112">**VgVector2D**.</span></span>

<span data-ttu-id="61a4f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="61a4f-113">**Applies To**</span></span>

[<span data-ttu-id="61a4f-114">Line</span><span class="sxs-lookup"><span data-stu-id="61a4f-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="61a4f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="61a4f-115">**Tag Syntax**</span></span>

<span data-ttu-id="61a4f-116"><v: *Element* a = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="61a4f-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="61a4f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="61a4f-117">**Script Syntax**</span></span>

<span data-ttu-id="61a4f-118">*Element* . to = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="61a4f-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="61a4f-119">*expresión* = de *elemento*. para</span><span class="sxs-lookup"><span data-stu-id="61a4f-119">*expression*=*element*.to</span></span>

<span data-ttu-id="61a4f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="61a4f-120">**Remarks**</span></span>

<span data-ttu-id="61a4f-121">Define el punto final de la línea en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="61a4f-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="61a4f-122">El valor predeterminado es 10, 10.</span><span class="sxs-lookup"><span data-stu-id="61a4f-122">Default is 10,10.</span></span>

<span data-ttu-id="61a4f-123">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="61a4f-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="61a4f-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="61a4f-124">**Example**</span></span>

<span data-ttu-id="61a4f-125">La línea finaliza en una ubicación 100 apunta hacia abajo y 100 puntos a la derecha de la esquina superior izquierda del espacio primario.</span><span class="sxs-lookup"><span data-stu-id="61a4f-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 