---
title: Atributo de alto de VML
description: Atributo de alto de VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149373"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="562e7-103">Atributo de alto de VML</span><span class="sxs-lookup"><span data-stu-id="562e7-103">VML Height Attribute</span></span>

<span data-ttu-id="562e7-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="562e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="562e7-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="562e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="562e7-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="562e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="562e7-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="562e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="562e7-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="562e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="562e7-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="562e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="562e7-110">Especifica el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="562e7-110">Specifies the height of the shape.</span></span> <span data-ttu-id="562e7-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="562e7-111">Read/write.</span></span> <span data-ttu-id="562e7-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="562e7-112">**String**.</span></span>

<span data-ttu-id="562e7-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="562e7-113">**Applies To**</span></span>

[<span data-ttu-id="562e7-114">Forma</span><span class="sxs-lookup"><span data-stu-id="562e7-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="562e7-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="562e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="562e7-116"><v: *Element* style = "height: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="562e7-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="562e7-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="562e7-117">**Script Syntax**</span></span>

<span data-ttu-id="562e7-118">*Element* . Style. height = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="562e7-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="562e7-119">*expresión* = de *elemento*. Style. Height</span><span class="sxs-lookup"><span data-stu-id="562e7-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="562e7-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="562e7-120">**Remarks**</span></span>

<span data-ttu-id="562e7-121">El atributo de **alto** es similar al atributo **alto** de HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="562e7-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="562e7-122">Las unidades se pueden asignar al elemento primario o pueden estar en unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="562e7-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="562e7-123">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="562e7-123">Values include:</span></span>



| <span data-ttu-id="562e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="562e7-124">Value</span></span>      | <span data-ttu-id="562e7-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="562e7-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="562e7-126">Automático</span><span class="sxs-lookup"><span data-stu-id="562e7-126">Auto</span></span>       | <span data-ttu-id="562e7-127">Posición predeterminada de un elemento en el flujo de la página.</span><span class="sxs-lookup"><span data-stu-id="562e7-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="562e7-128">units</span><span class="sxs-lookup"><span data-stu-id="562e7-128">units</span></span>      | <span data-ttu-id="562e7-129">Número con un designador de unidades absolutas (cm, mm, PDA, PT, PC o PX) o un designador de unidades relativas (EM o ex).</span><span class="sxs-lookup"><span data-stu-id="562e7-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="562e7-130">Si no se especifica ninguna unidad, se supone que se trata de píxeles (PX).</span><span class="sxs-lookup"><span data-stu-id="562e7-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="562e7-131">percentage</span><span class="sxs-lookup"><span data-stu-id="562e7-131">percentage</span></span> | <span data-ttu-id="562e7-132">Valor expresado como porcentaje del alto del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="562e7-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="562e7-133">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="562e7-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="562e7-134">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="562e7-134">**See Also**</span></span>

[<span data-ttu-id="562e7-135">Unidades</span><span class="sxs-lookup"><span data-stu-id="562e7-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="562e7-136">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="562e7-136">**Example**</span></span>

<span data-ttu-id="562e7-137">El alto de la forma se establece en 30.</span><span class="sxs-lookup"><span data-stu-id="562e7-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="562e7-138">[Ejemplo de atributo de alto](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="562e7-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="562e7-139">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="562e7-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 