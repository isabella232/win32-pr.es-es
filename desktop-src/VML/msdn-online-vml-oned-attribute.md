---
title: Atributo OnEd de VML
description: Atributo OnEd de VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359359"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="2019e-103">Atributo OnEd de VML</span><span class="sxs-lookup"><span data-stu-id="2019e-103">VML OnEd Attribute</span></span>

<span data-ttu-id="2019e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2019e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2019e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="2019e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2019e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="2019e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2019e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2019e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2019e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2019e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2019e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2019e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2019e-110">Determina si los controladores adicionales de una forma están ocultos.</span><span class="sxs-lookup"><span data-stu-id="2019e-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="2019e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2019e-111">Read/write.</span></span> <span data-ttu-id="2019e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="2019e-112">**VgTriState**.</span></span>

<span data-ttu-id="2019e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2019e-113">**Applies To**</span></span>

[<span data-ttu-id="2019e-114">Forma</span><span class="sxs-lookup"><span data-stu-id="2019e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2019e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="2019e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2019e-116"><v: *Element* o:oned = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="2019e-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="2019e-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="2019e-117">**Remarks**</span></span>

<span data-ttu-id="2019e-118">Oculta todos los controladores de forma excepto la parte superior izquierda e inferior derecha; es decir, los mismos identificadores que se usan para un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="2019e-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="2019e-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="2019e-119">The default is **False**.</span></span>

<span data-ttu-id="2019e-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="2019e-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="2019e-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2019e-121">**Example**</span></span>

<span data-ttu-id="2019e-122">Todos los manipuladores, excepto los de la parte superior izquierda e inferior derecha de la forma, están ocultos.</span><span class="sxs-lookup"><span data-stu-id="2019e-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 