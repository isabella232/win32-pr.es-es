---
description: Contiene el IMFMediaType que describe el tipo de formato de imagen contenido en el \_ atributo de Fotominiatura MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721343"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="aecdb-103">\_Atributo PhotoThumbnailMediaType de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="aecdb-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="aecdb-104">Contiene el [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el tipo de formato de imagen contenido en el atributo de [ \_ fotominiatura MFSampleExtension](mfsampleextension-photothumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="aecdb-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="aecdb-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aecdb-105">Data type</span></span>

<span data-ttu-id="aecdb-106">**IUnknown** almacenado como **IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="aecdb-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="aecdb-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aecdb-107">Remarks</span></span>

<span data-ttu-id="aecdb-108">Si el atributo de [ \_ fotominiatura MFSampleExtension](mfsampleextension-photothumbnail.md) está presente en el ejemplo Photo, \_ se requiere MFSampleExtension PhotoThumbnailMediaType y debe contener, como mínimo, el [ \_ tipo de módulo MF MT \_ major \_ ](mf-mt-major-type-attribute.md), el [ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md) y [ \_ \_ \_ el tamaño de marco MF MT](mf-mt-frame-size-attribute.md) que describen la miniatura.</span><span class="sxs-lookup"><span data-stu-id="aecdb-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecdb-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aecdb-109">Requirements</span></span>



| <span data-ttu-id="aecdb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="aecdb-110">Requirement</span></span> | <span data-ttu-id="aecdb-111">Value</span><span class="sxs-lookup"><span data-stu-id="aecdb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aecdb-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aecdb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="aecdb-113">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="aecdb-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="aecdb-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aecdb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="aecdb-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="aecdb-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aecdb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aecdb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="aecdb-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecdb-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecdb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="aecdb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecdb-119">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aecdb-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aecdb-120">Fotominiatura MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="aecdb-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




