---
title: Atributo izquierdo de VML
description: Atributo izquierdo de VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488175"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="c5c07-103">Atributo izquierdo de VML</span><span class="sxs-lookup"><span data-stu-id="c5c07-103">VML Left Attribute</span></span>

<span data-ttu-id="c5c07-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5c07-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5c07-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c5c07-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5c07-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="c5c07-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5c07-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c5c07-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5c07-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5c07-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5c07-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5c07-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5c07-110">Determina la posición de la forma en relación con el elemento que queda en el flujo del documento.</span><span class="sxs-lookup"><span data-stu-id="c5c07-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="c5c07-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c5c07-111">Read/write.</span></span> <span data-ttu-id="c5c07-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="c5c07-112">**String**.</span></span>

<span data-ttu-id="c5c07-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="c5c07-113">**Applies To**</span></span>

[<span data-ttu-id="c5c07-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c5c07-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c5c07-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="c5c07-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5c07-116"><v: *Element* style = "Left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c5c07-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="c5c07-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="c5c07-117">**Script Syntax**</span></span>

<span data-ttu-id="c5c07-118">*Element* . Style. Left = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="c5c07-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="c5c07-119">*expresión* = de *Element*. Style. Left</span><span class="sxs-lookup"><span data-stu-id="c5c07-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="c5c07-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="c5c07-120">**Remarks**</span></span>

<span data-ttu-id="c5c07-121">El atributo **izquierdo** es similar al atributo **izquierdo** HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="c5c07-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="c5c07-122">Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="c5c07-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="c5c07-123">Este atributo no se escribirá para las formas insertadas en línea.</span><span class="sxs-lookup"><span data-stu-id="c5c07-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="c5c07-124">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="c5c07-124">Values include:</span></span>



| <span data-ttu-id="c5c07-125">Value</span><span class="sxs-lookup"><span data-stu-id="c5c07-125">Value</span></span>      | <span data-ttu-id="c5c07-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5c07-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c07-127">Automático</span><span class="sxs-lookup"><span data-stu-id="c5c07-127">Auto</span></span>       | <span data-ttu-id="c5c07-128">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="c5c07-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="c5c07-129">units</span><span class="sxs-lookup"><span data-stu-id="c5c07-129">units</span></span>      | <span data-ttu-id="c5c07-130">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="c5c07-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="c5c07-131">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="c5c07-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="c5c07-132">percentage</span><span class="sxs-lookup"><span data-stu-id="c5c07-132">percentage</span></span> | <span data-ttu-id="c5c07-133">Valor expresado como porcentaje del ancho del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="c5c07-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="c5c07-134">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="c5c07-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="c5c07-135">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="c5c07-135">**See Also**</span></span>

[<span data-ttu-id="c5c07-136">Unidades</span><span class="sxs-lookup"><span data-stu-id="c5c07-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="c5c07-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="c5c07-137">**Example**</span></span>

<span data-ttu-id="c5c07-138">El valor izquierdo de la forma se establece en 1 en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c5c07-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="c5c07-139">[Ejemplo de atributo](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md)de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="c5c07-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="c5c07-140">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="c5c07-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 