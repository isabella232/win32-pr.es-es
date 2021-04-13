---
title: Atributo ViewpointOrigin de VML
description: Atributo ViewpointOrigin de VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487855"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="3a78a-103">Atributo ViewpointOrigin de VML</span><span class="sxs-lookup"><span data-stu-id="3a78a-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="3a78a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3a78a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3a78a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3a78a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3a78a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3a78a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3a78a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3a78a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3a78a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3a78a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3a78a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3a78a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3a78a-110">Define el origen del punto de vista en el cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="3a78a-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="3a78a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a78a-111">Read/write.</span></span> <span data-ttu-id="3a78a-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3a78a-112">**VgVector2D**.</span></span>

<span data-ttu-id="3a78a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3a78a-113">**Applies To**</span></span>

[<span data-ttu-id="3a78a-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="3a78a-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="3a78a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3a78a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3a78a-116"><o: *elemento* viewpointorigin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3a78a-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="3a78a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3a78a-117">**Script Syntax**</span></span>

<span data-ttu-id="3a78a-118">*Element* . viewpointorigin = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3a78a-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="3a78a-119">*expresión* = de *elemento*. viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="3a78a-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="3a78a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3a78a-120">**Remarks**</span></span>

<span data-ttu-id="3a78a-121">Define el Viewpoint en términos de los valores x e y de la forma original.</span><span class="sxs-lookup"><span data-stu-id="3a78a-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="3a78a-122">Los valores x e y van de 0,5 a-0,5 (50% a-50% del origen de coordenadas de la forma).</span><span class="sxs-lookup"><span data-stu-id="3a78a-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="3a78a-123">El valor predeterminado es 0, 0.</span><span class="sxs-lookup"><span data-stu-id="3a78a-123">The default is 0,0.</span></span>

<span data-ttu-id="3a78a-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="3a78a-124">*Microsoft Office Extensions Attribute*</span></span>

 

 