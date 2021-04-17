---
description: Número máximo de marcos que el codificador H. 264 tarda en responder a un comando.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: MF_MT_H264_MAX_CODEC_CONFIG_DELAY atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659871"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="f3b81-103">\_Atributo de \_ \_ retraso de \_ configuración de códecs de \_ MF MT H264 Max \_</span><span class="sxs-lookup"><span data-stu-id="f3b81-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="f3b81-104">Número máximo de marcos que el codificador H. 264 tarda en responder a un comando.</span><span class="sxs-lookup"><span data-stu-id="f3b81-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3b81-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f3b81-105">Data type</span></span>

<span data-ttu-id="f3b81-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3b81-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f3b81-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="f3b81-107">Get/set</span></span>

<span data-ttu-id="f3b81-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f3b81-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f3b81-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f3b81-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f3b81-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f3b81-110">Applies to</span></span>

[<span data-ttu-id="f3b81-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f3b81-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="f3b81-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3b81-112">Remarks</span></span>

<span data-ttu-id="f3b81-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="f3b81-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="f3b81-114">El valor corresponde al campo **bMaxCodecConfigDelay** en el descriptor de formato de vídeo UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="f3b81-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="f3b81-115">Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="f3b81-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b81-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b81-116">Requirements</span></span>



| <span data-ttu-id="f3b81-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b81-117">Requirement</span></span> | <span data-ttu-id="f3b81-118">Value</span><span class="sxs-lookup"><span data-stu-id="f3b81-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b81-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3b81-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b81-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f3b81-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f3b81-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3b81-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b81-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f3b81-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f3b81-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3b81-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b81-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b81-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b81-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b81-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3b81-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3b81-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="f3b81-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




