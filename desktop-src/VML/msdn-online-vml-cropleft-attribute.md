---
title: Atributo CropLeft de VML
description: Atributo CropLeft de VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271279"
---
# <a name="vml-cropleft-attribute"></a><span data-ttu-id="3818b-103">Atributo CropLeft de VML</span><span class="sxs-lookup"><span data-stu-id="3818b-103">VML CropLeft Attribute</span></span>

<span data-ttu-id="3818b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3818b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3818b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3818b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3818b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3818b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3818b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3818b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3818b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3818b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3818b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3818b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3818b-110">Define el porcentaje de eliminación de imágenes del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="3818b-110">Defines the percentage of picture removal from the left side.</span></span> <span data-ttu-id="3818b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3818b-111">Read/write.</span></span> <span data-ttu-id="3818b-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="3818b-112">**VgNumber**.</span></span>

<span data-ttu-id="3818b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3818b-113">**Applies To**</span></span>

[<span data-ttu-id="3818b-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="3818b-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="3818b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3818b-115">**Tag Syntax**</span></span>

<span data-ttu-id="3818b-116"><v: *elemento* CropLeft = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3818b-116"><v: *element* cropleft=" *expression* "></span></span>

<span data-ttu-id="3818b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3818b-117">**Script Syntax**</span></span>

<span data-ttu-id="3818b-118">*Element* . CropLeft = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3818b-118">*element* .cropleft="*expression*"</span></span>

<span data-ttu-id="3818b-119">*expresión* = de *elemento*. CropLeft</span><span class="sxs-lookup"><span data-stu-id="3818b-119">*expression*=*element*.cropleft</span></span>

<span data-ttu-id="3818b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3818b-120">**Remarks**</span></span>

<span data-ttu-id="3818b-121">La cantidad de recorte puede oscilar entre-1,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="3818b-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="3818b-122">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3818b-122">The default value is 0.</span></span> <span data-ttu-id="3818b-123">Tenga en cuenta que el valor 1 no mostrará ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="3818b-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="3818b-124">Los valores negativos provocarán que la imagen se apriete hacia adentro desde el borde que se va a recortar (el color de relleno de la forma se rellenará con el espacio vacío entre la imagen y el borde recortado).</span><span class="sxs-lookup"><span data-stu-id="3818b-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="3818b-125">Los valores positivos inferiores a 1 darán lugar a que la imagen restante se estire para ajustarse a la forma.</span><span class="sxs-lookup"><span data-stu-id="3818b-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="3818b-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="3818b-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="3818b-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3818b-127">**Example**</span></span>

<span data-ttu-id="3818b-128">el 20% de la imagen se quitará en el lado izquierdo y la imagen restante se ajustará para ajustarse a la forma.</span><span class="sxs-lookup"><span data-stu-id="3818b-128">20% of the picture will be removed on the left side and the remaining picture will be stretched to fit the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 