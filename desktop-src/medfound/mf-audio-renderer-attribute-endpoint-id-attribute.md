---
description: Especifica el identificador del dispositivo de extremo de audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360518"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="63e18-103">Atributo \_ de \_ \_ \_ ID. de extremo de atributo de representador de audio MF \_</span><span class="sxs-lookup"><span data-stu-id="63e18-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="63e18-104">Especifica el identificador del dispositivo de extremo de audio.</span><span class="sxs-lookup"><span data-stu-id="63e18-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="63e18-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63e18-105">Data type</span></span>

<span data-ttu-id="63e18-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="63e18-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="63e18-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63e18-107">Remarks</span></span>

<span data-ttu-id="63e18-108">Puede usar este atributo para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="63e18-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="63e18-109">El uso depende de la función a la que llame para crear el representador de audio:</span><span class="sxs-lookup"><span data-stu-id="63e18-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="63e18-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="63e18-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="63e18-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="63e18-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="63e18-112">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="63e18-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="63e18-113">Un dispositivo de punto de conexión de audio es un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso a datos de audio, como un auricular o un altavoz.</span><span class="sxs-lookup"><span data-stu-id="63e18-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="63e18-114">Para obtener el identificador del punto de conexión de audio, use las siguientes API de audio principales:</span><span class="sxs-lookup"><span data-stu-id="63e18-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="63e18-115">Use la interfaz [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) para enumerar los dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="63e18-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="63e18-116">Llame a [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63e18-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="63e18-117">Para obtener más información, consulte la documentación básica de la API de [audio](../coreaudio/core-audio-apis-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="63e18-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="63e18-118">Si no se establece este atributo, el representador de audio utiliza el dispositivo de extremo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="63e18-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="63e18-119">Si se establece este atributo, no establezca el atributo [**de \_ rol de \_ punto \_ de \_ conexión \_ de atributo de representador de audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="63e18-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="63e18-120">Si se establecen ambos atributos, se producirá un error cuando se cree el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="63e18-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="63e18-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="63e18-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e18-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e18-122">Requirements</span></span>



| <span data-ttu-id="63e18-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e18-123">Requirement</span></span> | <span data-ttu-id="63e18-124">Value</span><span class="sxs-lookup"><span data-stu-id="63e18-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63e18-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e18-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63e18-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63e18-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63e18-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e18-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63e18-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63e18-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63e18-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63e18-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e18-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e18-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e18-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e18-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e18-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63e18-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63e18-133">Atributos del representador de audio</span><span class="sxs-lookup"><span data-stu-id="63e18-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="63e18-134">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="63e18-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="63e18-135">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="63e18-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="63e18-136">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="63e18-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
