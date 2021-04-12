---
title: Atributo de Margin-Left VML
description: Atributo de Margin-Left VML
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359196"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="3f624-103">Atributo de Margin-Left VML</span><span class="sxs-lookup"><span data-stu-id="3f624-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="3f624-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f624-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f624-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3f624-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f624-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3f624-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f624-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3f624-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f624-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f624-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f624-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f624-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f624-110">Especifica el borde izquierdo del rectángulo que contiene la forma en relación con el delimitador de la forma.</span><span class="sxs-lookup"><span data-stu-id="3f624-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="3f624-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f624-111">Read/write.</span></span> <span data-ttu-id="3f624-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="3f624-112">**String**.</span></span>

<span data-ttu-id="3f624-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3f624-113">**Applies To**</span></span>

[<span data-ttu-id="3f624-114">Forma</span><span class="sxs-lookup"><span data-stu-id="3f624-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3f624-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3f624-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f624-116"><v: *Element* style = "margin-left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f624-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="3f624-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3f624-117">**Script Syntax**</span></span>

<span data-ttu-id="3f624-118">*Element* . Style. MarginLeft = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3f624-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="3f624-119">*expresión* = de *Element*. Style. MarginLeft</span><span class="sxs-lookup"><span data-stu-id="3f624-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="3f624-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3f624-120">**Remarks**</span></span>

<span data-ttu-id="3f624-121">El atributo **margin-left** es similar al atributo **margin-left de** HTML estándar que se usa con las hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="3f624-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="3f624-122">Tenga en cuenta que se usa **MarginLeft** en lugar de **margin-left** para scripting.</span><span class="sxs-lookup"><span data-stu-id="3f624-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="3f624-123">Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.</span><span class="sxs-lookup"><span data-stu-id="3f624-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="3f624-124">Esta propiedad se utiliza en lugar de la **izquierda** para las formas de Microsoft Word y Microsoft Excel que están flotando en una posición relativa a un punto de anclaje.</span><span class="sxs-lookup"><span data-stu-id="3f624-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="3f624-125">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="3f624-125">Values include:</span></span>



| <span data-ttu-id="3f624-126">Value</span><span class="sxs-lookup"><span data-stu-id="3f624-126">Value</span></span>      | <span data-ttu-id="3f624-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f624-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f624-128">Automático</span><span class="sxs-lookup"><span data-stu-id="3f624-128">Auto</span></span>       | <span data-ttu-id="3f624-129">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="3f624-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="3f624-130">units</span><span class="sxs-lookup"><span data-stu-id="3f624-130">units</span></span>      | <span data-ttu-id="3f624-131">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f624-131">Default.</span></span> <span data-ttu-id="3f624-132">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="3f624-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="3f624-133">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="3f624-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="3f624-134">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3f624-134">The default value is 0.</span></span> |
| <span data-ttu-id="3f624-135">percentage</span><span class="sxs-lookup"><span data-stu-id="3f624-135">percentage</span></span> | <span data-ttu-id="3f624-136">Valor expresado como porcentaje del alto del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="3f624-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="3f624-137">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="3f624-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f624-138">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="3f624-138">**See Also**</span></span>

[<span data-ttu-id="3f624-139">Unidades</span><span class="sxs-lookup"><span data-stu-id="3f624-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="3f624-140">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3f624-140">**Example**</span></span>

<span data-ttu-id="3f624-141">El margen izquierdo se establece en 25 píxeles.</span><span class="sxs-lookup"><span data-stu-id="3f624-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="3f624-142">[Ejemplo de atributo margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span><span class="sxs-lookup"><span data-stu-id="3f624-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="3f624-143">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="3f624-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 