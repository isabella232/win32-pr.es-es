---
title: Atributo AlignShape de VML
description: Atributo AlignShape de VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359362"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="b9dd2-103">Atributo AlignShape de VML</span><span class="sxs-lookup"><span data-stu-id="b9dd2-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="b9dd2-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b9dd2-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b9dd2-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b9dd2-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b9dd2-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b9dd2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b9dd2-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b9dd2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b9dd2-110">Determina si una imagen se alineará con una forma.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="b9dd2-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9dd2-111">Read/write.</span></span> <span data-ttu-id="b9dd2-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-112">**VgTriState**.</span></span>

<span data-ttu-id="b9dd2-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b9dd2-113">**Applies To**</span></span>

[<span data-ttu-id="b9dd2-114">Fill</span><span class="sxs-lookup"><span data-stu-id="b9dd2-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b9dd2-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b9dd2-115">**Tag Syntax**</span></span>

<span data-ttu-id="b9dd2-116"><v: *Element* alignshape = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b9dd2-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="b9dd2-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b9dd2-117">**Script Syntax**</span></span>

<span data-ttu-id="b9dd2-118">*Element* . alignshape = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b9dd2-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="b9dd2-119">*expresión* = de *elemento*. alignshape</span><span class="sxs-lookup"><span data-stu-id="b9dd2-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="b9dd2-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b9dd2-120">**Remarks**</span></span>

<span data-ttu-id="b9dd2-121">Si es **true**, la imagen utilizada para crear el relleno está alineada con la forma.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="b9dd2-122">Si es **false**, la imagen utilizada para crear el relleno está alineada con la ventana.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="b9dd2-123">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-123">Default is **True**.</span></span>

<span data-ttu-id="b9dd2-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b9dd2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b9dd2-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b9dd2-125">**Example**</span></span>

<span data-ttu-id="b9dd2-126">La imagen de relleno en mosaico creada a partir de myimage.gif se alinea con la ventana, no con la forma; Aunque la forma se gira, la imagen no lo es.</span><span class="sxs-lookup"><span data-stu-id="b9dd2-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 