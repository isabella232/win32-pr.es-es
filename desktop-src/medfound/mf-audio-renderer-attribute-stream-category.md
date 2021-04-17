---
description: Especifica la categoría de secuencia de audio para el representador de audio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687219"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="e5d4f-103">\_Atributo de \_ categoría de \_ secuencia de atributo de representador de audio \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="e5d4f-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="e5d4f-104">Especifica la categoría de secuencia de audio para el [representador de audio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="e5d4f-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="e5d4f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e5d4f-105">Data type</span></span>

<span data-ttu-id="e5d4f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5d4f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d4f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5d4f-107">Remarks</span></span>

<span data-ttu-id="e5d4f-108">Puede usar este atributo para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="e5d4f-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="e5d4f-109">El uso depende de la función a la que llame para crear el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="e5d4f-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="e5d4f-110">Función</span><span class="sxs-lookup"><span data-stu-id="e5d4f-110">Function</span></span>                                                               | <span data-ttu-id="e5d4f-111">Cómo establecer el atributo</span><span class="sxs-lookup"><span data-stu-id="e5d4f-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5d4f-112">**MFCreateAudioRenderer**</span><span class="sxs-lookup"><span data-stu-id="e5d4f-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="e5d4f-113">Use el puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="e5d4f-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="e5d4f-114">**MFCreateAudioRendererActivate**</span><span class="sxs-lookup"><span data-stu-id="e5d4f-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="e5d4f-115">Use el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="e5d4f-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="e5d4f-116">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="e5d4f-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="e5d4f-117">El valor del atributo es un miembro de la enumeración de la [**\_ \_ categoría secuencia de audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .</span><span class="sxs-lookup"><span data-stu-id="e5d4f-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="e5d4f-118">El servicio de audio usa la categoría Stream para determinar las directivas de audio cuando varias aplicaciones reproducen audio al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e5d4f-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d4f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d4f-119">Requirements</span></span>



| <span data-ttu-id="e5d4f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d4f-120">Requirement</span></span> | <span data-ttu-id="e5d4f-121">Value</span><span class="sxs-lookup"><span data-stu-id="e5d4f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d4f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d4f-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5d4f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e5d4f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d4f-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5d4f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e5d4f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5d4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d4f-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d4f-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d4f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5d4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d4f-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5d4f-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
