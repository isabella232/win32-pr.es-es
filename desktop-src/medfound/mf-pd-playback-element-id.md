---
description: Contiene el identificador del elemento de lista de reproducción en la presentación.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659981"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="64422-103">\_Atributo de \_ \_ \_ ID. de elemento de reproducción MF PD</span><span class="sxs-lookup"><span data-stu-id="64422-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="64422-104">Contiene el identificador del elemento de lista de reproducción en la presentación.</span><span class="sxs-lookup"><span data-stu-id="64422-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="64422-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="64422-105">Data type</span></span>

<span data-ttu-id="64422-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="64422-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="64422-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="64422-107">Get/set</span></span>

<span data-ttu-id="64422-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="64422-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="64422-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="64422-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="64422-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="64422-110">Applies to</span></span>

[<span data-ttu-id="64422-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="64422-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="64422-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64422-112">Remarks</span></span>

<span data-ttu-id="64422-113">Los orígenes multimedia que ofrecen listas de reproducción pueden establecer opcionalmente este atributo en los descriptores de presentación.</span><span class="sxs-lookup"><span data-stu-id="64422-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="64422-114">Cuando un origen multimedia entrega una lista de reproducción, envía un evento [MENewPresentation](menewpresentation.md) para cada elemento de lista de reproducción después de la primera.</span><span class="sxs-lookup"><span data-stu-id="64422-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="64422-115">Este evento contiene un descriptor de presentación para el nuevo elemento de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="64422-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="64422-116">El origen multimedia puede asignar identificadores a los elementos mediante el establecimiento del \_ \_ \_ atributo ID del elemento de reproducción MF PD \_ en cada descriptor de presentación, incluido el creado por [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="64422-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="64422-117">Un origen multimedia también puede enviar el evento [MENewPresentation](menewpresentation.md) debido a un cambio de flujo dinámico o un cambio en el número de secuencias.</span><span class="sxs-lookup"><span data-stu-id="64422-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="64422-118">En esa situación, el valor del \_ identificador de elemento de reproducción MF PD \_ \_ \_ debe permanecer igual en ambas presentaciones para indicar que ambas presentaciones representan el mismo elemento de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="64422-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="64422-119">Si dos presentaciones consecutivas tienen el mismo valor para este atributo, la canalización Microsoft Media Foundation espera que las marcas de tiempo sigan siendo continuas en la transición.</span><span class="sxs-lookup"><span data-stu-id="64422-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="64422-120">Por lo tanto, el origen multimedia no debe usar el atributo de [ \_ \_ \_ \_ Inicio real del origen de eventos MF](mf-event-source-actual-start-attribute.md) cuando realiza la transición a la siguiente presentación.</span><span class="sxs-lookup"><span data-stu-id="64422-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="64422-121">Los orígenes de medios que implementan [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar el atributo de la [secuencia de MF \_ \_ \_ TOPONODE](mf-toponode-sequence-elementid-attribute.md) en lugar del \_ atributo de identificador de elemento de reproducción MF PD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="64422-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="64422-122">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="64422-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="64422-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64422-123">Requirements</span></span>



| <span data-ttu-id="64422-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64422-124">Requirement</span></span> | <span data-ttu-id="64422-125">Value</span><span class="sxs-lookup"><span data-stu-id="64422-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64422-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64422-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64422-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="64422-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="64422-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64422-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64422-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="64422-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="64422-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64422-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64422-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64422-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64422-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="64422-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64422-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64422-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="64422-134">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="64422-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




