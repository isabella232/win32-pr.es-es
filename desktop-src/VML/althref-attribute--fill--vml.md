---
title: Atributo AltHRef (relleno) (VML)
description: Atributo AltHRef (relleno) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487886"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="13a08-103">Atributo AltHRef (relleno) (VML)</span><span class="sxs-lookup"><span data-stu-id="13a08-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="13a08-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="13a08-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="13a08-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="13a08-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="13a08-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="13a08-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="13a08-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="13a08-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="13a08-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="13a08-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="13a08-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="13a08-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="13a08-110">Define una referencia alternativa para una imagen.</span><span class="sxs-lookup"><span data-stu-id="13a08-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="13a08-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13a08-111">Read/write.</span></span> <span data-ttu-id="13a08-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="13a08-112">**String**.</span></span>

<span data-ttu-id="13a08-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="13a08-113">**Applies To**</span></span>

[<span data-ttu-id="13a08-114">Fill</span><span class="sxs-lookup"><span data-stu-id="13a08-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="13a08-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="13a08-115">**Tag Syntax**</span></span>

<span data-ttu-id="13a08-116"><v: *Element* o:althref = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="13a08-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="13a08-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="13a08-117">**Script Syntax**</span></span>

<span data-ttu-id="13a08-118">*Element* . althref = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="13a08-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="13a08-119">*expresión* = de *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="13a08-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="13a08-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="13a08-120">**Remarks**</span></span>

<span data-ttu-id="13a08-121">Admite la conservación de datos PICT a través de Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="13a08-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="13a08-122">En la escritura HTML, se guarda la representación alternativa (los datos PICT originales si el archivo se originó en Apple Macintosh).</span><span class="sxs-lookup"><span data-stu-id="13a08-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="13a08-123">En la lectura de HTML, **AltHRef** se favorece en **src**.</span><span class="sxs-lookup"><span data-stu-id="13a08-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="13a08-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="13a08-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="13a08-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="13a08-125">**Example**</span></span>

<span data-ttu-id="13a08-126">El relleno de la forma tiene un **AltHRef** que señala a un archivo denominado myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="13a08-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 