---
description: Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423800"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="4587d-103">\_ \_ Atributo Delta SESSIONCAPS de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="4587d-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="4587d-104">Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="4587d-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="4587d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4587d-105">Data type</span></span>

<span data-ttu-id="4587d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4587d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4587d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4587d-107">Remarks</span></span>

<span data-ttu-id="4587d-108">Este atributo contiene una máscara de máscara que indica qué marcas de capacidades han cambiado.</span><span class="sxs-lookup"><span data-stu-id="4587d-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="4587d-109">Para obtener una lista de posibles marcas, vea [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="4587d-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="4587d-110">Los bits se establecen en 1 en la máscara de bits por cualquiera de los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="4587d-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="4587d-111">El bit de funcionalidad correspondiente cambió de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="4587d-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="4587d-112">El bit de funcionalidad correspondiente cambió de 1 a 0.</span><span class="sxs-lookup"><span data-stu-id="4587d-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="4587d-113">El bit de funcionalidad correspondiente seguía siendo 1, pero los detalles de la funcionalidad cambiaron.</span><span class="sxs-lookup"><span data-stu-id="4587d-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="4587d-114">Por ejemplo, la velocidad de reproducción máxima ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4587d-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="4587d-115">Este atributo se usa con el evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4587d-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="4587d-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4587d-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4587d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4587d-117">Requirements</span></span>



| <span data-ttu-id="4587d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4587d-118">Requirement</span></span> | <span data-ttu-id="4587d-119">Value</span><span class="sxs-lookup"><span data-stu-id="4587d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4587d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4587d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4587d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4587d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4587d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4587d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4587d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4587d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4587d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4587d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4587d-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4587d-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4587d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4587d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4587d-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4587d-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4587d-128">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="4587d-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4587d-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4587d-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4587d-130">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4587d-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




