---
title: Atributo de Margin-Right VML
description: Atributo de Margin-Right VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078344"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="5f6a9-103">Atributo de Margin-Right VML</span><span class="sxs-lookup"><span data-stu-id="5f6a9-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="5f6a9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f6a9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f6a9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f6a9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f6a9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f6a9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f6a9-110">Especifica el borde derecho del rectángulo que contiene la forma en relación con el delimitador de la forma.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="5f6a9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f6a9-111">Read/write.</span></span> <span data-ttu-id="5f6a9-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-112">**String**.</span></span>

<span data-ttu-id="5f6a9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-113">**Applies To**</span></span>

[<span data-ttu-id="5f6a9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="5f6a9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5f6a9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-115">**Tag Syntax**</span></span>

<span data-ttu-id="5f6a9-116"><v: *Element* style = "margin-right: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5f6a9-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="5f6a9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-117">**Script Syntax**</span></span>

<span data-ttu-id="5f6a9-118">*Element* . Style. marginRight = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="5f6a9-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="5f6a9-119">*expresión* = de *Element*. Style. marginRight</span><span class="sxs-lookup"><span data-stu-id="5f6a9-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="5f6a9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-120">**Remarks**</span></span>

<span data-ttu-id="5f6a9-121">El atributo **margin-right** es similar al atributo **margin-right de** HTML estándar que se usa con las hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="5f6a9-122">Tenga en cuenta que se usa **marginRight** en lugar de **margin-right** para scripting.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="5f6a9-123">Tenga en cuenta también que si la **posición** es **absoluta**, el margen no aparecerá para cambiar.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="5f6a9-124">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="5f6a9-124">Values include:</span></span>



| <span data-ttu-id="5f6a9-125">Value</span><span class="sxs-lookup"><span data-stu-id="5f6a9-125">Value</span></span>      | <span data-ttu-id="5f6a9-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f6a9-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6a9-127">Automático</span><span class="sxs-lookup"><span data-stu-id="5f6a9-127">Auto</span></span>       | <span data-ttu-id="5f6a9-128">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="5f6a9-129">units</span><span class="sxs-lookup"><span data-stu-id="5f6a9-129">units</span></span>      | <span data-ttu-id="5f6a9-130">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-130">Default.</span></span> <span data-ttu-id="5f6a9-131">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="5f6a9-132">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="5f6a9-133">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-133">The default value is 0.</span></span> |
| <span data-ttu-id="5f6a9-134">percentage</span><span class="sxs-lookup"><span data-stu-id="5f6a9-134">percentage</span></span> | <span data-ttu-id="5f6a9-135">Valor expresado como porcentaje del alto del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="5f6a9-136">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="5f6a9-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="5f6a9-137">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-137">**See Also**</span></span>

[<span data-ttu-id="5f6a9-138">Unidades</span><span class="sxs-lookup"><span data-stu-id="5f6a9-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="5f6a9-139">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5f6a9-139">**Example**</span></span>

<span data-ttu-id="5f6a9-140">El margen derecho se establece en 25 píxeles.</span><span class="sxs-lookup"><span data-stu-id="5f6a9-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="5f6a9-141">[Ejemplo de atributo margin-right](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="5f6a9-142">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="5f6a9-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 