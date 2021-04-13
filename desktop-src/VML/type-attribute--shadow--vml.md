---
title: Atributo de tipo (sombra) (VML)
description: Atributo de tipo (sombra) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421062"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="74106-103">Atributo de tipo (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="74106-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="74106-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74106-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74106-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="74106-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74106-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="74106-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74106-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="74106-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74106-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74106-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74106-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74106-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74106-110">Especifica el tipo de sombra.</span><span class="sxs-lookup"><span data-stu-id="74106-110">Specifies the type of shadow.</span></span> <span data-ttu-id="74106-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74106-111">Read/write.</span></span> <span data-ttu-id="74106-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="74106-112">**String**.</span></span>

<span data-ttu-id="74106-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="74106-113">**Applies To**</span></span>

[<span data-ttu-id="74106-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="74106-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="74106-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="74106-115">**Tag Syntax**</span></span>

<span data-ttu-id="74106-116"><v: *Element* Type = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="74106-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="74106-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="74106-117">**Script Syntax**</span></span>

<span data-ttu-id="74106-118">*Element* . Type = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="74106-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="74106-119">*expresión* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="74106-119">*expression*=*element*.type</span></span>

<span data-ttu-id="74106-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="74106-120">**Remarks**</span></span>

<span data-ttu-id="74106-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="74106-121">Values include:</span></span>



| <span data-ttu-id="74106-122">Value</span><span class="sxs-lookup"><span data-stu-id="74106-122">Value</span></span>           | <span data-ttu-id="74106-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="74106-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74106-124">sola</span><span class="sxs-lookup"><span data-stu-id="74106-124">single</span></span>          | <span data-ttu-id="74106-125">Sombra única.</span><span class="sxs-lookup"><span data-stu-id="74106-125">Single shadow.</span></span> <span data-ttu-id="74106-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74106-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="74106-127">double</span><span class="sxs-lookup"><span data-stu-id="74106-127">double</span></span>          | <span data-ttu-id="74106-128">Sombra doble.</span><span class="sxs-lookup"><span data-stu-id="74106-128">A double shadow.</span></span> <span data-ttu-id="74106-129">[Color2](color2-attribute--shadow--vml.md) se usa para el color de la segunda sombra y se usa [Offset2](msdn-online-vml-offset2-attribute.md) para el desplazamiento de la segunda sombra.</span><span class="sxs-lookup"><span data-stu-id="74106-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="74106-130">perspectiva</span><span class="sxs-lookup"><span data-stu-id="74106-130">perspective</span></span>     | <span data-ttu-id="74106-131">Sombra de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="74106-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="74106-132">shapeRelative</span><span class="sxs-lookup"><span data-stu-id="74106-132">shapeRelative</span></span>   | <span data-ttu-id="74106-133">La sombra se crea en relación con la forma.</span><span class="sxs-lookup"><span data-stu-id="74106-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="74106-134">drawingRelative</span><span class="sxs-lookup"><span data-stu-id="74106-134">drawingRelative</span></span> | <span data-ttu-id="74106-135">La sombra se crea en relación con el dibujo.</span><span class="sxs-lookup"><span data-stu-id="74106-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="74106-136">relieve</span><span class="sxs-lookup"><span data-stu-id="74106-136">emboss</span></span>          | <span data-ttu-id="74106-137">La sombra tiene una apariencia en relieve.</span><span class="sxs-lookup"><span data-stu-id="74106-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="74106-138">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="74106-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="74106-139">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="74106-139">**Example**</span></span>

<span data-ttu-id="74106-140">Se crea una sombra doble con la segunda sombra verde y desplazamiento 5 puntos hacia abajo y hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="74106-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 