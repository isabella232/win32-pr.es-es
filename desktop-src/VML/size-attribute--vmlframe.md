---
title: Atributo size (VMLFrame)
description: Atributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077816"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="00916-103">Atributo size (VMLFrame)</span><span class="sxs-lookup"><span data-stu-id="00916-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="00916-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="00916-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="00916-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="00916-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="00916-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="00916-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="00916-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="00916-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="00916-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="00916-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="00916-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="00916-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="00916-110">Define el tamaño de la región de recorte del marco.</span><span class="sxs-lookup"><span data-stu-id="00916-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="00916-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="00916-111">Read/write.</span></span> <span data-ttu-id="00916-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="00916-112">**VgVector2D**.</span></span>

<span data-ttu-id="00916-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="00916-113">**Applies To**</span></span>

[<span data-ttu-id="00916-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="00916-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="00916-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="00916-115">**Tag Syntax**</span></span>

<span data-ttu-id="00916-116"><v: *elemento* size = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="00916-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="00916-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="00916-117">**Script Syntax**</span></span>

<span data-ttu-id="00916-118">*Element* . size = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="00916-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="00916-119">*expresión* = de *elemento*. Size</span><span class="sxs-lookup"><span data-stu-id="00916-119">*expression*=*element*.size</span></span>

<span data-ttu-id="00916-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="00916-120">**Remarks**</span></span>

<span data-ttu-id="00916-121">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="00916-121">The default value is 0,0.</span></span> <span data-ttu-id="00916-122">Tenga en cuenta que **el tamaño** solo funciona si [clip](msdn-online-vml-clip-attribute.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="00916-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="00916-123">En este atributo, el tamaño se define como el ancho y el alto del marco.</span><span class="sxs-lookup"><span data-stu-id="00916-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="00916-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="00916-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="00916-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="00916-125">**Example**</span></span>

<span data-ttu-id="00916-126">El tamaño de la región de recorte será 50pt, 50pt.</span><span class="sxs-lookup"><span data-stu-id="00916-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 