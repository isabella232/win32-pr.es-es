---
title: Atributo ImageAlignShape de VML
description: Atributo ImageAlignShape de VML
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359135"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="f420b-103">Atributo ImageAlignShape de VML</span><span class="sxs-lookup"><span data-stu-id="f420b-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="f420b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f420b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f420b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f420b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f420b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f420b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f420b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f420b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f420b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f420b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f420b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f420b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f420b-110">Determina la alineación de la imagen del trazo.</span><span class="sxs-lookup"><span data-stu-id="f420b-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="f420b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f420b-111">Read/write.</span></span> <span data-ttu-id="f420b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f420b-112">**VgTriState**.</span></span>

<span data-ttu-id="f420b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f420b-113">**Applies To**</span></span>

[<span data-ttu-id="f420b-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="f420b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="f420b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f420b-115">**Tag Syntax**</span></span>

<span data-ttu-id="f420b-116"><v:</span><span class="sxs-lookup"><span data-stu-id="f420b-116"><v:</span></span>

<span data-ttu-id="f420b-117">Element *imagealignshape = "* expresión *" >*</span><span class="sxs-lookup"><span data-stu-id="f420b-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="f420b-118">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f420b-118">**Script Syntax**</span></span>

<span data-ttu-id="f420b-119">Element *. imagealignshape = "* expresión *"*</span><span class="sxs-lookup"><span data-stu-id="f420b-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="f420b-120">*=* elemento Expression *. imagealignshape*</span><span class="sxs-lookup"><span data-stu-id="f420b-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="f420b-121">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f420b-121">**Remarks**</span></span>

<span data-ttu-id="f420b-122">Si **es true**, alinea la imagen con la forma, de lo contrario, la imagen se alinea con la ventana.</span><span class="sxs-lookup"><span data-stu-id="f420b-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="f420b-123">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="f420b-123">The default is **True**.</span></span>

<span data-ttu-id="f420b-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="f420b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f420b-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f420b-125">**Example**</span></span>

<span data-ttu-id="f420b-126">La imagen se alinea con la ventana.</span><span class="sxs-lookup"><span data-stu-id="f420b-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 