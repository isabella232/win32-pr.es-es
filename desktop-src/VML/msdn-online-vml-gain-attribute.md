---
title: Atributo de ganancia de VML
description: Atributo de ganancia de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421068"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="f5a27-103">Atributo de ganancia de VML</span><span class="sxs-lookup"><span data-stu-id="f5a27-103">VML Gain Attribute</span></span>

<span data-ttu-id="f5a27-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f5a27-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f5a27-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f5a27-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f5a27-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f5a27-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f5a27-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f5a27-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f5a27-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f5a27-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f5a27-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f5a27-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f5a27-110">Define la intensidad de todos los colores de una imagen.</span><span class="sxs-lookup"><span data-stu-id="f5a27-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="f5a27-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f5a27-111">Read/write.</span></span> <span data-ttu-id="f5a27-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="f5a27-112">**VgNumber**.</span></span>

<span data-ttu-id="f5a27-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f5a27-113">**Applies To**</span></span>

[<span data-ttu-id="f5a27-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="f5a27-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="f5a27-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f5a27-115">**Tag Syntax**</span></span>

<span data-ttu-id="f5a27-116"><v: *elemento* ganancia = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="f5a27-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="f5a27-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f5a27-117">**Script Syntax**</span></span>

<span data-ttu-id="f5a27-118">*Element* . beneficio = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="f5a27-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="f5a27-119">*expresión* = de *elemento*. ganancia</span><span class="sxs-lookup"><span data-stu-id="f5a27-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="f5a27-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f5a27-120">**Remarks**</span></span>

<span data-ttu-id="f5a27-121">Este atributo define la luminosidad del color blanco, lo que afecta a todos los demás colores.</span><span class="sxs-lookup"><span data-stu-id="f5a27-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="f5a27-122">Los valores oscilan entre 0 y infinito.</span><span class="sxs-lookup"><span data-stu-id="f5a27-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="f5a27-123">El valor predeterminado es 1,0.</span><span class="sxs-lookup"><span data-stu-id="f5a27-123">The default value is 1.0.</span></span> <span data-ttu-id="f5a27-124">Un valor de 0 no muestra ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="f5a27-124">A value of 0 displays no image.</span></span> <span data-ttu-id="f5a27-125">Los valores mayores que 1 aclaran la imagen y los valores inferiores a 1 hacen que la imagen parezca Grayer.</span><span class="sxs-lookup"><span data-stu-id="f5a27-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="f5a27-126">Este atributo se puede usar para crear efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="f5a27-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="f5a27-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="f5a27-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="f5a27-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f5a27-128">**Example**</span></span>

<span data-ttu-id="f5a27-129">La imagen se mostrará con todos los colores que tienden a atenuar.</span><span class="sxs-lookup"><span data-stu-id="f5a27-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 