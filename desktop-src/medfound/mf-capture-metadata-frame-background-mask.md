---
description: Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691866"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="7c2f5-103">Atributo MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK</span><span class="sxs-lookup"><span data-stu-id="7c2f5-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="7c2f5-104">Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7c2f5-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c2f5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7c2f5-105">Data type</span></span>

<span data-ttu-id="7c2f5-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="7c2f5-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c2f5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c2f5-107">Remarks</span></span>

<span data-ttu-id="7c2f5-108">Los datos que lleva este atributo son una estructura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) que contiene información sobre las dimensiones de la máscara de fondo, así como su cobertura del marco del que se deduce, que es el marco que genera la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7c2f5-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="7c2f5-109">También lleva un búfer contiguo que representa la máscara que va a aprovechar la aplicación consumidora para definir qué píxeles se consideran parte del primer plano o el fondo.</span><span class="sxs-lookup"><span data-stu-id="7c2f5-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="7c2f5-110">La aplicación consumidora controla la correlación de escala y coordenada de imagen de la máscara con respecto al marco.</span><span class="sxs-lookup"><span data-stu-id="7c2f5-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="7c2f5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c2f5-111">Requirements</span></span>



| <span data-ttu-id="7c2f5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c2f5-112">Requirement</span></span> | <span data-ttu-id="7c2f5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7c2f5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2f5-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c2f5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2f5-115">Windows Compilación 22000t</span><span class="sxs-lookup"><span data-stu-id="7c2f5-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="7c2f5-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c2f5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2f5-117">Windows Compilación 22000</span><span class="sxs-lookup"><span data-stu-id="7c2f5-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="7c2f5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c2f5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2f5-119"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2f5-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c2f5-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c2f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2f5-121">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="7c2f5-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c2f5-122">**ATTRIBUTEAttributes::GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7c2f5-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7c2f5-123">**ATTRIBUTEAttributes::SetBlob**</span><span class="sxs-lookup"><span data-stu-id="7c2f5-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7c2f5-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7c2f5-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7c2f5-125">Atributos de tipo multimedia</span><span class="sxs-lookup"><span data-stu-id="7c2f5-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




