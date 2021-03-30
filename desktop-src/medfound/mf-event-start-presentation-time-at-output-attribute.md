---
description: El momento de la presentación en el que los receptores de medios van a representar el primer ejemplo de la nueva topología.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910806"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="b058b-103">\_ \_ \_ \_ Tiempo de presentación de inicio \_ de evento MF en el \_ atributo de salida</span><span class="sxs-lookup"><span data-stu-id="b058b-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="b058b-104">El momento de la presentación en el que los receptores de medios van a representar el primer ejemplo de la nueva topología.</span><span class="sxs-lookup"><span data-stu-id="b058b-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="b058b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b058b-105">Data type</span></span>

<span data-ttu-id="b058b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b058b-106">**UINT64**</span></span>

<span data-ttu-id="b058b-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="b058b-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b058b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b058b-108">Remarks</span></span>

<span data-ttu-id="b058b-109">Si algún objeto de canalización de la topología anterior almacenaba en búfer los datos, este valor será ligeramente menor que el valor del atributo de [**desplazamiento de tiempo de \_ presentación de eventos \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , ya que los receptores deben representar los datos almacenados en búfer.</span><span class="sxs-lookup"><span data-stu-id="b058b-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="b058b-110">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="b058b-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="b058b-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b058b-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b058b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b058b-112">Requirements</span></span>



| <span data-ttu-id="b058b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b058b-113">Requirement</span></span> | <span data-ttu-id="b058b-114">Value</span><span class="sxs-lookup"><span data-stu-id="b058b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b058b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b058b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b058b-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b058b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b058b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b058b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b058b-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b058b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b058b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b058b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b058b-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b058b-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b058b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b058b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b058b-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b058b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b058b-123">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="b058b-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="b058b-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b058b-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="b058b-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b058b-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




