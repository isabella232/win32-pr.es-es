---
description: Especifica la clase de directiva de audio para el representador de audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911425"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="69c4f-103">\_Atributo de \_ \_ \_ ID. de sesión de atributo de representador MF audio \_</span><span class="sxs-lookup"><span data-stu-id="69c4f-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="69c4f-104">Especifica la clase de directiva de audio para el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="69c4f-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="69c4f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69c4f-105">Data type</span></span>

<span data-ttu-id="69c4f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="69c4f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="69c4f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69c4f-107">Remarks</span></span>

<span data-ttu-id="69c4f-108">Este atributo asocia el procesador de audio a una clase de directiva de audio.</span><span class="sxs-lookup"><span data-stu-id="69c4f-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="69c4f-109">Cada clase de directiva tiene su propio control de volumen y Directiva.</span><span class="sxs-lookup"><span data-stu-id="69c4f-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="69c4f-110">Si no se establece este atributo, el nuevo SAR se une a la sesión de audio predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69c4f-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="69c4f-111">Para obtener más información, consulte [**IAudioClient:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) en la documentación básica de la API de audio.</span><span class="sxs-lookup"><span data-stu-id="69c4f-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="69c4f-112">Puede usar este atributo para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="69c4f-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="69c4f-113">El uso depende de la función a la que llame para crear el representador de audio:</span><span class="sxs-lookup"><span data-stu-id="69c4f-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="69c4f-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="69c4f-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="69c4f-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="69c4f-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="69c4f-116">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="69c4f-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="69c4f-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69c4f-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c4f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c4f-118">Requirements</span></span>



| <span data-ttu-id="69c4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c4f-119">Requirement</span></span> | <span data-ttu-id="69c4f-120">Value</span><span class="sxs-lookup"><span data-stu-id="69c4f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69c4f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69c4f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69c4f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="69c4f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="69c4f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69c4f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69c4f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="69c4f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69c4f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69c4f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c4f-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c4f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c4f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="69c4f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c4f-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69c4f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69c4f-129">Atributos del representador de audio</span><span class="sxs-lookup"><span data-stu-id="69c4f-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="69c4f-130">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="69c4f-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="69c4f-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="69c4f-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="69c4f-132">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="69c4f-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
