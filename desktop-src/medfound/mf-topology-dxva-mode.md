---
description: Especifica si el cargador de topología habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705559"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="908d5-103">\_ \_ Atributo de modo DXVA de topología MF \_</span><span class="sxs-lookup"><span data-stu-id="908d5-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="908d5-104">Especifica si el cargador de topología habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.</span><span class="sxs-lookup"><span data-stu-id="908d5-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="908d5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="908d5-105">Data type</span></span>

<span data-ttu-id="908d5-106">**[**MFTOPOLOGY \_ \_Modo DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="908d5-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="908d5-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="908d5-107">Get/set</span></span>

<span data-ttu-id="908d5-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="908d5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="908d5-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="908d5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="908d5-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="908d5-110">Applies to</span></span>

[<span data-ttu-id="908d5-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="908d5-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="908d5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="908d5-112">Remarks</span></span>

<span data-ttu-id="908d5-113">El valor de este atributo es una constante de enumeración del [**\_ \_ modo DXVA de MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="908d5-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="908d5-114">El valor predeterminado es **MFTOPOLOGY \_ DXVA \_ default**.</span><span class="sxs-lookup"><span data-stu-id="908d5-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="908d5-115">Este atributo controla qué MFTs reciben un puntero al administrador de dispositivos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="908d5-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="908d5-116">Para habilitar la aceleración de vídeo completa, establezca el valor en **MFTOPOLOGY \_ DXVA \_ Full**.</span><span class="sxs-lookup"><span data-stu-id="908d5-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="908d5-117">El valor **\_ \_ predeterminado de DXVA MFTOPOLOGY** se define para la compatibilidad con versiones anteriores; coincide con el comportamiento de todas las versiones anteriores de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="908d5-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="908d5-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="908d5-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="908d5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="908d5-119">Requirements</span></span>



| <span data-ttu-id="908d5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="908d5-120">Requirement</span></span> | <span data-ttu-id="908d5-121">Value</span><span class="sxs-lookup"><span data-stu-id="908d5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="908d5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="908d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="908d5-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="908d5-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="908d5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="908d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="908d5-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="908d5-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="908d5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="908d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="908d5-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="908d5-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908d5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="908d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908d5-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="908d5-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="908d5-130">Administrador de dispositivos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="908d5-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="908d5-131">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="908d5-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




