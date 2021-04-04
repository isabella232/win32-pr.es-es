---
title: Atributo ImageSize de VML
description: Atributo ImageSize de VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792214"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="ee49a-103">Atributo ImageSize de VML</span><span class="sxs-lookup"><span data-stu-id="ee49a-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="ee49a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ee49a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ee49a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ee49a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ee49a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ee49a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ee49a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ee49a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ee49a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ee49a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ee49a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ee49a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ee49a-110">Define el tamaño de la imagen del trazo.</span><span class="sxs-lookup"><span data-stu-id="ee49a-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="ee49a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ee49a-111">Read/write.</span></span> <span data-ttu-id="ee49a-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ee49a-112">**VgVector2D**.</span></span>

<span data-ttu-id="ee49a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ee49a-113">**Applies To**</span></span>

[<span data-ttu-id="ee49a-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="ee49a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ee49a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ee49a-115">**Tag Syntax**</span></span>

<span data-ttu-id="ee49a-116"><v: *elemento* ImageSize = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="ee49a-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="ee49a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="ee49a-117">**Script Syntax**</span></span>

<span data-ttu-id="ee49a-118">*Element* . ImageSize = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="ee49a-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="ee49a-119">*expresión* = de *elemento*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="ee49a-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="ee49a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ee49a-120">**Remarks**</span></span>

<span data-ttu-id="ee49a-121">El valor predeterminado es el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ee49a-121">Default is the size of the image.</span></span>

<span data-ttu-id="ee49a-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="ee49a-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ee49a-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ee49a-123">**Example**</span></span>

<span data-ttu-id="ee49a-124">La imagen del trazo tendrá un tamaño de 10 por 10 puntos.</span><span class="sxs-lookup"><span data-stu-id="ee49a-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 