---
description: Especifica el rol de punto de conexión de audio para el representador de audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002308"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="b2af6-103">Atributo \_ de \_ rol de \_ \_ punto de conexión de atributo de representador de audio MF \_</span><span class="sxs-lookup"><span data-stu-id="b2af6-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="b2af6-104">Especifica el rol de punto de conexión de audio para el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="b2af6-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2af6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b2af6-105">Data type</span></span>

<span data-ttu-id="b2af6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2af6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b2af6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2af6-107">Remarks</span></span>

<span data-ttu-id="b2af6-108">Puede usar este atributo para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="b2af6-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="b2af6-109">El uso depende de la función a la que llame para crear el representador de audio:</span><span class="sxs-lookup"><span data-stu-id="b2af6-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="b2af6-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b2af6-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="b2af6-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="b2af6-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="b2af6-112">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="b2af6-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b2af6-113">Un dispositivo de punto de conexión de audio es un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso a datos de audio, como un auricular o un altavoz.</span><span class="sxs-lookup"><span data-stu-id="b2af6-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="b2af6-114">Si se establece este atributo, el representador de audio usa el dispositivo de audio predeterminado para el rol especificado.</span><span class="sxs-lookup"><span data-stu-id="b2af6-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="b2af6-115">El valor de este atributo es un miembro de la enumeración **ERole** , que se define en el archivo de encabezado mmdeviceapi. h.</span><span class="sxs-lookup"><span data-stu-id="b2af6-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="b2af6-116">Para obtener más información, consulte la documentación básica de la API de audio.</span><span class="sxs-lookup"><span data-stu-id="b2af6-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="b2af6-117">Si no se establece este atributo, el representador de audio utiliza el dispositivo de extremo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b2af6-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="b2af6-118">Si se establece este atributo, no establezca el atributo de ID. de [**\_ extremo de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b2af6-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="b2af6-119">Si se establecen ambos atributos, se producirá un error cuando se cree el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="b2af6-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="b2af6-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b2af6-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2af6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2af6-121">Requirements</span></span>



| <span data-ttu-id="b2af6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2af6-122">Requirement</span></span> | <span data-ttu-id="b2af6-123">Value</span><span class="sxs-lookup"><span data-stu-id="b2af6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2af6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2af6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2af6-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2af6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b2af6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2af6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2af6-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2af6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b2af6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2af6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2af6-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2af6-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2af6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2af6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2af6-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2af6-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2af6-132">Atributos del representador de audio</span><span class="sxs-lookup"><span data-stu-id="b2af6-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2af6-133">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b2af6-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b2af6-134">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b2af6-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b2af6-135">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="b2af6-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




