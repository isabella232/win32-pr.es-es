---
title: Atributo AltHRef (Stroke) (VML)
description: Atributo AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695716"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="4c560-103">Atributo AltHRef (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="4c560-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="4c560-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4c560-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4c560-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4c560-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4c560-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4c560-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4c560-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4c560-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4c560-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4c560-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4c560-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4c560-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4c560-110">Especifica una referencia alternativa para una imagen.</span><span class="sxs-lookup"><span data-stu-id="4c560-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="4c560-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4c560-111">Read/write.</span></span> <span data-ttu-id="4c560-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="4c560-112">**String**.</span></span>

<span data-ttu-id="4c560-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4c560-113">**Applies To**</span></span>

[<span data-ttu-id="4c560-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="4c560-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="4c560-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4c560-115">**Tag Syntax**</span></span>

<span data-ttu-id="4c560-116"><v: *Element* o:althref = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4c560-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="4c560-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4c560-117">**Script Syntax**</span></span>

<span data-ttu-id="4c560-118">*Element* . althref = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4c560-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="4c560-119">*expresión* = de *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="4c560-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="4c560-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4c560-120">**Remarks**</span></span>

<span data-ttu-id="4c560-121">Admite la conservación de datos PICT a través de Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="4c560-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="4c560-122">En la escritura HTML, se guarda la representación alternativa (es decir, los datos PICT originales si el archivo se originó en el equipo Macintosh).</span><span class="sxs-lookup"><span data-stu-id="4c560-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="4c560-123">En la lectura de HTML, **AltHRef** se favorece en **src**.</span><span class="sxs-lookup"><span data-stu-id="4c560-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="4c560-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="4c560-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="4c560-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4c560-125">**Example**</span></span>

<span data-ttu-id="4c560-126">El trazo de la forma tiene un **AltHRef** que señala a un archivo denominado myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="4c560-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 