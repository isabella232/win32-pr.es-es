---
description: Representa un acelerador de hardware para DirectX video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interfaz IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715885"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="668bd-103">Interfaz IDirect3DDXVADevice9</span><span class="sxs-lookup"><span data-stu-id="668bd-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="668bd-104">Representa un acelerador de hardware para DirectX video Acceleration (DXVA) 1,0.</span><span class="sxs-lookup"><span data-stu-id="668bd-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="668bd-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="668bd-105">Members</span></span>

<span data-ttu-id="668bd-106">La interfaz **IDirect3DDXVADevice9** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="668bd-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="668bd-107">**IDirect3DDXVADevice9** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="668bd-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="668bd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="668bd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="668bd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="668bd-109">Methods</span></span>

<span data-ttu-id="668bd-110">La interfaz **IDirect3DDXVADevice9** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="668bd-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="668bd-111">Método</span><span class="sxs-lookup"><span data-stu-id="668bd-111">Method</span></span>                                                  | <span data-ttu-id="668bd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="668bd-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="668bd-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="668bd-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="668bd-114">Comienza el procesamiento para crear una imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="668bd-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="668bd-115">**EndFrame**</span><span class="sxs-lookup"><span data-stu-id="668bd-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="668bd-116">Finaliza el procesamiento para crear una imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="668bd-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="668bd-117">**Ejecut**</span><span class="sxs-lookup"><span data-stu-id="668bd-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="668bd-118">Realiza una operación de descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="668bd-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="668bd-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="668bd-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="668bd-120">Consulta el estado de lectura y escritura de una superficie de descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="668bd-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="668bd-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="668bd-121">Remarks</span></span>

<span data-ttu-id="668bd-122">Para obtener un puntero a esta interfaz, llame a [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="668bd-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="668bd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="668bd-123">Requirements</span></span>



| <span data-ttu-id="668bd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="668bd-124">Requirement</span></span> | <span data-ttu-id="668bd-125">Value</span><span class="sxs-lookup"><span data-stu-id="668bd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="668bd-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="668bd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="668bd-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="668bd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="668bd-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="668bd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="668bd-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="668bd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="668bd-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="668bd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="668bd-131"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="668bd-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="668bd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="668bd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668bd-133">Interfaces de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="668bd-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
