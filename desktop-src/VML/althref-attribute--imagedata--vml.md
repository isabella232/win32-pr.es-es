---
title: Atributo AltHRef (ImageData) (VML)
description: Atributo AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077938"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="21eca-103">Atributo AltHRef (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="21eca-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="21eca-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21eca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21eca-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="21eca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21eca-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="21eca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21eca-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="21eca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21eca-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21eca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21eca-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21eca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21eca-110">Especifica una referencia alternativa para una imagen.</span><span class="sxs-lookup"><span data-stu-id="21eca-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="21eca-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="21eca-111">Read/write.</span></span> <span data-ttu-id="21eca-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="21eca-112">**String**.</span></span>

<span data-ttu-id="21eca-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="21eca-113">**Applies To**</span></span>

[<span data-ttu-id="21eca-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="21eca-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="21eca-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="21eca-115">**Tag Syntax**</span></span>

<span data-ttu-id="21eca-116"><v: *Element* o:althref = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="21eca-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="21eca-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="21eca-117">**Script Syntax**</span></span>

<span data-ttu-id="21eca-118">*Element* . althref = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="21eca-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="21eca-119">*expresión* = de *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="21eca-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="21eca-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="21eca-120">**Remarks**</span></span>

<span data-ttu-id="21eca-121">Admite la conservación de datos PICT a través de Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="21eca-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="21eca-122">En la escritura en HTML, se guarda la representación alternativa (es decir, los datos PICT originales si el archivo se originó en el equipo Macintosh).</span><span class="sxs-lookup"><span data-stu-id="21eca-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="21eca-123">En una lectura de HTML, **AltHRef** se favorece en **src**.</span><span class="sxs-lookup"><span data-stu-id="21eca-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="21eca-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="21eca-124">*Microsoft Office Extensions Attribute*</span></span>

 

 