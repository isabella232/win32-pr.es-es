---
title: Atributo Z-index de VML
description: Atributo Z-index de VML
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995320"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="45d13-103">Atributo Z-index de VML</span><span class="sxs-lookup"><span data-stu-id="45d13-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="45d13-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="45d13-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="45d13-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="45d13-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="45d13-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="45d13-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="45d13-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="45d13-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="45d13-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="45d13-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="45d13-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="45d13-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="45d13-110">Determina el orden de presentación de las formas superpuestas.</span><span class="sxs-lookup"><span data-stu-id="45d13-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="45d13-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="45d13-111">Read/write.</span></span> <span data-ttu-id="45d13-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="45d13-112">**String**.</span></span>

<span data-ttu-id="45d13-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="45d13-113">**Applies To**</span></span>

[<span data-ttu-id="45d13-114">Forma</span><span class="sxs-lookup"><span data-stu-id="45d13-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="45d13-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="45d13-115">**Tag Syntax**</span></span>

<span data-ttu-id="45d13-116"><v: *Element* style = "z-index: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="45d13-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="45d13-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="45d13-117">**Script Syntax**</span></span>

<span data-ttu-id="45d13-118">*Element* . Style. ZIndex = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="45d13-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="45d13-119">*expresión* = de *elemento*. Style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="45d13-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="45d13-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="45d13-120">**Remarks**</span></span>

<span data-ttu-id="45d13-121">El atributo **z-index** es similar al atributo **z-index** de HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="45d13-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="45d13-122">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="45d13-122">Values include:</span></span>



| <span data-ttu-id="45d13-123">Value</span><span class="sxs-lookup"><span data-stu-id="45d13-123">Value</span></span> | <span data-ttu-id="45d13-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="45d13-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d13-125">Automático</span><span class="sxs-lookup"><span data-stu-id="45d13-125">Auto</span></span>  | <span data-ttu-id="45d13-126">Se utilizará el orden en que se muestran las formas en la página HTML, de abajo a arriba.</span><span class="sxs-lookup"><span data-stu-id="45d13-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="45d13-127">orden</span><span class="sxs-lookup"><span data-stu-id="45d13-127">order</span></span> | <span data-ttu-id="45d13-128">Número que representa la precedencia de la pila.</span><span class="sxs-lookup"><span data-stu-id="45d13-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="45d13-129">Una forma con un número mayor se mostrará como si wereoverlapping (en "Front") una forma con un número inferior.</span><span class="sxs-lookup"><span data-stu-id="45d13-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="45d13-130">Se pueden usar números negativos.</span><span class="sxs-lookup"><span data-stu-id="45d13-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="45d13-131">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="45d13-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="45d13-132">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="45d13-132">**Example**</span></span>

<span data-ttu-id="45d13-133">La forma roja se mostrará en "Front" de la forma azul, porque tiene un índice z superior.</span><span class="sxs-lookup"><span data-stu-id="45d13-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="45d13-134">[Ejemplo de atributo de índice Z](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45d13-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="45d13-135">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="45d13-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 