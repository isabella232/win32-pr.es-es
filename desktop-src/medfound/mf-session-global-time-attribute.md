---
description: Especifica si las topologías tienen una hora de inicio y de finalización global.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: MF_SESSION_GLOBAL_TIME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716417"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="36bc9-103">\_Atributo de \_ hora global de sesión MF \_</span><span class="sxs-lookup"><span data-stu-id="36bc9-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="36bc9-104">Especifica si las topologías tienen una hora de inicio y de finalización global.</span><span class="sxs-lookup"><span data-stu-id="36bc9-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="36bc9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="36bc9-105">Data type</span></span>

<span data-ttu-id="36bc9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="36bc9-106">**UINT32**</span></span>

<span data-ttu-id="36bc9-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="36bc9-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36bc9-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36bc9-108">Remarks</span></span>

<span data-ttu-id="36bc9-109">Puede establecer este atributo al crear el sesison de medios mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="36bc9-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="36bc9-110">Si este atributo está presente y es distinto de cero, todas las topologías que se pasan a la sesión multimedia deben tener los atributos [**de \_ \_ PROJECTSTOP de topología**](mf-topology-projectstop-attribute.md) [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) y MF.</span><span class="sxs-lookup"><span data-stu-id="36bc9-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="36bc9-111">Estos atributos especifican las horas de inicio y detención de la topología en relación con toda la presentación.</span><span class="sxs-lookup"><span data-stu-id="36bc9-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="36bc9-112">Si este atributo no está presente o **false**, las topologías no deben tener el atributo [**MF Topology \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) o [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="36bc9-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="36bc9-113">Use este atributo para crear secuencias de edición.</span><span class="sxs-lookup"><span data-stu-id="36bc9-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="36bc9-114">Para obtener más información, vea [tiempos de presentación de secuencias](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="36bc9-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="36bc9-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="36bc9-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36bc9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36bc9-116">Requirements</span></span>



| <span data-ttu-id="36bc9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36bc9-117">Requirement</span></span> | <span data-ttu-id="36bc9-118">Value</span><span class="sxs-lookup"><span data-stu-id="36bc9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36bc9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36bc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36bc9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="36bc9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36bc9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36bc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36bc9-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="36bc9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36bc9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36bc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36bc9-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36bc9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36bc9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="36bc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bc9-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36bc9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36bc9-127">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="36bc9-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="36bc9-128">Tiempos de presentación de secuencia</span><span class="sxs-lookup"><span data-stu-id="36bc9-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="36bc9-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="36bc9-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="36bc9-130">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="36bc9-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="36bc9-131">**\_PROJECTSTART de topología \_ MF**</span><span class="sxs-lookup"><span data-stu-id="36bc9-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="36bc9-132">**\_PROJECTSTOP de topología \_ MF**</span><span class="sxs-lookup"><span data-stu-id="36bc9-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




