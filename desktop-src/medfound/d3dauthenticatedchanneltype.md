---
description: Especifica el tipo de canal de Direct3D autenticado.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Enumeración D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659782"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="c691f-103">Enumeración D3DAUTHENTICATEDCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="c691f-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="c691f-104">Especifica el tipo de canal de Direct3D autenticado.</span><span class="sxs-lookup"><span data-stu-id="c691f-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="c691f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c691f-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="c691f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c691f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c691f-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="c691f-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="c691f-108">Canal de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c691f-108">Direct3D 9 channel.</span></span> <span data-ttu-id="c691f-109">Este canal proporciona comunicación con el tiempo de ejecución de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c691f-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="c691f-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="c691f-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="c691f-111">Canal del controlador de software.</span><span class="sxs-lookup"><span data-stu-id="c691f-111">Software driver channel.</span></span> <span data-ttu-id="c691f-112">Este canal proporciona comunicación con un controlador que implementa mecanismos de protección de contenido en el software.</span><span class="sxs-lookup"><span data-stu-id="c691f-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="c691f-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="c691f-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="c691f-114">Canal del controlador de hardware.</span><span class="sxs-lookup"><span data-stu-id="c691f-114">Hardware driver channel.</span></span> <span data-ttu-id="c691f-115">Este canal proporciona comunicación con un controlador que implementa mecanismos de protección de contenido en el hardware de la GPU.</span><span class="sxs-lookup"><span data-stu-id="c691f-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c691f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c691f-116">Requirements</span></span>



| <span data-ttu-id="c691f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c691f-117">Requirement</span></span> | <span data-ttu-id="c691f-118">Value</span><span class="sxs-lookup"><span data-stu-id="c691f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c691f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c691f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c691f-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c691f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c691f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c691f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c691f-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c691f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c691f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c691f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c691f-124"><dt>D3d9types. h (incluye d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c691f-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c691f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c691f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c691f-126">Enumeraciones de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c691f-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="c691f-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="c691f-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




