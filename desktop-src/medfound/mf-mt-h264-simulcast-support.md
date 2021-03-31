---
description: Especifica el número de puntos de conexión de streaming y el número de secuencias admitidas para un codificador UVC H. 264.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: MF_MT_H264_SIMULCAST_SUPPORT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908041"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a><span data-ttu-id="4d611-103">Atributo de compatibilidad de MF \_ MT \_ H264 \_ SIMULCAST \_</span><span class="sxs-lookup"><span data-stu-id="4d611-103">MF\_MT\_H264\_SIMULCAST\_SUPPORT attribute</span></span>

<span data-ttu-id="4d611-104">Especifica el número de puntos de conexión de streaming y el número de secuencias admitidas para un codificador UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="4d611-104">Specifies the number of streaming endpoints and the number of supported streams for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="4d611-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4d611-105">Data type</span></span>

<span data-ttu-id="4d611-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4d611-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4d611-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="4d611-107">Get/set</span></span>

<span data-ttu-id="4d611-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4d611-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4d611-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4d611-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4d611-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4d611-110">Applies to</span></span>

[<span data-ttu-id="4d611-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4d611-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="4d611-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d611-112">Remarks</span></span>

<span data-ttu-id="4d611-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="4d611-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="4d611-114">El valor corresponde al campo **bSimulcastSupport** en el descriptor de formato de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="4d611-114">The value corresponds to the **bSimulcastSupport** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="4d611-115">Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="4d611-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d611-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d611-116">Requirements</span></span>



| <span data-ttu-id="4d611-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d611-117">Requirement</span></span> | <span data-ttu-id="4d611-118">Value</span><span class="sxs-lookup"><span data-stu-id="4d611-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d611-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d611-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d611-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="4d611-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4d611-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d611-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d611-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="4d611-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4d611-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d611-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d611-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d611-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d611-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d611-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d611-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d611-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d611-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="4d611-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




