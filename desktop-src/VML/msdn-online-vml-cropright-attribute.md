---
title: Atributo CropRight de VML
description: Atributo CropRight de VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487770"
---
# <a name="vml-cropright-attribute"></a><span data-ttu-id="136cd-103">Atributo CropRight de VML</span><span class="sxs-lookup"><span data-stu-id="136cd-103">VML CropRight Attribute</span></span>

<span data-ttu-id="136cd-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="136cd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="136cd-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="136cd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="136cd-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="136cd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="136cd-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="136cd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="136cd-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="136cd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="136cd-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="136cd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="136cd-110">Define el porcentaje de eliminación de imágenes del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="136cd-110">Defines the percentage of picture removal from the right side.</span></span> <span data-ttu-id="136cd-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="136cd-111">Read/write.</span></span> <span data-ttu-id="136cd-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="136cd-112">**VgNumber**.</span></span>

<span data-ttu-id="136cd-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="136cd-113">**Applies To**</span></span>

[<span data-ttu-id="136cd-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="136cd-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="136cd-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="136cd-115">**Tag Syntax**</span></span>

<span data-ttu-id="136cd-116"><v: *elemento* CropRight = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="136cd-116"><v: *element* cropright=" *expression* "></span></span>

<span data-ttu-id="136cd-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="136cd-117">**Script Syntax**</span></span>

<span data-ttu-id="136cd-118">*Element* . CropRight = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="136cd-118">*element* .cropright="*expression*"</span></span>

<span data-ttu-id="136cd-119">*expresión* = de *elemento*. CropRight</span><span class="sxs-lookup"><span data-stu-id="136cd-119">*expression*=*element*.cropright</span></span>

<span data-ttu-id="136cd-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="136cd-120">**Remarks**</span></span>

<span data-ttu-id="136cd-121">La cantidad de recorte puede oscilar entre-1,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="136cd-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="136cd-122">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="136cd-122">The default value is 0.</span></span> <span data-ttu-id="136cd-123">Tenga en cuenta que el valor 1 no mostrará ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="136cd-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="136cd-124">Los valores negativos provocarán que la imagen se apriete hacia adentro desde el borde que se va a recortar (el color de relleno de la forma se rellenará con el espacio vacío entre la imagen y el borde recortado).</span><span class="sxs-lookup"><span data-stu-id="136cd-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="136cd-125">Los valores positivos inferiores a 1 darán lugar a que la imagen restante se estire para ajustarse a la forma.</span><span class="sxs-lookup"><span data-stu-id="136cd-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="136cd-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="136cd-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="136cd-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="136cd-127">**Example**</span></span>

<span data-ttu-id="136cd-128">La imagen se apapretará del lado derecho en un 20% del ancho.</span><span class="sxs-lookup"><span data-stu-id="136cd-128">The picture will be squeezed from the right side by 20% of the width.</span></span> <span data-ttu-id="136cd-129">El espacio vacío entre la imagen y el borde derecho se rellenará con el color de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="136cd-129">The empty space between the picture and the right edge will be filled by the fill color of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 