---
title: Atributo de faceta VML
description: Atributo de faceta VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149375"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="cd65f-103">Atributo de faceta VML</span><span class="sxs-lookup"><span data-stu-id="cd65f-103">VML Facet Attribute</span></span>

<span data-ttu-id="cd65f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cd65f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cd65f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="cd65f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cd65f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="cd65f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cd65f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="cd65f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cd65f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cd65f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cd65f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cd65f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cd65f-110">Define el número de caras utilizadas para describir las superficies curvas de una extrusión.</span><span class="sxs-lookup"><span data-stu-id="cd65f-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="cd65f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cd65f-111">Read/write.</span></span> <span data-ttu-id="cd65f-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="cd65f-112">**VgNumber**.</span></span>

<span data-ttu-id="cd65f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="cd65f-113">**Applies To**</span></span>

[<span data-ttu-id="cd65f-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="cd65f-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="cd65f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="cd65f-115">**Tag Syntax**</span></span>

<span data-ttu-id="cd65f-116"><o: *elemento* Facet = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="cd65f-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="cd65f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="cd65f-117">**Script Syntax**</span></span>

<span data-ttu-id="cd65f-118">*Element* . Facet = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="cd65f-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="cd65f-119">*expresión* = de *elemento*. Facet</span><span class="sxs-lookup"><span data-stu-id="cd65f-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="cd65f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="cd65f-120">**Remarks**</span></span>

<span data-ttu-id="cd65f-121">Define la manera en que un motor de representación aproximará la extrusión.</span><span class="sxs-lookup"><span data-stu-id="cd65f-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="cd65f-122">Un número menor indicará una tolerancia de representación inferior al motor de representación y producirá más aspectos.</span><span class="sxs-lookup"><span data-stu-id="cd65f-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="cd65f-123">Los números más altos harán que la extrusión parezca más faceteada.</span><span class="sxs-lookup"><span data-stu-id="cd65f-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="cd65f-124">El valor predeterminado es 30.000.</span><span class="sxs-lookup"><span data-stu-id="cd65f-124">The default value is 30,000.</span></span>

<span data-ttu-id="cd65f-125">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="cd65f-125">*Microsoft Office Extensions Attribute*</span></span>

 

 