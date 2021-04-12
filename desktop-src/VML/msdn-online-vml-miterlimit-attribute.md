---
title: Atributo MiterLimit de VML
description: Atributo MiterLimit de VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487878"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="8daa0-103">Atributo MiterLimit de VML</span><span class="sxs-lookup"><span data-stu-id="8daa0-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="8daa0-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8daa0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8daa0-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8daa0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8daa0-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8daa0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8daa0-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8daa0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8daa0-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8daa0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8daa0-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8daa0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8daa0-110">Define la suavidad de la unión angular.</span><span class="sxs-lookup"><span data-stu-id="8daa0-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="8daa0-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8daa0-111">Read/write.</span></span> <span data-ttu-id="8daa0-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="8daa0-112">**VgNumber**.</span></span>

<span data-ttu-id="8daa0-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8daa0-113">**Applies To**</span></span>

[<span data-ttu-id="8daa0-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="8daa0-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="8daa0-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8daa0-115">**Tag Syntax**</span></span>

<span data-ttu-id="8daa0-116"><v: *Element* miterLimit = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8daa0-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="8daa0-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8daa0-117">**Script Syntax**</span></span>

<span data-ttu-id="8daa0-118">*Element* . miterLimit = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8daa0-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="8daa0-119">*expresión* = de *elemento*. miterLimit</span><span class="sxs-lookup"><span data-stu-id="8daa0-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="8daa0-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8daa0-120">**Remarks**</span></span>

<span data-ttu-id="8daa0-121">Distancia máxima entre el punto interno y el punto exterior de una Unión.</span><span class="sxs-lookup"><span data-stu-id="8daa0-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="8daa0-122">Este número es un múltiplo del grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="8daa0-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="8daa0-123">El valor predeterminado es 8.</span><span class="sxs-lookup"><span data-stu-id="8daa0-123">The default value is 8.</span></span>

<span data-ttu-id="8daa0-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8daa0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="8daa0-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8daa0-125">**Example**</span></span>

<span data-ttu-id="8daa0-126">Las uniones en la polilínea están en ángulo con un límite de 10, es decir, 5 veces 2 puntos.</span><span class="sxs-lookup"><span data-stu-id="8daa0-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 