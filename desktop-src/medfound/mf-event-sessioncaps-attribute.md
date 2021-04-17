---
description: Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: MF_EVENT_SESSIONCAPS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659855"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="e109d-103">\_Atributo SESSIONCAPS de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="e109d-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="e109d-104">Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="e109d-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="e109d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e109d-105">Data type</span></span>

<span data-ttu-id="e109d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e109d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e109d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e109d-107">Remarks</span></span>

<span data-ttu-id="e109d-108">Este atributo contiene un or **bit a** bit de cero o más marcadores.</span><span class="sxs-lookup"><span data-stu-id="e109d-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="e109d-109">Para obtener una lista de posibles marcas, vea [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="e109d-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="e109d-110">Este atributo se usa con el evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e109d-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="e109d-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e109d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e109d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e109d-112">Requirements</span></span>



| <span data-ttu-id="e109d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e109d-113">Requirement</span></span> | <span data-ttu-id="e109d-114">Value</span><span class="sxs-lookup"><span data-stu-id="e109d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e109d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e109d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e109d-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e109d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e109d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e109d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e109d-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e109d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e109d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e109d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e109d-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e109d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e109d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e109d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e109d-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e109d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e109d-123">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="e109d-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="e109d-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e109d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e109d-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e109d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




