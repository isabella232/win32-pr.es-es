---
description: Una superficie representa un área lineal de la memoria de la pantalla y suele residir en la memoria de visualización de la tarjeta de pantalla, aunque pueden existir superficies en la memoria del sistema. La interfaz IDirect3DSurface9 administra las superficies.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superficies de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805198"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="b4b3f-104">Superficies de Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="b4b3f-105">Una superficie representa un área lineal de la memoria de la pantalla y suele residir en la memoria de visualización de la tarjeta de pantalla, aunque pueden existir superficies en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="b4b3f-106">La interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) administra las superficies.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="b4b3f-107">Búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-107">Front Buffer.</span></span> <span data-ttu-id="b4b3f-108">Un rectángulo de memoria que el adaptador de gráficos traduce y que se muestra en el monitor.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="b4b3f-109">En Direct3D, una aplicación nunca escribe directamente en el búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="b4b3f-110">Búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-110">Back Buffer.</span></span> <span data-ttu-id="b4b3f-111">Un rectángulo de memoria en el que puede escribir una aplicación directamente.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="b4b3f-112">El búfer de reserva nunca se muestra directamente en el monitor.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="b4b3f-113">Voltear superficies.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-113">Flipping surfaces.</span></span> <span data-ttu-id="b4b3f-114">Proceso de mover el búfer de reserva al búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="b4b3f-115">Cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-115">Swap chain.</span></span> <span data-ttu-id="b4b3f-116">Colección de uno o más búferes de reserva que se pueden presentar en serie al búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="b4b3f-117">Obtención de una superficie</span><span class="sxs-lookup"><span data-stu-id="b4b3f-117">Getting a Surface</span></span>

<span data-ttu-id="b4b3f-118">Cree una superficie llamando a cualquiera de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="b4b3f-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="b4b3f-119">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="b4b3f-120">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="b4b3f-121">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="b4b3f-122">Los formatos de superficie determinan cómo se interpretan los datos de cada píxel en la memoria de la superficie.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="b4b3f-123">Direct3D usa el miembro [D3DFORMAT](d3dformat.md) de la [**estructura \_ DESC de D3DSURFACE**](d3dsurface-desc.md) para describir el formato de la superficie.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="b4b3f-124">Puede recuperar el formato de una superficie existente llamando al método [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="b4b3f-125">Una vez creada una superficie, puede obtener un puntero llamando a cualquiera de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="b4b3f-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="b4b3f-126">**GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="b4b3f-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="b4b3f-128">**GetDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="b4b3f-129">**GetFrontBufferData**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="b4b3f-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="b4b3f-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="b4b3f-132">**GetSurfaceLevel**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="b4b3f-133">La interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) permite el acceso indirecto a la memoria a través del método [**UpdateSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b4b3f-134">Este método permite copiar una región rectangular de píxeles de una interfaz **IDirect3DSurface9** a otra interfaz **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="b4b3f-135">La interfaz Surface también tiene métodos para acceder directamente a la memoria de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="b4b3f-136">Por ejemplo, puede usar el método [**LockRect**](/windows/desktop/api) para bloquear una región rectangular de la memoria de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="b4b3f-137">Es importante llamar a [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) después de haber terminado de trabajar con la región rectangular bloqueada en la superficie.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="b4b3f-138">Temas de superficie adicionales</span><span class="sxs-lookup"><span data-stu-id="b4b3f-138">Additional Surface Topics</span></span>

<span data-ttu-id="b4b3f-139">Obtenga más información sobre cómo usar las superficies con cualquiera de estos temas:</span><span class="sxs-lookup"><span data-stu-id="b4b3f-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="b4b3f-140">Formatos de superficie (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="b4b3f-141">¿Qué es una cadena de intercambio? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="b4b3f-142">Ancho frente a paso (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="b4b3f-143">Voltear superficies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="b4b3f-144">Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="b4b3f-145">Copiar en superficies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="b4b3f-146">Copiar superficies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="b4b3f-147">Acceso directo a la memoria de la superficie (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="b4b3f-148">Datos de la superficie privada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="b4b3f-149">Controles gamma (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4b3f-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="b4b3f-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4b3f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4b3f-151">Introducción</span><span class="sxs-lookup"><span data-stu-id="b4b3f-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
