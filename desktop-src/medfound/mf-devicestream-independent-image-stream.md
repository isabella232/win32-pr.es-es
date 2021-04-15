---
description: Especifica si el flujo de imagen en un origen de captura de vídeo es independiente de la secuencia de vídeo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648261"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="e80db-103">\_Atributo de \_ \_ secuencia de imagen independiente MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="e80db-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="e80db-104">Especifica si el flujo de imagen en un origen de captura de vídeo es independiente de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e80db-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e80db-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e80db-105">Data type</span></span>

<span data-ttu-id="e80db-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e80db-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e80db-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e80db-107">Remarks</span></span>

<span data-ttu-id="e80db-108">Algunas cámaras de vídeo USB exponen un flujo que genera imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="e80db-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="e80db-109">En algunas cámaras, el flujo de imagen simplemente devuelve el siguiente fotograma de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e80db-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="e80db-110">En otras cámaras, el flujo de imágenes funciona independientemente de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e80db-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="e80db-111">Si la cámara tiene una secuencia de imágenes independiente, el origen de medios del dispositivo de captura establece este atributo en **true** en el flujo de imagen.</span><span class="sxs-lookup"><span data-stu-id="e80db-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="e80db-112">Para obtener este atributo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e80db-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="e80db-113">Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="e80db-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="e80db-114">Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e80db-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="e80db-115">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="e80db-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="e80db-116">Este atributo solo se aplica cuando el atributo de [ \_ \_ \_ secuencia de imagen MF DEVICESTREAM](mf-devicestream-image-stream.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="e80db-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80db-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80db-117">Requirements</span></span>



| <span data-ttu-id="e80db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80db-118">Requirement</span></span> | <span data-ttu-id="e80db-119">Value</span><span class="sxs-lookup"><span data-stu-id="e80db-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e80db-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e80db-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80db-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e80db-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e80db-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80db-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e80db-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e80db-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80db-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e80db-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80db-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80db-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e80db-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




