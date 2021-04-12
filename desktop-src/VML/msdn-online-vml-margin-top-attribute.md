---
title: Atributo de Margin-Top VML
description: Atributo de Margin-Top VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359397"
---
# <a name="vml-margin-top-attribute"></a><span data-ttu-id="a7245-103">Atributo de Margin-Top VML</span><span class="sxs-lookup"><span data-stu-id="a7245-103">VML Margin-Top Attribute</span></span>

<span data-ttu-id="a7245-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7245-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7245-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a7245-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a7245-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a7245-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7245-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a7245-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7245-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7245-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7245-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7245-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a7245-110">Especifica el borde superior del rectángulo que contiene la forma en relación con el delimitador de la forma.</span><span class="sxs-lookup"><span data-stu-id="a7245-110">Specifies the top edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="a7245-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a7245-111">Read/write.</span></span> <span data-ttu-id="a7245-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="a7245-112">**String**.</span></span>

<span data-ttu-id="a7245-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a7245-113">**Applies To**</span></span>

[<span data-ttu-id="a7245-114">Forma</span><span class="sxs-lookup"><span data-stu-id="a7245-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a7245-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a7245-115">**Tag Syntax**</span></span>

<span data-ttu-id="a7245-116"><v: *elemento* margin-top = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a7245-116"><v: *element* margin-top=" *expression* "></span></span>

<span data-ttu-id="a7245-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a7245-117">**Script Syntax**</span></span>

<span data-ttu-id="a7245-118">*Element* . margin-top = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a7245-118">*element* .margin-top="*expression*"</span></span>

<span data-ttu-id="a7245-119">*expresión* = de *elemento*. margin-top</span><span class="sxs-lookup"><span data-stu-id="a7245-119">*expression*=*element*.margin-top</span></span>

<span data-ttu-id="a7245-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a7245-120">**Remarks**</span></span>

<span data-ttu-id="a7245-121">El atributo **margin-top** es similar al atributo **margin-top** de HTML estándar que se usa con las hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="a7245-121">The **Margin-Top** attribute is similar to the standard HTML **Margin-Top** attribute used with style sheets.</span></span>

<span data-ttu-id="a7245-122">Tenga en cuenta que se utiliza **marginTop** en lugar de **margin-top** para el scripting.</span><span class="sxs-lookup"><span data-stu-id="a7245-122">Note that **margintop** is used instead of **margin-top** for scripting.</span></span> <span data-ttu-id="a7245-123">Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.</span><span class="sxs-lookup"><span data-stu-id="a7245-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="a7245-124">Esta propiedad se utiliza en lugar de la **parte superior** para las formas de Microsoft Word y Microsoft Excel que están flotando en una posición relativa a un punto de anclaje.</span><span class="sxs-lookup"><span data-stu-id="a7245-124">This property is used instead of **Top** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="a7245-125">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="a7245-125">Values include:</span></span>



| <span data-ttu-id="a7245-126">Value</span><span class="sxs-lookup"><span data-stu-id="a7245-126">Value</span></span>      | <span data-ttu-id="a7245-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7245-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7245-128">Automático</span><span class="sxs-lookup"><span data-stu-id="a7245-128">Auto</span></span>       | <span data-ttu-id="a7245-129">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="a7245-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="a7245-130">units</span><span class="sxs-lookup"><span data-stu-id="a7245-130">units</span></span>      | <span data-ttu-id="a7245-131">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a7245-131">Default.</span></span> <span data-ttu-id="a7245-132">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="a7245-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="a7245-133">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="a7245-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="a7245-134">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="a7245-134">The default value is 0.</span></span> |
| <span data-ttu-id="a7245-135">percentage</span><span class="sxs-lookup"><span data-stu-id="a7245-135">percentage</span></span> | <span data-ttu-id="a7245-136">Valor expresado como porcentaje del alto del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="a7245-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="a7245-137">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="a7245-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="a7245-138">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="a7245-138">**See Also**</span></span>

[<span data-ttu-id="a7245-139">Unidades</span><span class="sxs-lookup"><span data-stu-id="a7245-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="a7245-140">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a7245-140">**Example**</span></span>

<span data-ttu-id="a7245-141">El margen superior se establece en 25 píxeles.</span><span class="sxs-lookup"><span data-stu-id="a7245-141">The top margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



<span data-ttu-id="a7245-142">[Ejemplo de atributo margin-top](/previous-versions/bb264087(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a7245-142">[Margin-Top Attribute Example](/previous-versions/bb264087(v=vs.85)).</span></span> <span data-ttu-id="a7245-143">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="a7245-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 