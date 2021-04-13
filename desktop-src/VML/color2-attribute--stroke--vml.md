---
title: Atributo color2 (Stroke) (VML)
description: Atributo color2 (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488043"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="60373-103">Atributo color2 (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="60373-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="60373-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="60373-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="60373-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="60373-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="60373-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="60373-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="60373-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="60373-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="60373-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="60373-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="60373-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="60373-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="60373-110">Define un segundo color para los trazos.</span><span class="sxs-lookup"><span data-stu-id="60373-110">Defines a second color for strokes.</span></span> <span data-ttu-id="60373-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="60373-111">Read/write.</span></span> <span data-ttu-id="60373-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="60373-112">**String**.</span></span>

<span data-ttu-id="60373-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="60373-113">**Applies To**</span></span>

[<span data-ttu-id="60373-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="60373-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="60373-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="60373-115">**Tag Syntax**</span></span>

<span data-ttu-id="60373-116"><v: *elemento* color2 = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="60373-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="60373-117">Sintaxis de script</span><span class="sxs-lookup"><span data-stu-id="60373-117">Script Syntax</span></span>

<span data-ttu-id="60373-118">*Element* . color2 = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="60373-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="60373-119">*expresión* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="60373-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="60373-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="60373-120">**Remarks**</span></span>

<span data-ttu-id="60373-121">Se utiliza un segundo color cuando el tipo de relleno de un trazo es un patrón.</span><span class="sxs-lookup"><span data-stu-id="60373-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="60373-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="60373-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="60373-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="60373-123">**Example**</span></span>

<span data-ttu-id="60373-124">El trazo de la forma es un relleno de patrón en el que la imagen de origen define el relleno, pero el segundo color define el fondo transparente.</span><span class="sxs-lookup"><span data-stu-id="60373-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 