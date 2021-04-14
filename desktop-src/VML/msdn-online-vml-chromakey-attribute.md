---
title: Atributo Chromakey de VML
description: Atributo Chromakey de VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359140"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="646ce-103">Atributo Chromakey de VML</span><span class="sxs-lookup"><span data-stu-id="646ce-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="646ce-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="646ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="646ce-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="646ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="646ce-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="646ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="646ce-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="646ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="646ce-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="646ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="646ce-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="646ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="646ce-110">Define el valor de color de la imagen que se tratará como transparente.</span><span class="sxs-lookup"><span data-stu-id="646ce-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="646ce-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="646ce-111">Read/write.</span></span> <span data-ttu-id="646ce-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="646ce-112">**VgColor**.</span></span>

<span data-ttu-id="646ce-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="646ce-113">**Applies To**</span></span>

[<span data-ttu-id="646ce-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="646ce-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="646ce-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="646ce-115">**Tag Syntax**</span></span>

<span data-ttu-id="646ce-116"><v: *Element* Chromakey = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="646ce-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="646ce-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="646ce-117">**Script Syntax**</span></span>

<span data-ttu-id="646ce-118">*Element* . Chromakey = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="646ce-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="646ce-119">*expresión* = de *elemento*. Chromakey</span><span class="sxs-lookup"><span data-stu-id="646ce-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="646ce-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="646ce-120">**Remarks**</span></span>

<span data-ttu-id="646ce-121">Use este atributo para que las partes de una imagen sean transparentes mediante la creación de una incrustación de la transparencia en un color específico.</span><span class="sxs-lookup"><span data-stu-id="646ce-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="646ce-122">Por ejemplo, si hace que el valor de **Chromakey** sea **negro**, cualquier parte de la imagen que sea negra será transparente y el color de relleno se "mostrará a través" de esa parte de la imagen.</span><span class="sxs-lookup"><span data-stu-id="646ce-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="646ce-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="646ce-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="646ce-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="646ce-124">**Example**</span></span>

<span data-ttu-id="646ce-125">En su lugar, las áreas de la imagen que son de negro sólido serán transparentes, lo que permite que el color de relleno verde se muestre a través de esas áreas.</span><span class="sxs-lookup"><span data-stu-id="646ce-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 