---
description: Especifica el modo de uso para un codificador UVC H. 264.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: MF_MT_H264_USAGE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154463"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="42cbe-103">MF \_ MT \_ H264 \_ atributo Usage</span><span class="sxs-lookup"><span data-stu-id="42cbe-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="42cbe-104">Especifica el modo de uso para un codificador UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="42cbe-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="42cbe-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="42cbe-105">Data type</span></span>

<span data-ttu-id="42cbe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="42cbe-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="42cbe-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="42cbe-107">Get/set</span></span>

<span data-ttu-id="42cbe-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="42cbe-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="42cbe-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="42cbe-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="42cbe-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="42cbe-110">Applies to</span></span>

[<span data-ttu-id="42cbe-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="42cbe-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="42cbe-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42cbe-112">Remarks</span></span>

<span data-ttu-id="42cbe-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="42cbe-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="42cbe-114">El valor corresponde al campo **bUsage** del control de sondeo y confirmación de UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="42cbe-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="42cbe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42cbe-115">Requirements</span></span>



| <span data-ttu-id="42cbe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="42cbe-116">Requirement</span></span> | <span data-ttu-id="42cbe-117">Value</span><span class="sxs-lookup"><span data-stu-id="42cbe-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42cbe-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42cbe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42cbe-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="42cbe-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="42cbe-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42cbe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42cbe-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="42cbe-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="42cbe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42cbe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42cbe-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42cbe-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42cbe-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="42cbe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cbe-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42cbe-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="42cbe-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="42cbe-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




