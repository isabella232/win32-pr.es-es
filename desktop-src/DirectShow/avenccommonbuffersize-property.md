---
description: Especifica el tamaño del búfer usado durante la codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propiedad AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152579"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="db71f-104">Propiedad AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="db71f-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="db71f-105">Especifica el tamaño del búfer usado durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="db71f-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="db71f-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="db71f-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="db71f-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="db71f-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="db71f-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="db71f-108">Data type</span></span>

<span data-ttu-id="db71f-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="db71f-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="db71f-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="db71f-110">Property GUID</span></span>

<span data-ttu-id="db71f-111">**CODECAPI \_ AVEncCommonBufferSize**</span><span class="sxs-lookup"><span data-stu-id="db71f-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="db71f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="db71f-112">Property value</span></span>

<span data-ttu-id="db71f-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="db71f-113">This property has a linear range of values.</span></span> <span data-ttu-id="db71f-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="db71f-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="db71f-115">Los intervalos de parámetros no se admiten para los codificadores de cámara H. 264 UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="db71f-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="db71f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db71f-116">Remarks</span></span>

<span data-ttu-id="db71f-117">En algunos formatos de vídeo, el tamaño de búfer se especifica en bits y, en el caso de otros, se especifica en bytes.</span><span class="sxs-lookup"><span data-stu-id="db71f-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="db71f-118">Vea los comentarios siguientes para obtener información específica.</span><span class="sxs-lookup"><span data-stu-id="db71f-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="db71f-119">Para vídeo MPEG, esta propiedad define el tamaño de búfer del comprobador de búfer de vídeo (VBV).</span><span class="sxs-lookup"><span data-stu-id="db71f-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="db71f-120">El tamaño del búfer está en bits.</span><span class="sxs-lookup"><span data-stu-id="db71f-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="db71f-121">Para el vídeo H. 264 y el Windows Media Video, la propiedad define el tamaño hipotético del descodificador de referencia (HRD).</span><span class="sxs-lookup"><span data-stu-id="db71f-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="db71f-122">El tamaño del búfer está en bytes.</span><span class="sxs-lookup"><span data-stu-id="db71f-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="db71f-123">En el caso de las cámaras de codificación UVC 1,5 H264, el valor de CPB enviado al codificador de cámara debe estar alineado con 16 bits.</span><span class="sxs-lookup"><span data-stu-id="db71f-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="db71f-124">El tamaño del búfer está en bytes.</span><span class="sxs-lookup"><span data-stu-id="db71f-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="db71f-125">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="db71f-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="db71f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db71f-126">Requirements</span></span>



| <span data-ttu-id="db71f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="db71f-127">Requirement</span></span> | <span data-ttu-id="db71f-128">Value</span><span class="sxs-lookup"><span data-stu-id="db71f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db71f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db71f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db71f-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="db71f-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="db71f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db71f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db71f-132">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="db71f-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="db71f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db71f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="db71f-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db71f-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db71f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="db71f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db71f-136">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="db71f-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="db71f-137">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="db71f-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

