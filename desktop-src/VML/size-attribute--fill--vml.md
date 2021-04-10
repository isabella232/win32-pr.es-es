---
title: Size (atributo, Fill) (VML)
description: Size (atributo, Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995318"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="8d5b4-103">Size (atributo, Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="8d5b4-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8d5b4-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8d5b4-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8d5b4-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8d5b4-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8d5b4-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8d5b4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8d5b4-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8d5b4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8d5b4-110">Define el tamaño de la imagen para el relleno.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="8d5b4-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8d5b4-111">Read/write.</span></span> <span data-ttu-id="8d5b4-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8d5b4-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="8d5b4-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-113">**Applies To**</span></span>

[<span data-ttu-id="8d5b4-114">Fill</span><span class="sxs-lookup"><span data-stu-id="8d5b4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8d5b4-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-115">**Tag Syntax**</span></span>

<span data-ttu-id="8d5b4-116"><v: *elemento* size = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8d5b4-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="8d5b4-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-117">**Script Syntax**</span></span>

<span data-ttu-id="8d5b4-118">*Element* . size = "*expresión \* *"**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="8d5b4-119">*expresión* = de *elemento*. Size</span><span class="sxs-lookup"><span data-stu-id="8d5b4-119">*expression*=*element*.size</span></span>

<span data-ttu-id="8d5b4-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-120">**Remarks**</span></span>

<span data-ttu-id="8d5b4-121">El valor predeterminado es el tamaño de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-121">The default is the size of the original image.</span></span> <span data-ttu-id="8d5b4-122">Los tamaños mayores que el shapewill muestran una versión ampliada pero recortada de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="8d5b4-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8d5b4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8d5b4-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8d5b4-124">**Example**</span></span>

<span data-ttu-id="8d5b4-125">Aunque el tamaño original de la imagen es de 50 a 50 puntos, se mostrará la imagen como una imagen de 10 por 10 en el centro del relleno.</span><span class="sxs-lookup"><span data-stu-id="8d5b4-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 