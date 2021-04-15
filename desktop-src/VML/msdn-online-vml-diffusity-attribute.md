---
title: Atributo de difusión VML
description: Atributo de difusión VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a8e51750bcd71421609221812eb38bbf709657
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695615"
---
# <a name="vml-diffusity-attribute"></a><span data-ttu-id="14fbd-103">Atributo de difusión VML</span><span class="sxs-lookup"><span data-stu-id="14fbd-103">VML Diffusity Attribute</span></span>

<span data-ttu-id="14fbd-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="14fbd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="14fbd-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="14fbd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="14fbd-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="14fbd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="14fbd-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="14fbd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="14fbd-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="14fbd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="14fbd-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="14fbd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="14fbd-110">Define la cantidad de difusión de la luz reflejada a partir de una forma extruida.</span><span class="sxs-lookup"><span data-stu-id="14fbd-110">Defines the amount of diffusion of reflected light from an extruded shape.</span></span> <span data-ttu-id="14fbd-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="14fbd-111">Read/write.</span></span> <span data-ttu-id="14fbd-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="14fbd-112">**VgNumber**.</span></span>

<span data-ttu-id="14fbd-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="14fbd-113">**Applies To**</span></span>

[<span data-ttu-id="14fbd-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="14fbd-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="14fbd-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="14fbd-115">**Tag Syntax**</span></span>

<span data-ttu-id="14fbd-116"><o: difusión de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="14fbd-116"><o: *element* diffusity=" *expression* "></span></span>

<span data-ttu-id="14fbd-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="14fbd-117">**Script Syntax**</span></span>

<span data-ttu-id="14fbd-118">*Element* . difusa = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="14fbd-118">*element* .diffusity="*expression*"</span></span>

<span data-ttu-id="14fbd-119">*expresión* = de *elemento*. difusión</span><span class="sxs-lookup"><span data-stu-id="14fbd-119">*expression*=*element*.diffusity</span></span>

<span data-ttu-id="14fbd-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="14fbd-120">**Remarks**</span></span>

<span data-ttu-id="14fbd-121">Este valor define la relación de la luz de incidente con la luz reflejada difusa.</span><span class="sxs-lookup"><span data-stu-id="14fbd-121">This value defines the ratio of incident light to diffused reflected light.</span></span> <span data-ttu-id="14fbd-122">Los valores normales oscilan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="14fbd-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="14fbd-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="14fbd-123">The default value is 0.</span></span>

<span data-ttu-id="14fbd-124">Si se especifican valores mayores que 1, se pueden producir efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="14fbd-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="14fbd-125">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="14fbd-125">*Microsoft Office Extensions Attribute*</span></span>

 

 