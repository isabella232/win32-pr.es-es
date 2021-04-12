---
description: Contiene la hora de inicio en la que un origen multimedia se reinicia desde su posición actual.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423824"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="00160-103">\_Atributo de \_ \_ Inicio real del origen de eventos MF \_</span><span class="sxs-lookup"><span data-stu-id="00160-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="00160-104">Contiene la hora de inicio en la que un origen multimedia se reinicia desde su posición actual.</span><span class="sxs-lookup"><span data-stu-id="00160-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="00160-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="00160-105">Data type</span></span>

<span data-ttu-id="00160-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="00160-106">**UINT64**</span></span>

<span data-ttu-id="00160-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="00160-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00160-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00160-108">Remarks</span></span>

<span data-ttu-id="00160-109">Este atributo se usa con el evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="00160-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="00160-110">El atributo es relevante cuando los datos de evento están vacíos (**VT \_ vacío**), lo que indica que el origen de medios se inició desde la posición de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="00160-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="00160-111">En ese caso, el atributo de **\_ \_ \_ \_ Inicio real del origen de eventos MF** especifica la hora de inicio real.</span><span class="sxs-lookup"><span data-stu-id="00160-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="00160-112">Si los datos de evento **están \_ vacíos en VT** y este atributo no está establecido, se supone que la hora de inicio es cero.</span><span class="sxs-lookup"><span data-stu-id="00160-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="00160-113">Cuando los datos del evento [MESourceStarted](mesourcestarted.md) contienen la hora de inicio (**VT \_ i8**), no se debe establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="00160-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="00160-114">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="00160-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="00160-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="00160-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00160-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00160-116">Requirements</span></span>



| <span data-ttu-id="00160-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00160-117">Requirement</span></span> | <span data-ttu-id="00160-118">Value</span><span class="sxs-lookup"><span data-stu-id="00160-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00160-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00160-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00160-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00160-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00160-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00160-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00160-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00160-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00160-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00160-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00160-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00160-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00160-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="00160-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00160-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00160-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00160-127">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="00160-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="00160-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="00160-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="00160-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="00160-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




