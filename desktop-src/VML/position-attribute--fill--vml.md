---
title: Atributo Position (relleno) (VML)
description: Atributo Position (relleno) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149588"
---
# <a name="position-attribute-fillvml"></a><span data-ttu-id="6f3ef-103">Atributo Position (relleno) (VML)</span><span class="sxs-lookup"><span data-stu-id="6f3ef-103">Position Attribute (Fill)(VML)</span></span>

<span data-ttu-id="6f3ef-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f3ef-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f3ef-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f3ef-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f3ef-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f3ef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f3ef-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f3ef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f3ef-110">Define la posición de la imagen de relleno.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-110">Defines the position of fill image.</span></span> <span data-ttu-id="6f3ef-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f3ef-111">Read/write.</span></span> <span data-ttu-id="6f3ef-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3ef-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="6f3ef-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6f3ef-113">**Applies To**</span></span>

[<span data-ttu-id="6f3ef-114">Fill</span><span class="sxs-lookup"><span data-stu-id="6f3ef-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="6f3ef-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6f3ef-115">**Tag Syntax**</span></span>

<span data-ttu-id="6f3ef-116"><v: *elemento* position = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="6f3ef-116"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="6f3ef-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="6f3ef-117">**Script Syntax**</span></span>

<span data-ttu-id="6f3ef-118">*Element* . position = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="6f3ef-118">*element* .position="*expression*"</span></span>

<span data-ttu-id="6f3ef-119">*expresión* = de *elemento*. Position</span><span class="sxs-lookup"><span data-stu-id="6f3ef-119">*expression*=*element*.position</span></span>

<span data-ttu-id="6f3ef-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6f3ef-120">**Remarks**</span></span>

<span data-ttu-id="6f3ef-121">Especifica un punto de la forma para colocar el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-121">Specifies a point in the shape to position the origin of the image.</span></span> <span data-ttu-id="6f3ef-122">El valor predeterminado es el centro del rectángulo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-122">Default is the center of the container rectangle.</span></span> <span data-ttu-id="6f3ef-123">El vector es una fracción del ancho y el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="6f3ef-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="6f3ef-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6f3ef-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6f3ef-125">**Example**</span></span>

<span data-ttu-id="6f3ef-126">La imagen del relleno se desplaza hacia la derecha hasta un punto 50% del ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-126">The image of the fill is shifted right to a point 50% of the width of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 