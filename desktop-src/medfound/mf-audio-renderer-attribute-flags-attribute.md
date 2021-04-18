---
description: Contiene marcas para configurar el representador de audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687220"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="71039-103">\_Atributo de \_ marcadores de \_ atributo de representador de audio MF \_</span><span class="sxs-lookup"><span data-stu-id="71039-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="71039-104">Contiene marcas para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="71039-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="71039-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71039-105">Data type</span></span>

<span data-ttu-id="71039-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="71039-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="71039-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71039-107">Remarks</span></span>

<span data-ttu-id="71039-108">El valor de este atributo es **una operación OR bit a bit** de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="71039-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="71039-109">Value</span><span class="sxs-lookup"><span data-stu-id="71039-109">Value</span></span>                                                   | <span data-ttu-id="71039-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="71039-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71039-111">**\_etiquetas de \_ atributo de representador de audio MF \_ \_ \_ CROSSPROCESS**</span><span class="sxs-lookup"><span data-stu-id="71039-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="71039-112">El representador de audio utiliza una sesión de audio entre procesos.</span><span class="sxs-lookup"><span data-stu-id="71039-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="71039-113">Esta marca permite que los representadores de audio en varios procesos compartan la misma sesión de audio, junto con los controles de volumen y de directiva asociados.</span><span class="sxs-lookup"><span data-stu-id="71039-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="71039-114">Si no se establece esta marca, los representadores de audio no podrán compartir la sesión de audio en otros procesos.</span><span class="sxs-lookup"><span data-stu-id="71039-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="71039-115">**\_marcas de \_ atributo de representador de audio MF \_ \_ \_ nopersist**</span><span class="sxs-lookup"><span data-stu-id="71039-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="71039-116">La API de sesión de audio de Windows (WASAPI) no conservará las propiedades de esta sesión de audio, como el volumen de sesión.</span><span class="sxs-lookup"><span data-stu-id="71039-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="71039-117">Si no se establece esta marca, WASAPI conservará las propiedades de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="71039-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="71039-118">Puede usar este atributo para configurar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="71039-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="71039-119">El uso depende de la función a la que llame para crear el representador de audio:</span><span class="sxs-lookup"><span data-stu-id="71039-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="71039-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="71039-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="71039-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="71039-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="71039-122">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="71039-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="71039-123">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="71039-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="71039-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71039-124">Requirements</span></span>



| <span data-ttu-id="71039-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="71039-125">Requirement</span></span> | <span data-ttu-id="71039-126">Value</span><span class="sxs-lookup"><span data-stu-id="71039-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71039-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71039-127">Minimum supported client</span></span><br/> | <span data-ttu-id="71039-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71039-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71039-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71039-129">Minimum supported server</span></span><br/> | <span data-ttu-id="71039-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71039-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71039-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71039-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="71039-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="71039-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71039-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="71039-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71039-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71039-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="71039-135">Atributos del representador de audio</span><span class="sxs-lookup"><span data-stu-id="71039-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="71039-136">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="71039-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="71039-137">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="71039-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="71039-138">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="71039-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




