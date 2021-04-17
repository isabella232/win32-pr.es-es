---
description: Especifica el formato de salida de un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697953"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="4401b-103">Atributo \_ de \_ \_ tipo de medio de atributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="4401b-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="4401b-104">Especifica el formato de salida de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4401b-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="4401b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4401b-105">Data type</span></span>

<span data-ttu-id="4401b-106">**[**MFT \_ REGISTRAR \_ \_ información de tipo**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** almacenada como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4401b-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="4401b-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="4401b-107">Get/set</span></span>

<span data-ttu-id="4401b-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="4401b-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="4401b-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="4401b-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="4401b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4401b-110">Remarks</span></span>

<span data-ttu-id="4401b-111">Este atributo contiene un par de GUID: un tipo principal y un subtipo.</span><span class="sxs-lookup"><span data-stu-id="4401b-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="4401b-112">Estos GUID describen el formato de salida predeterminado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4401b-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="4401b-113">Es posible que el dispositivo admita formatos de salida adicionales.</span><span class="sxs-lookup"><span data-stu-id="4401b-113">The device might support additional output formats.</span></span>

<span data-ttu-id="4401b-114">Por ejemplo, si un dispositivo de captura de vídeo genera vídeo RGB-32, el valor de este atributo es `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="4401b-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="4401b-115">Este atributo es una sugerencia para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4401b-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="4401b-116">Para obtener el formato de salida exacto, cree el origen de medios para el dispositivo y obtenga el descriptor de presentación del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="4401b-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="4401b-117">Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="4401b-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="4401b-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="4401b-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="4401b-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="4401b-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="4401b-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4401b-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4401b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4401b-121">Requirements</span></span>



| <span data-ttu-id="4401b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4401b-122">Requirement</span></span> | <span data-ttu-id="4401b-123">Value</span><span class="sxs-lookup"><span data-stu-id="4401b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4401b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4401b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4401b-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4401b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4401b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4401b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4401b-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4401b-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4401b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4401b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4401b-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4401b-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4401b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4401b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4401b-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4401b-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4401b-132">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="4401b-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="4401b-133">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4401b-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




