---
title: Atributo BWPure de VML
description: Atributo BWPure de VML
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904680"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="2230f-103">Atributo BWPure de VML</span><span class="sxs-lookup"><span data-stu-id="2230f-103">VML BWPure Attribute</span></span>

<span data-ttu-id="2230f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2230f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2230f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="2230f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2230f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="2230f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2230f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2230f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2230f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2230f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2230f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2230f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2230f-110">Define el modo de blanco y negro para dispositivos de salida negros y blancos puros.</span><span class="sxs-lookup"><span data-stu-id="2230f-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="2230f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2230f-111">Read/write.</span></span> <span data-ttu-id="2230f-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="2230f-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="2230f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2230f-113">**Applies To**</span></span>

[<span data-ttu-id="2230f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="2230f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2230f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="2230f-115">**Tag Syntax**</span></span>

<span data-ttu-id="2230f-116"><v: *Element* o:bwpure = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="2230f-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="2230f-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="2230f-117">**Remarks**</span></span>

<span data-ttu-id="2230f-118">Cuando [BWMode](msdn-online-vml-bwmode-attribute.md) se establece en **auto**, este atributo se usa para determinar cómo representar la forma en blanco y negro puros.</span><span class="sxs-lookup"><span data-stu-id="2230f-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="2230f-119">Para obtener más información sobre los valores de este atributo, vea el tema [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="2230f-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="2230f-120">El valor predeterminado es **automático**.</span><span class="sxs-lookup"><span data-stu-id="2230f-120">The default is **auto**.</span></span>

<span data-ttu-id="2230f-121">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="2230f-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="2230f-122">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2230f-122">**Example**</span></span>

<span data-ttu-id="2230f-123">La forma se procesa como una imagen de contraste alto para el resultado puro en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="2230f-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 