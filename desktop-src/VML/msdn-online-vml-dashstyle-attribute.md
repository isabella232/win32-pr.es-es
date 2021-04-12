---
title: Atributo DashStyle de VML
description: Atributo DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359034"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="78b58-103">Atributo DashStyle de VML</span><span class="sxs-lookup"><span data-stu-id="78b58-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="78b58-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="78b58-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="78b58-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="78b58-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="78b58-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="78b58-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="78b58-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="78b58-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="78b58-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="78b58-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="78b58-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="78b58-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="78b58-110">Especifica el patrón de puntos y guiones de un trazo.</span><span class="sxs-lookup"><span data-stu-id="78b58-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="78b58-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="78b58-111">Read/write.</span></span> <span data-ttu-id="78b58-112">**VgLineDashStyle**.</span><span class="sxs-lookup"><span data-stu-id="78b58-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="78b58-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="78b58-113">**Applies To**</span></span>

[<span data-ttu-id="78b58-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="78b58-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="78b58-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="78b58-115">**Tag Syntax**</span></span>

<span data-ttu-id="78b58-116"><v: *elemento* DashStyle = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="78b58-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="78b58-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="78b58-117">**Script Syntax**</span></span>

<span data-ttu-id="78b58-118">*Element* . DashStyle = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="78b58-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="78b58-119">*expresión* = de *elemento*. DashStyle</span><span class="sxs-lookup"><span data-stu-id="78b58-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="78b58-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="78b58-120">**Remarks**</span></span>

<span data-ttu-id="78b58-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="78b58-121">Values include:</span></span>

-   <span data-ttu-id="78b58-122">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="78b58-122">Solid (default)</span></span>
-   <span data-ttu-id="78b58-123">ShortDash</span><span class="sxs-lookup"><span data-stu-id="78b58-123">ShortDash</span></span>
-   <span data-ttu-id="78b58-124">ShortDot</span><span class="sxs-lookup"><span data-stu-id="78b58-124">ShortDot</span></span>
-   <span data-ttu-id="78b58-125">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="78b58-125">ShortDashDot</span></span>
-   <span data-ttu-id="78b58-126">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="78b58-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="78b58-127">Punto</span><span class="sxs-lookup"><span data-stu-id="78b58-127">Dot</span></span>
-   <span data-ttu-id="78b58-128">Guión</span><span class="sxs-lookup"><span data-stu-id="78b58-128">Dash</span></span>
-   <span data-ttu-id="78b58-129">LongDash</span><span class="sxs-lookup"><span data-stu-id="78b58-129">LongDash</span></span>
-   <span data-ttu-id="78b58-130">DashDot</span><span class="sxs-lookup"><span data-stu-id="78b58-130">DashDot</span></span>
-   <span data-ttu-id="78b58-131">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="78b58-131">LongDashDot</span></span>
-   <span data-ttu-id="78b58-132">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="78b58-132">LongDashDotDot</span></span>

<span data-ttu-id="78b58-133">El atributo **DashStyle** permite al usuario especificar un patrón de guiones definido de forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="78b58-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="78b58-134">Esto se hace mediante una serie de números.</span><span class="sxs-lookup"><span data-stu-id="78b58-134">This is done using a series of numbers.</span></span> <span data-ttu-id="78b58-135">Los estilos de guión se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones.</span><span class="sxs-lookup"><span data-stu-id="78b58-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="78b58-136">Las longitudes son relativas al ancho de línea: una longitud de "1" es igual al ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="78b58-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="78b58-137">El estilo **EndCap** se aplica a cada guión; el estilo de la flecha no lo es.</span><span class="sxs-lookup"><span data-stu-id="78b58-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="78b58-138">La cadena define primero la longitud del guión y, a continuación, la longitud del espacio.</span><span class="sxs-lookup"><span data-stu-id="78b58-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="78b58-139">Esto puede repetirse para formar estilos de guiones complejos.</span><span class="sxs-lookup"><span data-stu-id="78b58-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="78b58-140">La cadena siempre debe contener un par de números; Si contiene un número impar de números, es posible que se descarte la última.</span><span class="sxs-lookup"><span data-stu-id="78b58-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="78b58-141">En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="78b58-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="78b58-142">"0" implica un punto que debe ser fourfold simétrico (con extremos de redondeo redondeados debe ser un círculo).</span><span class="sxs-lookup"><span data-stu-id="78b58-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="78b58-143">Si el extremo de la línea es "plano", un visor debe elegir un guion del sistema operativo integrado siempre que sea posible (en otras palabras.</span><span class="sxs-lookup"><span data-stu-id="78b58-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="78b58-144">algo que es rápido de dibujar).</span><span class="sxs-lookup"><span data-stu-id="78b58-144">something that is fast to draw.).</span></span> <span data-ttu-id="78b58-145">En la tabla siguiente se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="78b58-145">The following table shows some examples.</span></span>



| <span data-ttu-id="78b58-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="78b58-146">DashStyle</span></span>     | <span data-ttu-id="78b58-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="78b58-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b58-148">"2 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-148">"2 2"</span></span>         | <span data-ttu-id="78b58-149">Guiones cortos.</span><span class="sxs-lookup"><span data-stu-id="78b58-149">Short-dashes.</span></span> <span data-ttu-id="78b58-150">Cada guión y el espacio entre es dos veces el ancho de la línea.</span><span class="sxs-lookup"><span data-stu-id="78b58-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="78b58-151">"0 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-151">"0 2"</span></span>         | <span data-ttu-id="78b58-152">Suspensivos.</span><span class="sxs-lookup"><span data-stu-id="78b58-152">Dots.</span></span> <span data-ttu-id="78b58-153">El espacio entre es dos veces el ancho de la línea.</span><span class="sxs-lookup"><span data-stu-id="78b58-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="78b58-154">"2 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-154">"2 2 0 2"</span></span>     | <span data-ttu-id="78b58-155">Guión corto punto.</span><span class="sxs-lookup"><span data-stu-id="78b58-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="78b58-156">"2 2 0 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="78b58-157">Breve guión punto punto.</span><span class="sxs-lookup"><span data-stu-id="78b58-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="78b58-158">"1 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-158">"1 2"</span></span>         | <span data-ttu-id="78b58-159">Semitono.</span><span class="sxs-lookup"><span data-stu-id="78b58-159">Dot.</span></span> <span data-ttu-id="78b58-160">Cada guión es el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea.</span><span class="sxs-lookup"><span data-stu-id="78b58-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="78b58-161">"4 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-161">"4 2"</span></span>         | <span data-ttu-id="78b58-162">Dash.</span><span class="sxs-lookup"><span data-stu-id="78b58-162">Dash.</span></span> <span data-ttu-id="78b58-163">Cada guión es cuatro veces el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea.</span><span class="sxs-lookup"><span data-stu-id="78b58-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="78b58-164">"8 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-164">"8 2"</span></span>         | <span data-ttu-id="78b58-165">Guion largo.</span><span class="sxs-lookup"><span data-stu-id="78b58-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="78b58-166">"4 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-166">"4 2 1 2"</span></span>     | <span data-ttu-id="78b58-167">Guión punto.</span><span class="sxs-lookup"><span data-stu-id="78b58-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="78b58-168">"8 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-168">"8 2 1 2"</span></span>     | <span data-ttu-id="78b58-169">Guión largo punto.</span><span class="sxs-lookup"><span data-stu-id="78b58-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="78b58-170">"8 2 1 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="78b58-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="78b58-171">Largo guión punto punto.</span><span class="sxs-lookup"><span data-stu-id="78b58-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="78b58-172">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="78b58-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="78b58-173">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="78b58-173">**Example**</span></span>

<span data-ttu-id="78b58-174">La forma tiene un estilo de guión de guiones y puntos alternos.</span><span class="sxs-lookup"><span data-stu-id="78b58-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 