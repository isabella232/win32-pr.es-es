---
title: Atributo de ancho VML
description: Atributo de ancho VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695651"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="fcf34-103">Atributo de ancho VML</span><span class="sxs-lookup"><span data-stu-id="fcf34-103">VML Width Attribute</span></span>

<span data-ttu-id="fcf34-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fcf34-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fcf34-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="fcf34-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fcf34-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="fcf34-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fcf34-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="fcf34-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fcf34-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fcf34-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fcf34-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fcf34-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fcf34-110">Define el ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="fcf34-110">Defines the width of the shape.</span></span> <span data-ttu-id="fcf34-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fcf34-111">Read/write.</span></span> <span data-ttu-id="fcf34-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="fcf34-112">**String**.</span></span>

<span data-ttu-id="fcf34-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="fcf34-113">**Applies To**</span></span>

[<span data-ttu-id="fcf34-114">Forma</span><span class="sxs-lookup"><span data-stu-id="fcf34-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="fcf34-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="fcf34-115">**Tag Syntax**</span></span>

<span data-ttu-id="fcf34-116"><v: *Element* style = "width: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="fcf34-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="fcf34-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="fcf34-117">**Script Syntax**</span></span>

<span data-ttu-id="fcf34-118">*Element* . Style. width = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="fcf34-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="fcf34-119">*expresión* = de *elemento*. Style. width</span><span class="sxs-lookup"><span data-stu-id="fcf34-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="fcf34-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="fcf34-120">**Remarks**</span></span>

<span data-ttu-id="fcf34-121">El atributo **ancho** es similar al atributo **ancho** HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="fcf34-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="fcf34-122">Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="fcf34-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="fcf34-123">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="fcf34-123">Values include:</span></span>



| <span data-ttu-id="fcf34-124">Value</span><span class="sxs-lookup"><span data-stu-id="fcf34-124">Value</span></span>      | <span data-ttu-id="fcf34-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcf34-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf34-126">Automático</span><span class="sxs-lookup"><span data-stu-id="fcf34-126">Auto</span></span>       | <span data-ttu-id="fcf34-127">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="fcf34-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="fcf34-128">units</span><span class="sxs-lookup"><span data-stu-id="fcf34-128">units</span></span>      | <span data-ttu-id="fcf34-129">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="fcf34-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="fcf34-130">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="fcf34-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="fcf34-131">percentage</span><span class="sxs-lookup"><span data-stu-id="fcf34-131">percentage</span></span> | <span data-ttu-id="fcf34-132">Valor expresado como porcentaje del ancho del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="fcf34-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="fcf34-133">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="fcf34-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="fcf34-134">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="fcf34-134">**See Also**</span></span>

[<span data-ttu-id="fcf34-135">Unidades</span><span class="sxs-lookup"><span data-stu-id="fcf34-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="fcf34-136">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="fcf34-136">**Example**</span></span>

<span data-ttu-id="fcf34-137">El ancho de la forma es 25.</span><span class="sxs-lookup"><span data-stu-id="fcf34-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="fcf34-138">[Ejemplo de atributo de ancho](/previous-versions/bb264101(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fcf34-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="fcf34-139">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="fcf34-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 