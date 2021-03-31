---
description: Especifica las capacidades de SVC de una secuencia de vídeo H. 264.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: MF_MT_H264_SVC_CAPABILITIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35a39b5f1727af8399d9d0c56c93d2d9d1486c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810100"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a><span data-ttu-id="117d6-103">\_Atributo de \_ \_ capacidades SVC MT H264 SVC \_</span><span class="sxs-lookup"><span data-stu-id="117d6-103">MF\_MT\_H264\_SVC\_CAPABILITIES attribute</span></span>

<span data-ttu-id="117d6-104">Especifica las capacidades de SVC de una secuencia de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="117d6-104">Specifies the SVC capabilities of an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="117d6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="117d6-105">Data type</span></span>

<span data-ttu-id="117d6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="117d6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="117d6-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="117d6-107">Get/set</span></span>

<span data-ttu-id="117d6-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="117d6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="117d6-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="117d6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="117d6-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="117d6-110">Applies to</span></span>

[<span data-ttu-id="117d6-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="117d6-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="117d6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="117d6-112">Remarks</span></span>

<span data-ttu-id="117d6-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="117d6-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="117d6-114">El valor corresponde al campo **bmSVCCapabilities** en el descriptor de fotogramas de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="117d6-114">The value corresponds to the **bmSVCCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="117d6-115">Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="117d6-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="117d6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="117d6-116">Requirements</span></span>



| <span data-ttu-id="117d6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="117d6-117">Requirement</span></span> | <span data-ttu-id="117d6-118">Value</span><span class="sxs-lookup"><span data-stu-id="117d6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="117d6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="117d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="117d6-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="117d6-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="117d6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="117d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="117d6-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="117d6-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="117d6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="117d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="117d6-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="117d6-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="117d6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="117d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="117d6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="117d6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="117d6-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="117d6-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




