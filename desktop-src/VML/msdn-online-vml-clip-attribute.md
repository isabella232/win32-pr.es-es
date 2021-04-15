---
title: Atributo de clip VML
description: Atributo de clip VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695672"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="318d7-103">Atributo de clip VML</span><span class="sxs-lookup"><span data-stu-id="318d7-103">VML Clip Attribute</span></span>

<span data-ttu-id="318d7-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="318d7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="318d7-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="318d7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="318d7-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="318d7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="318d7-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="318d7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="318d7-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="318d7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="318d7-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="318d7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="318d7-110">Determina si el recorte está activado.</span><span class="sxs-lookup"><span data-stu-id="318d7-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="318d7-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="318d7-111">Read/write.</span></span> <span data-ttu-id="318d7-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="318d7-112">**VgTriState**.</span></span>

<span data-ttu-id="318d7-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="318d7-113">**Applies To**</span></span>

[<span data-ttu-id="318d7-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="318d7-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="318d7-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="318d7-115">**Tag Syntax**</span></span>

<span data-ttu-id="318d7-116"><v: *elemento* clip = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="318d7-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="318d7-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="318d7-117">**Script Syntax**</span></span>

<span data-ttu-id="318d7-118">*Element* . clip = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="318d7-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="318d7-119">*expresión* = de *elemento*. clip</span><span class="sxs-lookup"><span data-stu-id="318d7-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="318d7-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="318d7-120">**Remarks**</span></span>

<span data-ttu-id="318d7-121">Si **clip** es **false**, la forma se escalará para ajustarse al marco.</span><span class="sxs-lookup"><span data-stu-id="318d7-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="318d7-122">Si **es true**, no se mostrarán las partes de la forma que estén fuera del marco.</span><span class="sxs-lookup"><span data-stu-id="318d7-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="318d7-123">Tenga en cuenta que el [origen](origin-attribute--vmlframe--vml.md) y [el tamaño](size-attribute--vmlframe.md) no se usarán a menos que el **recorte** sea **true**.</span><span class="sxs-lookup"><span data-stu-id="318d7-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="318d7-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="318d7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="318d7-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="318d7-125">**Example**</span></span>

<span data-ttu-id="318d7-126">Se recortará la imagen definida en el archivo externo.</span><span class="sxs-lookup"><span data-stu-id="318d7-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 