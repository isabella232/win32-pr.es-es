---
title: Atributo src (ImageData) (VML)
description: Atributo src (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077815"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="b56d7-103">Atributo src (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="b56d7-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="b56d7-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b56d7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b56d7-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b56d7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b56d7-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b56d7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b56d7-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b56d7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b56d7-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b56d7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b56d7-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b56d7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b56d7-110">Define un origen para la imagen.</span><span class="sxs-lookup"><span data-stu-id="b56d7-110">Defines a source for the image.</span></span> <span data-ttu-id="b56d7-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b56d7-111">Read/write.</span></span> <span data-ttu-id="b56d7-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="b56d7-112">**String**.</span></span>

<span data-ttu-id="b56d7-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b56d7-113">**Applies To**</span></span>

[<span data-ttu-id="b56d7-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="b56d7-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="b56d7-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b56d7-115">**Tag Syntax**</span></span>

<span data-ttu-id="b56d7-116"><v: *elemento* src = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b56d7-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="b56d7-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b56d7-117">**Script Syntax**</span></span>

<span data-ttu-id="b56d7-118">*Element* . src = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b56d7-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="b56d7-119">*expresión* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="b56d7-119">*expression*=*element*.src</span></span>

<span data-ttu-id="b56d7-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b56d7-120">**Remarks**</span></span>

<span data-ttu-id="b56d7-121">Este atributo siempre debe usarse con el elemento [ImageData](msdn-online-vml-imagedata-element.md) y apuntar a datos de imagen válidos para que se muestre una imagen.</span><span class="sxs-lookup"><span data-stu-id="b56d7-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="b56d7-122">Si este atributo aparece sin [href](https://www.bing.com/search?q=HRef) o [title](title-attribute--imagedata--vml.md), la imagen está vinculada.</span><span class="sxs-lookup"><span data-stu-id="b56d7-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="b56d7-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b56d7-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b56d7-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b56d7-124">**Example**</span></span>

<span data-ttu-id="b56d7-125">El origen de la imagen es un archivo denominado "kids.jpg".</span><span class="sxs-lookup"><span data-stu-id="b56d7-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 