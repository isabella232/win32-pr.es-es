---
title: Atributo de visibilidad de VML
description: Atributo de visibilidad de VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695654"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="d5e7f-103">Atributo de visibilidad de VML</span><span class="sxs-lookup"><span data-stu-id="d5e7f-103">VML Visibility Attribute</span></span>

<span data-ttu-id="d5e7f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d5e7f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d5e7f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d5e7f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d5e7f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d5e7f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d5e7f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d5e7f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d5e7f-110">Determina si se muestra una forma.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="d5e7f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d5e7f-111">Read/write.</span></span> <span data-ttu-id="d5e7f-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-112">**String**.</span></span>

<span data-ttu-id="d5e7f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="d5e7f-113">**Applies To**</span></span>

[<span data-ttu-id="d5e7f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="d5e7f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d5e7f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="d5e7f-115">**Tag Syntax**</span></span>

<span data-ttu-id="d5e7f-116"><v: *elemento* style = "Visibility: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d5e7f-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="d5e7f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="d5e7f-117">**Script Syntax**</span></span>

<span data-ttu-id="d5e7f-118">*Element* . Style. Visibility = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="d5e7f-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="d5e7f-119">*expresión* = de *elemento*. Style. Visibility</span><span class="sxs-lookup"><span data-stu-id="d5e7f-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="d5e7f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="d5e7f-120">**Remarks**</span></span>

<span data-ttu-id="d5e7f-121">El atributo **Visibility** es similar al atributo de **visibilidad** HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="d5e7f-122">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="d5e7f-122">Values include:</span></span>



| <span data-ttu-id="d5e7f-123">Value</span><span class="sxs-lookup"><span data-stu-id="d5e7f-123">Value</span></span>    | <span data-ttu-id="d5e7f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5e7f-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e7f-125">visible</span><span class="sxs-lookup"><span data-stu-id="d5e7f-125">visible</span></span>  | <span data-ttu-id="d5e7f-126">La forma está visible.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d5e7f-127">hidden</span><span class="sxs-lookup"><span data-stu-id="d5e7f-127">hidden</span></span>   | <span data-ttu-id="d5e7f-128">La forma no es visible, pero sigue siendo parte del flujo de los objetos en el explorador.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="d5e7f-129">No se procesan los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="d5e7f-130">inherit</span><span class="sxs-lookup"><span data-stu-id="d5e7f-130">inherit</span></span>  | <span data-ttu-id="d5e7f-131">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-131">Default.</span></span> <span data-ttu-id="d5e7f-132">El estado de visibilidad se hereda del elemento primario de la forma.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="d5e7f-133">Las aplicaciones de Microsoft Office solo utilizan **inherit** y **Hidden**. los demás valores se asignan a **inherit**.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="d5e7f-134">contraer</span><span class="sxs-lookup"><span data-stu-id="d5e7f-134">collapse</span></span> | <span data-ttu-id="d5e7f-135">Se usa para aplicaciones de edición gráficas que pueden contraer grupos de formas. por ejemplo, los esquemas.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="d5e7f-136">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="d5e7f-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="d5e7f-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="d5e7f-137">**Example**</span></span>

<span data-ttu-id="d5e7f-138">En el código siguiente se crea una forma, pero se oculta.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="d5e7f-139">Otros objetos del documento fluyen alrededor de él, lo que deja un espacio del mismo tamaño que la forma.</span><span class="sxs-lookup"><span data-stu-id="d5e7f-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="d5e7f-140">[Ejemplo de atributo de visibilidad](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5e7f-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="d5e7f-141">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="d5e7f-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 