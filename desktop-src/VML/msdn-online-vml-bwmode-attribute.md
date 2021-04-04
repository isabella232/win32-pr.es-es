---
title: Atributo BWMode de VML
description: Atributo BWMode de VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792370"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="c7880-103">Atributo BWMode de VML</span><span class="sxs-lookup"><span data-stu-id="c7880-103">VML BWMode Attribute</span></span>

<span data-ttu-id="c7880-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c7880-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7880-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c7880-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7880-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="c7880-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7880-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c7880-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7880-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7880-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7880-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7880-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7880-110">Determina cómo se representará una forma para dispositivos de salida en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="c7880-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="c7880-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c7880-111">Read/write.</span></span> <span data-ttu-id="c7880-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c7880-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="c7880-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="c7880-113">**Applies To**</span></span>

[<span data-ttu-id="c7880-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c7880-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c7880-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="c7880-115">**Tag Syntax**</span></span>

<span data-ttu-id="c7880-116"><v: *Element* o:bwmode = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="c7880-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="c7880-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="c7880-117">**Remarks**</span></span>

<span data-ttu-id="c7880-118">Cuando una forma se imprime en una impresora de color negro y blanco o se muestra en una vista de color negro y blanco en una aplicación, es posible que haya varias opciones.</span><span class="sxs-lookup"><span data-stu-id="c7880-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="c7880-119">Para obtener más información sobre los valores de este atributo, vea el tema [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="c7880-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="c7880-120">El valor predeterminado es **automático**.</span><span class="sxs-lookup"><span data-stu-id="c7880-120">The default value is **auto**.</span></span>

<span data-ttu-id="c7880-121">Si se especifica **auto** , [BWNormal](msdn-online-vml-bwnormal-attribute.md) se usa para determinar el comportamiento de la salida normal de blanco y negro, y [BWPure](msdn-online-vml-bwpure-attribute.md) se usa para determinar el comportamiento de los resultados puros en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="c7880-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="c7880-122">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="c7880-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c7880-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="c7880-123">**Example**</span></span>

<span data-ttu-id="c7880-124">El modo de blanco y negro de la forma es **automático**.</span><span class="sxs-lookup"><span data-stu-id="c7880-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 