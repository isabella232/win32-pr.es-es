---
title: Origin (atributo, Fill) (VML)
description: Origin (atributo, Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421366"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="2763c-103">Origin (atributo, Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="2763c-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="2763c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2763c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2763c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="2763c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2763c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="2763c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2763c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2763c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2763c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2763c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2763c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2763c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2763c-110">Define el centro de una imagen de relleno.</span><span class="sxs-lookup"><span data-stu-id="2763c-110">Defines the center of a fill image.</span></span> <span data-ttu-id="2763c-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2763c-111">Read/write.</span></span> <span data-ttu-id="2763c-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="2763c-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="2763c-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2763c-113">**Applies To**</span></span>

[<span data-ttu-id="2763c-114">Fill</span><span class="sxs-lookup"><span data-stu-id="2763c-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="2763c-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="2763c-115">**Tag Syntax**</span></span>

<span data-ttu-id="2763c-116"><v: *elemento* Origin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="2763c-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="2763c-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="2763c-117">**Script Syntax**</span></span>

<span data-ttu-id="2763c-118">*Element* . Origin = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="2763c-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="2763c-119">*expresión* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="2763c-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="2763c-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="2763c-120">**Remarks**</span></span>

<span data-ttu-id="2763c-121">Especifica un punto relativo a la esquina superior izquierda de la imagen; este punto se trata como el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2763c-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="2763c-122">El valor predeterminado es el centro de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2763c-122">Default is the center of the image.</span></span> <span data-ttu-id="2763c-123">El vector es una fracción del ancho y el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2763c-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="2763c-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="2763c-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="2763c-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2763c-125">**Example**</span></span>

<span data-ttu-id="2763c-126">La imagen del relleno se desplaza hacia la izquierda hasta un punto 50% del ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="2763c-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 