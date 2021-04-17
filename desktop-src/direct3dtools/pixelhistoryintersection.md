---
description: Representa información sobre un determinado.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705247"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="e167f-103"><span id="vspixengine.pixelhistoryintersection"></span>Estructura PixelHistoryIntersection</span><span class="sxs-lookup"><span data-stu-id="e167f-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="e167f-104">Representa información sobre un determinado</span><span class="sxs-lookup"><span data-stu-id="e167f-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="e167f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e167f-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="e167f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e167f-106">Members</span></span>

<span data-ttu-id="e167f-107">**Númeromarco**</span><span class="sxs-lookup"><span data-stu-id="e167f-107">**frameNumber**</span></span>  
<span data-ttu-id="e167f-108">El marco del evento de gráficos asociada con esta operación.</span><span class="sxs-lookup"><span data-stu-id="e167f-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="e167f-109">**Eid**</span><span class="sxs-lookup"><span data-stu-id="e167f-109">**eid**</span></span>  
<span data-ttu-id="e167f-110">IDENTIFICADOR del evento de gráficos asociado a esta operación.</span><span class="sxs-lookup"><span data-stu-id="e167f-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="e167f-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="e167f-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="e167f-112">Destino de representación asociado originalmente (dentro de la aplicación capturada) con esta operación.</span><span class="sxs-lookup"><span data-stu-id="e167f-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="e167f-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="e167f-113">**eventType**</span></span>  
<span data-ttu-id="e167f-114">El tipo de evento asociado a esta operación (en concreto, si este evento es una llamada a Draw).</span><span class="sxs-lookup"><span data-stu-id="e167f-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="e167f-115">**Elija**</span><span class="sxs-lookup"><span data-stu-id="e167f-115">**point**</span></span>  
<span data-ttu-id="e167f-116">Coordenadas del píxel en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e167f-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="e167f-117">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="e167f-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="e167f-118">True si el ensamblador de entrada genera identificadores de instancia; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="e167f-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="e167f-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="e167f-119">**flags**</span></span>  
<span data-ttu-id="e167f-120">Combinación de valores de PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="e167f-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="e167f-121">Para obtener más información, consulte la enumeración PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="e167f-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="e167f-122">**fbInitialRed**</span><span class="sxs-lookup"><span data-stu-id="e167f-122">**fbInitialRed**</span></span>  
<span data-ttu-id="e167f-123">Fotogramas: valor del componente de color rojo de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-124">**fbInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="e167f-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="e167f-125">Fotogramas: valor del componente de color verde de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-126">**fbInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="e167f-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="e167f-127">Fotogramas: valor del componente de color azul de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-128">**fbInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="e167f-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="e167f-129">Fotogramas: valor del componente de color alfa de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-130">**LabelFBInitialRed**</span><span class="sxs-lookup"><span data-stu-id="e167f-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="e167f-131">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-132">**LabelFBInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="e167f-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="e167f-133">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-134">**LabelFBInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="e167f-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="e167f-135">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-136">**LabelFBInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="e167f-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="e167f-137">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.</span><span class="sxs-lookup"><span data-stu-id="e167f-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="e167f-138">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="e167f-138">**fbRed**</span></span>  
<span data-ttu-id="e167f-139">Fotogramas: valor del componente de color rojo de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-140">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="e167f-140">**fbGreen**</span></span>  
<span data-ttu-id="e167f-141">Fotogramas: valor del componente de color verde de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-142">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="e167f-142">**fbBlue**</span></span>  
<span data-ttu-id="e167f-143">Fotogramas: valor del componente de color azul de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-144">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="e167f-144">**fbAlpha**</span></span>  
<span data-ttu-id="e167f-145">Fotogramas: valor del componente de color alfa de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-146">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="e167f-146">**LabelFBRed**</span></span>  
<span data-ttu-id="e167f-147">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-148">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="e167f-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="e167f-149">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-150">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="e167f-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="e167f-151">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-152">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="e167f-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="e167f-153">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e167f-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="e167f-154">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="e167f-154">**pixelKillReason**</span></span>  
<span data-ttu-id="e167f-155">Especifica la razón por la que se ha eliminado la contribución de color del píxel.</span><span class="sxs-lookup"><span data-stu-id="e167f-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="e167f-156">**HResult**</span><span class="sxs-lookup"><span data-stu-id="e167f-156">**HResult**</span></span>  
<span data-ttu-id="e167f-157">Si se produjo un error, contiene el valor HRESULT de DirectX que especifica el error.</span><span class="sxs-lookup"><span data-stu-id="e167f-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e167f-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e167f-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e167f-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e167f-159">Header</span></span></p></td><td><span data-ttu-id="e167f-160">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e167f-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



