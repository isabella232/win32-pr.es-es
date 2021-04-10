---
description: Habilita la descodificación acelerada por hardware desde un dispositivo de Direct3D 9 mediante la aceleración de vídeo de DirectX (DXVA) versión 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interfaz IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155185"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="2f6dd-103">Interfaz IDirect3DVideoDevice9</span><span class="sxs-lookup"><span data-stu-id="2f6dd-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="2f6dd-104">Habilita la descodificación acelerada por hardware desde un dispositivo de Direct3D 9 mediante la aceleración de vídeo de DirectX (DXVA) versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2f6dd-105">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="2f6dd-105">When to use</span></span>

<span data-ttu-id="2f6dd-106">Esta interfaz no está pensada para el uso general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="2f6dd-107">Los filtros del descodificador de DirectShow deben usar la interfaz [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , no **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="2f6dd-108">Los pin de entrada del filtro de representador de mezcla de vídeo (VMR) y el filtro de mezclador de superposición exponen **IAMVideoAccelerator**.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="2f6dd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f6dd-109">Members</span></span>

<span data-ttu-id="2f6dd-110">La interfaz **IDirect3DVideoDevice9** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f6dd-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f6dd-111">**IDirect3DVideoDevice9** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2f6dd-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="2f6dd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f6dd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f6dd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f6dd-113">Methods</span></span>

<span data-ttu-id="2f6dd-114">La interfaz **IDirect3DVideoDevice9** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="2f6dd-115">Método</span><span class="sxs-lookup"><span data-stu-id="2f6dd-115">Method</span></span>                                                                                   | <span data-ttu-id="2f6dd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f6dd-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f6dd-117">**CreateDXVADevice**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="2f6dd-118">Crea un dispositivo descodificador de DXVA.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2f6dd-119">**CreateSurface**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="2f6dd-120">Crea una superficie comprimida para la descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="2f6dd-121">**GetDXVACompressedBufferInfo**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="2f6dd-122">Obtiene información acerca de los búferes comprimidos necesarios para la descodificación acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="2f6dd-123">**GetDXVAGuids**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="2f6dd-124">Obtiene una lista de los perfiles de DXVA admitidos por el controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="2f6dd-125">**GetDXVAInternalInfo**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="2f6dd-126">Consulta la cantidad de memoria temporal que la capa de abstracción de hardware (HAL) asignará para su uso privado.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="2f6dd-127">**GetUncompressedDXVAFormats**</span><span class="sxs-lookup"><span data-stu-id="2f6dd-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="2f6dd-128">Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar con un perfil de DXVA especificado.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2f6dd-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f6dd-129">Remarks</span></span>

<span data-ttu-id="2f6dd-130">Para obtener un puntero a esta interfaz, llame a **QueryInterface** en un puntero [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .</span><span class="sxs-lookup"><span data-stu-id="2f6dd-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="2f6dd-131">Esta interfaz solo admite DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="2f6dd-132">No admite DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f6dd-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6dd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f6dd-133">Requirements</span></span>



| <span data-ttu-id="2f6dd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f6dd-134">Requirement</span></span> | <span data-ttu-id="2f6dd-135">Value</span><span class="sxs-lookup"><span data-stu-id="2f6dd-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2f6dd-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f6dd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6dd-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2f6dd-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f6dd-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f6dd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6dd-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f6dd-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f6dd-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f6dd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f6dd-141"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6dd-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6dd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f6dd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6dd-143">Interfaces de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f6dd-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2f6dd-144">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="2f6dd-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="2f6dd-145">Especificación de DXVA 1,0</span><span class="sxs-lookup"><span data-stu-id="2f6dd-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
