---
title: Atributo FillColor de VML
description: Atributo FillColor de VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695748"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="565ce-103">Atributo FillColor de VML</span><span class="sxs-lookup"><span data-stu-id="565ce-103">VML FillColor Attribute</span></span>

<span data-ttu-id="565ce-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="565ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="565ce-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="565ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="565ce-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="565ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="565ce-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="565ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="565ce-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="565ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="565ce-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="565ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="565ce-110">Define el color del pincel que rellena la ruta de acceso cerrada de una forma.</span><span class="sxs-lookup"><span data-stu-id="565ce-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="565ce-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="565ce-111">Read/write.</span></span> <span data-ttu-id="565ce-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="565ce-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="565ce-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="565ce-113">**Applies To**</span></span>

[<span data-ttu-id="565ce-114">Forma</span><span class="sxs-lookup"><span data-stu-id="565ce-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="565ce-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="565ce-115">**Tag Syntax**</span></span>

<span data-ttu-id="565ce-116"><v: *elemento* fillColor = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="565ce-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="565ce-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="565ce-117">**Script Syntax**</span></span>

<span data-ttu-id="565ce-118">*Element* . fillColor = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="565ce-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="565ce-119">*expresión* = de *elemento*. colorderelleno</span><span class="sxs-lookup"><span data-stu-id="565ce-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="565ce-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="565ce-120">**Remarks**</span></span>

<span data-ttu-id="565ce-121">El valor de **fillColor** se duplica desde el atributo **color** del elemento **Fill** .</span><span class="sxs-lookup"><span data-stu-id="565ce-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="565ce-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="565ce-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="565ce-123">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="565ce-123">**See Also**</span></span>

<span data-ttu-id="565ce-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="565ce-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="565ce-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="565ce-125">**Example**</span></span>

<span data-ttu-id="565ce-126">El color de relleno del rectángulo es rojo.</span><span class="sxs-lookup"><span data-stu-id="565ce-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="565ce-127">[Ejemplo del atributo fillColor](/previous-versions/bb229668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="565ce-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="565ce-128">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="565ce-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 