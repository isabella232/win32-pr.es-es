---
title: Atributo de modo encapsulado de VML MSO
description: Atributo de modo encapsulado de VML MSO
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359128"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="4790b-103">Atributo de modo encapsulado de VML MSO</span><span class="sxs-lookup"><span data-stu-id="4790b-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="4790b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4790b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4790b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4790b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4790b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4790b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4790b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4790b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4790b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4790b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4790b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4790b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4790b-110">Define el modo de ajuste del texto.</span><span class="sxs-lookup"><span data-stu-id="4790b-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="4790b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4790b-111">Read/write.</span></span> <span data-ttu-id="4790b-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="4790b-112">**String**.</span></span>

<span data-ttu-id="4790b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4790b-113">**Applies To**</span></span>

[<span data-ttu-id="4790b-114">Forma</span><span class="sxs-lookup"><span data-stu-id="4790b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4790b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4790b-115">**Tag Syntax**</span></span>

<span data-ttu-id="4790b-116"><v: *Element* style = "MSO-Wrap-Mode: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4790b-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="4790b-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4790b-117">**Remarks**</span></span>

<span data-ttu-id="4790b-118">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="4790b-118">Values include:</span></span>



| <span data-ttu-id="4790b-119">Value</span><span class="sxs-lookup"><span data-stu-id="4790b-119">Value</span></span>          | <span data-ttu-id="4790b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4790b-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="4790b-121">square</span><span class="sxs-lookup"><span data-stu-id="4790b-121">square</span></span>         | <span data-ttu-id="4790b-122">Ajusta el texto alrededor de la forma de un cuadrado.</span><span class="sxs-lookup"><span data-stu-id="4790b-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="4790b-123">acoplamiento</span><span class="sxs-lookup"><span data-stu-id="4790b-123">tight</span></span>          | <span data-ttu-id="4790b-124">El texto se ajusta cerca de la forma.</span><span class="sxs-lookup"><span data-stu-id="4790b-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="4790b-125">superior e inferior</span><span class="sxs-lookup"><span data-stu-id="4790b-125">top-and-bottom</span></span> | <span data-ttu-id="4790b-126">El texto salta de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="4790b-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="4790b-127">a través de</span><span class="sxs-lookup"><span data-stu-id="4790b-127">through</span></span>        | <span data-ttu-id="4790b-128">El texto se muestra a través de la forma.</span><span class="sxs-lookup"><span data-stu-id="4790b-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="4790b-129">ninguno</span><span class="sxs-lookup"><span data-stu-id="4790b-129">none</span></span>           | <span data-ttu-id="4790b-130">El texto no se ajusta.</span><span class="sxs-lookup"><span data-stu-id="4790b-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="4790b-131">Microsoft PowerPoint lo usa para guardar en HTML para indicar si el ajuste de palabra dentro de una autoforma está activado (**cuadrado**) o desactivado (**ninguno**).</span><span class="sxs-lookup"><span data-stu-id="4790b-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="4790b-132">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="4790b-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="4790b-133">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4790b-133">**Example**</span></span>

<span data-ttu-id="4790b-134">El código siguiente indica que WordWrap está activado en PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="4790b-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 