---
title: Atributo WrapCoords de VML
description: Atributo WrapCoords de VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792123"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="08332-103">Atributo WrapCoords de VML</span><span class="sxs-lookup"><span data-stu-id="08332-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="08332-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08332-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08332-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="08332-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08332-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="08332-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08332-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="08332-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08332-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08332-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08332-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08332-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08332-110">Define el polígono delimitador que rodea una forma.</span><span class="sxs-lookup"><span data-stu-id="08332-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="08332-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08332-111">Read/write.</span></span> <span data-ttu-id="08332-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="08332-112">**String**.</span></span>

<span data-ttu-id="08332-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="08332-113">**Applies To**</span></span>

[<span data-ttu-id="08332-114">Forma</span><span class="sxs-lookup"><span data-stu-id="08332-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="08332-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="08332-115">**Tag Syntax**</span></span>

<span data-ttu-id="08332-116"><v: *Element* o:wrapcoords = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="08332-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="08332-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="08332-117">**Remarks**</span></span>

<span data-ttu-id="08332-118">Describe una lista delimitada por comas de x y ycoordinates; es decir, "x1, Y1, x2, Y2, x3, Y3,..." Se usa cuando el texto se ajusta estrechamente alrededor de una forma.</span><span class="sxs-lookup"><span data-stu-id="08332-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="08332-119">El valor predeterminado es **null** (una cadena vacía) hasta que el atributo **MSO-Wrap-Mode** esté establecido en **tight** o **a través** de.</span><span class="sxs-lookup"><span data-stu-id="08332-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="08332-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="08332-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="08332-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="08332-121">**Example**</span></span>

<span data-ttu-id="08332-122">La forma tiene un cuadro de límite de ajuste de texto que es 5 unidades mayor que la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="08332-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 