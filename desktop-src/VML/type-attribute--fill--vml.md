---
title: Atributo type (Fill) (VML)
description: Atributo type (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792754"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="a71ef-103">Atributo type (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="a71ef-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="a71ef-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a71ef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a71ef-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a71ef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a71ef-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a71ef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a71ef-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a71ef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a71ef-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a71ef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a71ef-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a71ef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a71ef-110">Determina el tipo de relleno.</span><span class="sxs-lookup"><span data-stu-id="a71ef-110">Determines the type of fill.</span></span> <span data-ttu-id="a71ef-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a71ef-111">Read/write.</span></span> <span data-ttu-id="a71ef-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="a71ef-112">**VgFillType**.</span></span>

<span data-ttu-id="a71ef-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a71ef-113">**Applies To**</span></span>

[<span data-ttu-id="a71ef-114">Fill</span><span class="sxs-lookup"><span data-stu-id="a71ef-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="a71ef-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a71ef-115">**Tag Syntax**</span></span>

<span data-ttu-id="a71ef-116"><v: *Element* Type = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a71ef-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="a71ef-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a71ef-117">**Script Syntax**</span></span>

<span data-ttu-id="a71ef-118">*Element* . Type = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a71ef-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="a71ef-119">*expresión* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="a71ef-119">*expression*=*element*.type</span></span>

<span data-ttu-id="a71ef-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a71ef-120">**Remarks**</span></span>

<span data-ttu-id="a71ef-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="a71ef-121">Values include:</span></span>



| <span data-ttu-id="a71ef-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71ef-122">Type</span></span>           | <span data-ttu-id="a71ef-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a71ef-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a71ef-124">barra</span><span class="sxs-lookup"><span data-stu-id="a71ef-124">solid</span></span>          | <span data-ttu-id="a71ef-125">El patrón de relleno es sólido.</span><span class="sxs-lookup"><span data-stu-id="a71ef-125">The fill pattern is solid.</span></span> <span data-ttu-id="a71ef-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a71ef-126">Default.</span></span>                                     |
| <span data-ttu-id="a71ef-127">degradados</span><span class="sxs-lookup"><span data-stu-id="a71ef-127">gradient</span></span>       | <span data-ttu-id="a71ef-128">Los colores de relleno se combinan en un degradado lineal de abajo a arriba.</span><span class="sxs-lookup"><span data-stu-id="a71ef-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="a71ef-129">gradientradial</span><span class="sxs-lookup"><span data-stu-id="a71ef-129">gradientradial</span></span> | <span data-ttu-id="a71ef-130">Los colores de relleno se combinan en un degradado radial.</span><span class="sxs-lookup"><span data-stu-id="a71ef-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="a71ef-131">tile</span><span class="sxs-lookup"><span data-stu-id="a71ef-131">tile</span></span>           | <span data-ttu-id="a71ef-132">La imagen de relleno está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="a71ef-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="a71ef-133">pattern</span><span class="sxs-lookup"><span data-stu-id="a71ef-133">pattern</span></span>        | <span data-ttu-id="a71ef-134">La imagen se usa para crear un patrón con los colores de relleno.</span><span class="sxs-lookup"><span data-stu-id="a71ef-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="a71ef-135">frame</span><span class="sxs-lookup"><span data-stu-id="a71ef-135">frame</span></span>          | <span data-ttu-id="a71ef-136">La imagen se ajusta para rellenar la forma.</span><span class="sxs-lookup"><span data-stu-id="a71ef-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="a71ef-137">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="a71ef-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="a71ef-138">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a71ef-138">**Example**</span></span>

<span data-ttu-id="a71ef-139">Se crea un relleno de fondo rojo y de primer plano azul mediante el patrón de la imagen myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="a71ef-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 