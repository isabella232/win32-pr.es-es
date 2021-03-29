---
description: Especifica si una secuencia de un origen de captura de vídeo es una secuencia de imagen fija.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: MF_DEVICESTREAM_IMAGE_STREAM atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810484"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="d2922-103">\_Atributo de \_ secuencia de imagen MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="d2922-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="d2922-104">Especifica si una secuencia de un origen de captura de vídeo es una secuencia de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="d2922-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2922-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d2922-105">Data type</span></span>

<span data-ttu-id="d2922-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d2922-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d2922-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2922-107">Remarks</span></span>

<span data-ttu-id="d2922-108">Algunas cámaras de vídeo exponen una secuencia de imágenes fijas que produce imágenes de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="d2922-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="d2922-109">El flujo de imágenes puede generar imágenes sin comprimir o imágenes JPEG.</span><span class="sxs-lookup"><span data-stu-id="d2922-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="d2922-110">Si la cámara tiene un flujo de imagen, el origen de medios del dispositivo de captura establece este atributo en **true** en el flujo de imagen.</span><span class="sxs-lookup"><span data-stu-id="d2922-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="d2922-111">Para obtener este atributo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2922-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="d2922-112">Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="d2922-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="d2922-113">Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d2922-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="d2922-114">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="d2922-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2922-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2922-115">Requirements</span></span>



| <span data-ttu-id="d2922-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2922-116">Requirement</span></span> | <span data-ttu-id="d2922-117">Value</span><span class="sxs-lookup"><span data-stu-id="d2922-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2922-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2922-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2922-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2922-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d2922-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2922-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2922-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2922-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d2922-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2922-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2922-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2922-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2922-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2922-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2922-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2922-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




