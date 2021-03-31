---
title: Atributo Top de VML
description: Atributo Top de VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792333"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="ad55c-103">Atributo Top de VML</span><span class="sxs-lookup"><span data-stu-id="ad55c-103">VML Top Attribute</span></span>

<span data-ttu-id="ad55c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ad55c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad55c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ad55c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad55c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ad55c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad55c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ad55c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad55c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad55c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad55c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad55c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad55c-110">Define la posición de la forma en relación con el elemento situado encima de él en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="ad55c-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="ad55c-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ad55c-111">Read/write.</span></span> <span data-ttu-id="ad55c-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="ad55c-112">**String**.</span></span>

<span data-ttu-id="ad55c-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ad55c-113">**Applies To**</span></span>

[<span data-ttu-id="ad55c-114">Forma</span><span class="sxs-lookup"><span data-stu-id="ad55c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ad55c-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ad55c-115">**Tag Syntax**</span></span>

<span data-ttu-id="ad55c-116"><v: *Element* style = "Top: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ad55c-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="ad55c-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="ad55c-117">**Script Syntax**</span></span>

<span data-ttu-id="ad55c-118">*Element* . Style.Top = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="ad55c-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="ad55c-119">*expresión* = de *elemento*. Style.Top</span><span class="sxs-lookup"><span data-stu-id="ad55c-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="ad55c-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ad55c-120">**Remarks**</span></span>

<span data-ttu-id="ad55c-121">El atributo **Top** es similar al atributo **Top** de HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="ad55c-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="ad55c-122">Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="ad55c-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="ad55c-123">Este atributo no se puede escribir para las formas alineadas en línea.</span><span class="sxs-lookup"><span data-stu-id="ad55c-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="ad55c-124">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="ad55c-124">Values include:</span></span>



| <span data-ttu-id="ad55c-125">Value</span><span class="sxs-lookup"><span data-stu-id="ad55c-125">Value</span></span>      | <span data-ttu-id="ad55c-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad55c-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad55c-127">Automático</span><span class="sxs-lookup"><span data-stu-id="ad55c-127">Auto</span></span>       | <span data-ttu-id="ad55c-128">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="ad55c-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="ad55c-129">units</span><span class="sxs-lookup"><span data-stu-id="ad55c-129">units</span></span>      | <span data-ttu-id="ad55c-130">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="ad55c-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="ad55c-131">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="ad55c-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="ad55c-132">percentage</span><span class="sxs-lookup"><span data-stu-id="ad55c-132">percentage</span></span> | <span data-ttu-id="ad55c-133">Valor expresado como porcentaje del alto del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="ad55c-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="ad55c-134">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="ad55c-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="ad55c-135">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="ad55c-135">**See Also**</span></span>

[<span data-ttu-id="ad55c-136">Unidades</span><span class="sxs-lookup"><span data-stu-id="ad55c-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="ad55c-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ad55c-137">**Example**</span></span>

<span data-ttu-id="ad55c-138">El borde superior de la forma es de 5 píxeles por debajo del objeto que lo precede en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="ad55c-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="ad55c-139">[Ejemplo de atributo Top](/previous-versions/bb264098(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ad55c-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="ad55c-140">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="ad55c-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 