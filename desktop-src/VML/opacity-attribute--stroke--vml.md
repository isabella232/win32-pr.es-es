---
title: Opacity (atributo) (Stroke) (VML)
description: Opacity (atributo) (Stroke) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488242"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="c43c8-103">Opacity (atributo) (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="c43c8-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="c43c8-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c43c8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c43c8-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c43c8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c43c8-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="c43c8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c43c8-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c43c8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c43c8-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c43c8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c43c8-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c43c8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c43c8-110">Define la cantidad de transparencia de un trazo.</span><span class="sxs-lookup"><span data-stu-id="c43c8-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="c43c8-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c43c8-111">Read/write.</span></span> <span data-ttu-id="c43c8-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="c43c8-112">**VgFraction**.</span></span>

<span data-ttu-id="c43c8-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="c43c8-113">**Applies To**</span></span>

[<span data-ttu-id="c43c8-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="c43c8-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="c43c8-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="c43c8-115">**Tag Syntax**</span></span>

<span data-ttu-id="c43c8-116"><v: *elemento* Opacity = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="c43c8-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="c43c8-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="c43c8-117">**Script Syntax**</span></span>

<span data-ttu-id="c43c8-118">*elemento* . Opacity = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="c43c8-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="c43c8-119">*expresión* = de *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="c43c8-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="c43c8-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="c43c8-120">**Remarks**</span></span>

<span data-ttu-id="c43c8-121">El valor predeterminado es 1,0.</span><span class="sxs-lookup"><span data-stu-id="c43c8-121">The default value is 1.0.</span></span>

<span data-ttu-id="c43c8-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="c43c8-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="c43c8-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="c43c8-123">**Example**</span></span>

<span data-ttu-id="c43c8-124">El trazo es un 50% transparente.</span><span class="sxs-lookup"><span data-stu-id="c43c8-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 