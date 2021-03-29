---
title: Atributo de puntos VML
description: Atributo de puntos VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077847"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="ccedc-103">Atributo de puntos VML</span><span class="sxs-lookup"><span data-stu-id="ccedc-103">VML Points Attribute</span></span>

<span data-ttu-id="ccedc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ccedc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ccedc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ccedc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ccedc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ccedc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ccedc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ccedc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ccedc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ccedc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ccedc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ccedc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ccedc-110">Define un conjunto de puntos que forman una polilínea.</span><span class="sxs-lookup"><span data-stu-id="ccedc-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="ccedc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ccedc-111">Read/write.</span></span> <span data-ttu-id="ccedc-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ccedc-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="ccedc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ccedc-113">**Applies To**</span></span>

[<span data-ttu-id="ccedc-114">Polilínea</span><span class="sxs-lookup"><span data-stu-id="ccedc-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="ccedc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ccedc-115">**Tag Syntax**</span></span>

<span data-ttu-id="ccedc-116"><v: *elemento* Points = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="ccedc-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="ccedc-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="ccedc-117">**Script Syntax**</span></span>

<span data-ttu-id="ccedc-118">*Element* . Points = "*expresión \* *"**</span><span class="sxs-lookup"><span data-stu-id="ccedc-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="ccedc-119">*expresión* = de *elemento*. Points</span><span class="sxs-lookup"><span data-stu-id="ccedc-119">*expression*=*element*.points</span></span>

<span data-ttu-id="ccedc-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ccedc-120">**Remarks**</span></span>

<span data-ttu-id="ccedc-121">Define un conjunto de segmentos de línea recta que se componen de una serie de puntos.</span><span class="sxs-lookup"><span data-stu-id="ccedc-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="ccedc-122">Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="ccedc-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="ccedc-123">El valor predeterminado es "0, 0 10, 10".</span><span class="sxs-lookup"><span data-stu-id="ccedc-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="ccedc-124">Tenga en cuenta que no se requieren comas, pero facilitan la lectura.</span><span class="sxs-lookup"><span data-stu-id="ccedc-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="ccedc-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="ccedc-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="ccedc-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ccedc-126">**Example**</span></span>

<span data-ttu-id="ccedc-127">La polilínea comienza en el punto 10, 10 y termina en 100.100, con los valores en puntos.</span><span class="sxs-lookup"><span data-stu-id="ccedc-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 