---
title: Src (atributo, Stroke) (VML)
description: Src (atributo, Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791806"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="7d9c5-103">Src (atributo, Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="7d9c5-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="7d9c5-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7d9c5-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7d9c5-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7d9c5-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7d9c5-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7d9c5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7d9c5-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7d9c5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7d9c5-110">Define la imagen de origen que se va a cargar para un relleno de trazo.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="7d9c5-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7d9c5-111">Read/write.</span></span> <span data-ttu-id="7d9c5-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-112">**String**.</span></span>

<span data-ttu-id="7d9c5-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-113">**Applies To**</span></span>

[<span data-ttu-id="7d9c5-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7d9c5-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7d9c5-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-115">**Tag Syntax**</span></span>

<span data-ttu-id="7d9c5-116"><v: *elemento* src = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="7d9c5-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="7d9c5-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-117">**Script Syntax**</span></span>

<span data-ttu-id="7d9c5-118">*Element* . src = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="7d9c5-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="7d9c5-119">*expresión* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="7d9c5-119">*expression*=*element*.src</span></span>

<span data-ttu-id="7d9c5-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-120">**Remarks**</span></span>

<span data-ttu-id="7d9c5-121">Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="7d9c5-122">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="7d9c5-123">Si este atributo aparece solo, es decir, sin **href** ni **title**, la imagen se vincula.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="7d9c5-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="7d9c5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="7d9c5-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-125">**Example**</span></span>

<span data-ttu-id="7d9c5-126">El trazo se crea con la imagen especificada por el archivo de cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 