---
title: Atributo BlackLevel de VML
description: Atributo BlackLevel de VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077963"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="8f8de-103">Atributo BlackLevel de VML</span><span class="sxs-lookup"><span data-stu-id="8f8de-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="8f8de-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8f8de-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8f8de-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8f8de-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8f8de-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8f8de-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8f8de-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8f8de-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8f8de-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8f8de-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8f8de-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8f8de-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8f8de-110">Define la intensidad de negro en una imagen.</span><span class="sxs-lookup"><span data-stu-id="8f8de-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="8f8de-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f8de-111">Read/write.</span></span> <span data-ttu-id="8f8de-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="8f8de-112">**VgNumber**.</span></span>

<span data-ttu-id="8f8de-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8f8de-113">**Applies To**</span></span>

[<span data-ttu-id="8f8de-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="8f8de-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="8f8de-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8f8de-115">**Tag Syntax**</span></span>

<span data-ttu-id="8f8de-116"><v: *Element* blacklevel = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8f8de-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="8f8de-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8f8de-117">**Script Syntax**</span></span>

<span data-ttu-id="8f8de-118">*Element* . blacklevel = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8f8de-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="8f8de-119">*expresión* = de *elemento*. blacklevel</span><span class="sxs-lookup"><span data-stu-id="8f8de-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="8f8de-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8f8de-120">**Remarks**</span></span>

<span data-ttu-id="8f8de-121">Permite que el nivel de color se modifique para que los negros aparezcan como verdaderos negros y todos los demás colores estén visibles como sombras por encima del negro.</span><span class="sxs-lookup"><span data-stu-id="8f8de-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="8f8de-122">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="8f8de-122">The default value is 0.</span></span> <span data-ttu-id="8f8de-123">Aunque se permite cualquier número entre infinitos positivos y negativos, los valores menores que-0,5 se mostrarán como todos los negros y los valores superiores a 0,5 se mostrarán como todos los blancos.</span><span class="sxs-lookup"><span data-stu-id="8f8de-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="8f8de-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8f8de-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="8f8de-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8f8de-125">**Example**</span></span>

<span data-ttu-id="8f8de-126">La imagen se mostrará con tonos muy oscuros.</span><span class="sxs-lookup"><span data-stu-id="8f8de-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 