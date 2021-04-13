---
title: Atributo de brillo de VML
description: Atributo de brillo de VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359004"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="313c2-103">Atributo de brillo de VML</span><span class="sxs-lookup"><span data-stu-id="313c2-103">VML Shininess Attribute</span></span>

<span data-ttu-id="313c2-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="313c2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="313c2-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="313c2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="313c2-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="313c2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="313c2-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="313c2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="313c2-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="313c2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="313c2-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="313c2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="313c2-110">Define la concentración de la luz reflejada en una superficie de extrusión.</span><span class="sxs-lookup"><span data-stu-id="313c2-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="313c2-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="313c2-111">Read/write.</span></span> <span data-ttu-id="313c2-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="313c2-112">**VgNumber**.</span></span>

<span data-ttu-id="313c2-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="313c2-113">**Applies To**</span></span>

[<span data-ttu-id="313c2-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="313c2-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="313c2-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="313c2-115">**Tag Syntax**</span></span>

<span data-ttu-id="313c2-116"><o: *elemento* de brillo = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="313c2-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="313c2-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="313c2-117">**Script Syntax**</span></span>

<span data-ttu-id="313c2-118">*Element* . brillo = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="313c2-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="313c2-119">*expresión* = de *elemento*. brillo</span><span class="sxs-lookup"><span data-stu-id="313c2-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="313c2-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="313c2-120">**Remarks**</span></span>

<span data-ttu-id="313c2-121">Los valores altos (8-10) aproximarían el brillo de un reflejo y los valores bajos (2-3) aproximarían un efecto moteado.</span><span class="sxs-lookup"><span data-stu-id="313c2-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="313c2-122">Los valores de 4-7 son típicos.</span><span class="sxs-lookup"><span data-stu-id="313c2-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="313c2-123">Los reflejos no reflejan otros objetos; solo se reflejan las fuentes de luz de Pinpoint.</span><span class="sxs-lookup"><span data-stu-id="313c2-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="313c2-124">El valor predeterminado es 5.</span><span class="sxs-lookup"><span data-stu-id="313c2-124">Default value is 5.</span></span>

<span data-ttu-id="313c2-125">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="313c2-125">*Microsoft Office Extensions Attribute*</span></span>

 

 