---
description: Especifica si el cargador de topología habilita el procesador de vídeo de transcodificación (XVP). en el caso de las conversiones, habilitar la conversión de color acelerado de hardware.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK atributo (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105721409"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="7f3da-104">\_Topología MF \_ habilitar \_ XVP para el \_ atributo de \_ reproducción</span><span class="sxs-lookup"><span data-stu-id="7f3da-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="7f3da-105">Especifica si el cargador de topología habilita el procesador de vídeo de transcodificación (XVP).</span><span class="sxs-lookup"><span data-stu-id="7f3da-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="7f3da-106">en el caso de las conversiones, habilitar la conversión de color acelerado de hardware.</span><span class="sxs-lookup"><span data-stu-id="7f3da-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f3da-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7f3da-107">Data type</span></span>

<span data-ttu-id="7f3da-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f3da-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7f3da-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="7f3da-109">Get/set</span></span>

<span data-ttu-id="7f3da-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7f3da-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7f3da-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7f3da-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7f3da-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="7f3da-112">Applies to</span></span>

[<span data-ttu-id="7f3da-113">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="7f3da-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="7f3da-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f3da-114">Remarks</span></span>

<span data-ttu-id="7f3da-115">Si se establece este atributo, el cargador de topología incorporará el procesador de vídeo, si es necesario, durante la resolución de topología no transcodificada.</span><span class="sxs-lookup"><span data-stu-id="7f3da-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="7f3da-116">Cuando se usa la topología para compilar su propio [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , este atributo indica al cargador que use XVP para las conversiones en lugar del convertidor de color heredado, lo que permite la conversión de color acelerado de hardware. el convertidor de colores heredado es solo software.</span><span class="sxs-lookup"><span data-stu-id="7f3da-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3da-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f3da-117">Requirements</span></span>



| <span data-ttu-id="7f3da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3da-118">Requirement</span></span> | <span data-ttu-id="7f3da-119">Value</span><span class="sxs-lookup"><span data-stu-id="7f3da-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3da-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3da-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3da-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f3da-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3da-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3da-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7f3da-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f3da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3da-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f3da-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3da-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f3da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3da-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f3da-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f3da-128">Administrador de dispositivos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7f3da-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="7f3da-129">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="7f3da-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




