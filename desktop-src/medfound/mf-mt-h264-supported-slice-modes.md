---
description: Especifica los modos de segmento admitidos para una secuencia de vídeo H. 264.
ms.assetid: 72DA62EC-A509-4C3B-A51D-7313C176AAA9
title: MF_MT_H264_SUPPORTED_SLICE_MODES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9258a2ce2b9bef050fc6ea4468026539ff67f1be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686836"
---
# <a name="mf_mt_h264_supported_slice_modes-attribute"></a><span data-ttu-id="d3640-103">MF \_ MT \_ H264 \_ el \_ atributo Supported Segment \_ modes</span><span class="sxs-lookup"><span data-stu-id="d3640-103">MF\_MT\_H264\_SUPPORTED\_SLICE\_MODES attribute</span></span>

<span data-ttu-id="d3640-104">Especifica los modos de segmento admitidos para una secuencia de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="d3640-104">Specifies the supported slice modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d3640-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d3640-105">Data type</span></span>

<span data-ttu-id="d3640-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d3640-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d3640-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="d3640-107">Get/set</span></span>

<span data-ttu-id="d3640-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d3640-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d3640-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d3640-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d3640-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d3640-110">Applies to</span></span>

[<span data-ttu-id="d3640-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d3640-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="d3640-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3640-112">Remarks</span></span>

<span data-ttu-id="d3640-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="d3640-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="d3640-114">El valor corresponde al campo **bmSupportedSliceModes** en el descriptor de formato de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="d3640-114">The value corresponds to the **bmSupportedSliceModes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="d3640-115">Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="d3640-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3640-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3640-116">Requirements</span></span>



| <span data-ttu-id="d3640-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3640-117">Requirement</span></span> | <span data-ttu-id="d3640-118">Value</span><span class="sxs-lookup"><span data-stu-id="d3640-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3640-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3640-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3640-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d3640-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d3640-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3640-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3640-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d3640-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d3640-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3640-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3640-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3640-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3640-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3640-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3640-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3640-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3640-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="d3640-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




