---
title: Atributo de desplazamiento (sombra) (VML)
description: Atributo de desplazamiento (sombra) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995319"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="88f7e-103">Atributo de desplazamiento (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="88f7e-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="88f7e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="88f7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="88f7e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="88f7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="88f7e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="88f7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="88f7e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="88f7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="88f7e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="88f7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="88f7e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="88f7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="88f7e-110">Define hasta qué punto se extiende la sombra más allá de la forma.</span><span class="sxs-lookup"><span data-stu-id="88f7e-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="88f7e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="88f7e-111">Read/write.</span></span> <span data-ttu-id="88f7e-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="88f7e-112">**VgVector2D**.</span></span>

<span data-ttu-id="88f7e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="88f7e-113">**Applies To**</span></span>

[<span data-ttu-id="88f7e-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="88f7e-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="88f7e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="88f7e-115">**Tag Syntax**</span></span>

<span data-ttu-id="88f7e-116"><v: *elemento* offset = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="88f7e-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="88f7e-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="88f7e-117">**Script Syntax**</span></span>

<span data-ttu-id="88f7e-118">*Element* . offset = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="88f7e-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="88f7e-119">*expresión* = de *Element*. offset</span><span class="sxs-lookup"><span data-stu-id="88f7e-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="88f7e-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="88f7e-120">**Remarks**</span></span>

<span data-ttu-id="88f7e-121">El desplazamiento predeterminado para el valor x es 2PT y el valor predeterminado para el valor y es 2PT.</span><span class="sxs-lookup"><span data-stu-id="88f7e-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="88f7e-122">Los valores son una medida absoluta o un valor fraccionario de forma.</span><span class="sxs-lookup"><span data-stu-id="88f7e-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="88f7e-123">Si es fraccionario, van del 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="88f7e-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="88f7e-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="88f7e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="88f7e-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="88f7e-125">**Example**</span></span>

<span data-ttu-id="88f7e-126">La forma tiene una sombra con un desplazamiento de 5 puntos hacia abajo y 10 puntos a la derecha.</span><span class="sxs-lookup"><span data-stu-id="88f7e-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 