---
description: Almacena el tiempo (en unidades 100-nanosegundos) en el que debe comenzar la presentación, en relación con el inicio del origen del medio.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: MF_PD_PLAYBACK_BOUNDARY_TIME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083370"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="d1a7e-103">\_Atributo de \_ tiempo de límite de reproducción MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1a7e-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="d1a7e-104">Almacena el tiempo (en unidades 100-nanosegundos) en el que debe comenzar la presentación, en relación con el inicio del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1a7e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d1a7e-105">Data type</span></span>

<span data-ttu-id="d1a7e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d1a7e-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="d1a7e-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="d1a7e-107">Get/set</span></span>

<span data-ttu-id="d1a7e-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="d1a7e-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="d1a7e-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="d1a7e-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d1a7e-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d1a7e-110">Applies to</span></span>

[<span data-ttu-id="d1a7e-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d1a7e-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="d1a7e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1a7e-112">Remarks</span></span>

<span data-ttu-id="d1a7e-113">El \_ atributo de tiempo de límite de reproducción MF PD \_ \_ \_ es opcional para los orígenes multimedia de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="d1a7e-114">Este valor indica la hora de inicio real de la presentación.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="d1a7e-115">Considere una lista de reproducción que incluye los orígenes de medios *Element1*, *elemento2* y *Element3* en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="d1a7e-116">15 segundos después de que se reproduzca *elemento1* , se produce un cambio de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="d1a7e-117">La nueva secuencia debe empezar a reproducir 15 segundos en la presentación.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="d1a7e-118">Sin embargo, el fotograma clave más cercano al tiempo de presentación de 15 segundos es de 12 segundos para la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="d1a7e-119">Para iniciar la nueva presentación en 15 segundos, se requiere un signo para que las muestras descodificadas se quiten de 12 segundos a 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="d1a7e-120">Antes de la transición, el origen del medio genera el evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a7e-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="d1a7e-121">Esto devuelve el descriptor de presentación que contiene el atributo de ID. de [ \_ elemento de \_ reproducción \_ \_ MF PD](mf-pd-playback-element-id.md) para Element1.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="d1a7e-122">Además, contiene el atributo de \_ tiempo de límite de reproducción MF PD \_ \_ \_ que se establece en 15 segundos para indicar el momento en que se produjo la transición.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="d1a7e-123">El origen multimedia realiza el marcado en 15 segundos después de la descodificación, lo que evita que se muestren los fotogramas de 12 segundos a 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="d1a7e-124">Este valor solo afecta a Marking Time y no afecta al modo en que la sesión multimedia ajusta las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="d1a7e-125">Este atributo se omite a menos que el origen de medios indique a través del atributo de [ \_ \_ \_ \_ ID. de elemento de reproducción MF PD](mf-pd-playback-element-id.md) que esta presentación es el mismo elemento de reproducción que el anterior.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="d1a7e-126">El \_ atributo de tiempo de límite de reproducción MF PD \_ \_ \_ es similar al atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) que se establece en el nodo de la topología.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="d1a7e-127">En el caso de las aplicaciones que se ejecutan en Windows Vista, los orígenes multimedia que implementan [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar **MF \_ TOPONODE \_ MEDIASTART** en lugar del tiempo de límite de reproducción de MF \_ PD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d1a7e-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="d1a7e-128">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d1a7e-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a7e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a7e-129">Requirements</span></span>



| <span data-ttu-id="d1a7e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a7e-130">Requirement</span></span> | <span data-ttu-id="d1a7e-131">Value</span><span class="sxs-lookup"><span data-stu-id="d1a7e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a7e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1a7e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a7e-133">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a7e-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d1a7e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1a7e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a7e-135">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a7e-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d1a7e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1a7e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a7e-137"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a7e-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a7e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1a7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a7e-139">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1a7e-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1a7e-140">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="d1a7e-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




