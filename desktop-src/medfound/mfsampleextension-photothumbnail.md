---
description: Contiene la miniatura de la fotografía de un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: MFSampleExtension_PhotoThumbnail atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155961"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="ecd22-103">MFSampleExtension \_ Fotominiaturas, atributo</span><span class="sxs-lookup"><span data-stu-id="ecd22-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="ecd22-104">Contiene la miniatura de la fotografía de un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="ecd22-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="ecd22-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ecd22-105">Data type</span></span>

<span data-ttu-id="ecd22-106">**IUnknown** almacenado como **IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="ecd22-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="ecd22-107">La miniatura se configura mediante **KSPROPERTYSETID \_ ExtendedCameraControl**.</span><span class="sxs-lookup"><span data-stu-id="ecd22-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd22-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecd22-108">Remarks</span></span>

<span data-ttu-id="ecd22-109">Este atributo se establece en el [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) proporcionado por MFT0 y es la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) asociado a la miniatura de la fotografía.</span><span class="sxs-lookup"><span data-stu-id="ecd22-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="ecd22-110">El formato de la miniatura de la fotografía puede ser JPEG (imagen de tipo principal), NV12 o ARGB32.</span><span class="sxs-lookup"><span data-stu-id="ecd22-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="ecd22-111">[MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) es necesario para que las miniaturas describan el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="ecd22-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd22-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecd22-112">Requirements</span></span>



| <span data-ttu-id="ecd22-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd22-113">Requirement</span></span> | <span data-ttu-id="ecd22-114">Value</span><span class="sxs-lookup"><span data-stu-id="ecd22-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd22-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecd22-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd22-116">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="ecd22-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ecd22-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecd22-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd22-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ecd22-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ecd22-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecd22-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd22-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd22-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd22-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecd22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd22-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecd22-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecd22-123">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ecd22-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
