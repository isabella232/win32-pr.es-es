---
description: Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696638"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="31d8d-103">\_ \_ Hora de inicio de la topología MF \_ \_ en el \_ \_ atributo switch de presentación</span><span class="sxs-lookup"><span data-stu-id="31d8d-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="31d8d-104">Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.</span><span class="sxs-lookup"><span data-stu-id="31d8d-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="31d8d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31d8d-105">Data type</span></span>

<span data-ttu-id="31d8d-106">**INT64** almacenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="31d8d-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="31d8d-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="31d8d-107">Get/set</span></span>

<span data-ttu-id="31d8d-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="31d8d-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="31d8d-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="31d8d-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="31d8d-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="31d8d-110">Applies To</span></span>

[<span data-ttu-id="31d8d-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="31d8d-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="31d8d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31d8d-112">Remarks</span></span>

<span data-ttu-id="31d8d-113">Cuando la aplicación pone en cola la primera presentación en la sesión multimedia, la aplicación especifica la hora de inicio en el parámetro *pvarStartPosition* del método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) .</span><span class="sxs-lookup"><span data-stu-id="31d8d-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="31d8d-114">En el caso de las presentaciones posteriores, sin embargo, la hora de inicio la proporciona la hora de inicio \_ de la topología MF \_ \_ \_ en \_ \_ el atributo switch de la presentación en la topología.</span><span class="sxs-lookup"><span data-stu-id="31d8d-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="31d8d-115">La hora de inicio se especifica en unidades de 100-nanosegundos, con respecto al principio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="31d8d-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="31d8d-116">Por ejemplo, si el valor es 50 millones, la reproducción empieza 5 segundos en la presentación.</span><span class="sxs-lookup"><span data-stu-id="31d8d-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="31d8d-117">Si no se establece este atributo, la hora de inicio predeterminada es cero.</span><span class="sxs-lookup"><span data-stu-id="31d8d-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="31d8d-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="31d8d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d8d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31d8d-119">Requirements</span></span>



| <span data-ttu-id="31d8d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d8d-120">Requirement</span></span> | <span data-ttu-id="31d8d-121">Value</span><span class="sxs-lookup"><span data-stu-id="31d8d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31d8d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31d8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31d8d-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="31d8d-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31d8d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31d8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31d8d-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31d8d-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="31d8d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31d8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d8d-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d8d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d8d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="31d8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d8d-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31d8d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31d8d-130">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="31d8d-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




