---
title: Atributo ColorMode de VML
description: Atributo ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420930"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="67969-103">Atributo ColorMode de VML</span><span class="sxs-lookup"><span data-stu-id="67969-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="67969-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="67969-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="67969-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="67969-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="67969-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="67969-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="67969-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="67969-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="67969-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="67969-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="67969-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="67969-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="67969-110">Determina el modo de color de extrusión.</span><span class="sxs-lookup"><span data-stu-id="67969-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="67969-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67969-111">Read/write.</span></span> <span data-ttu-id="67969-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="67969-112">**VgTriState**.</span></span>

<span data-ttu-id="67969-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="67969-113">**Applies To**</span></span>

[<span data-ttu-id="67969-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="67969-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="67969-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="67969-115">**Tag Syntax**</span></span>

<span data-ttu-id="67969-116"><o: *elemento* ColorMode = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="67969-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="67969-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="67969-117">**Script Syntax**</span></span>

<span data-ttu-id="67969-118">*Element* . ColorMode = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="67969-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="67969-119">*expresión* = de *elemento*. ColorMode</span><span class="sxs-lookup"><span data-stu-id="67969-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="67969-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="67969-120">**Remarks**</span></span>

<span data-ttu-id="67969-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="67969-121">Values include:</span></span>



| <span data-ttu-id="67969-122">Value</span><span class="sxs-lookup"><span data-stu-id="67969-122">Value</span></span>  | <span data-ttu-id="67969-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="67969-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67969-124">auto</span><span class="sxs-lookup"><span data-stu-id="67969-124">auto</span></span>   | <span data-ttu-id="67969-125">Especifica que el color de la extrusión es el mismo que el color de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="67969-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="67969-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="67969-126">Default.</span></span>                |
| <span data-ttu-id="67969-127">custom</span><span class="sxs-lookup"><span data-stu-id="67969-127">custom</span></span> | <span data-ttu-id="67969-128">Especifica que la extrusión será el color del atributo de [color](color-attribute--extrusion--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="67969-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="67969-129">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="67969-129">*Microsoft Office Extensions Attribute*</span></span>

 

 