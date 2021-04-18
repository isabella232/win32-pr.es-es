---
description: Especifica el modo de control de velocidad para una secuencia de vídeo H. 264.
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: MF_MT_H264_RATE_CONTROL_MODES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3fc19070cd3b45aa25a1307a216f611dce1fd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720372"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a><span data-ttu-id="bf86a-103">\_Controlador MF MT \_ H264 \_ rate \_ \_ modes Attribute</span><span class="sxs-lookup"><span data-stu-id="bf86a-103">MF\_MT\_H264\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="bf86a-104">Especifica el modo de control de velocidad para una secuencia de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="bf86a-104">Specifies the rate-control mode for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="bf86a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bf86a-105">Data type</span></span>

<span data-ttu-id="bf86a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bf86a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="bf86a-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="bf86a-107">Get/set</span></span>

<span data-ttu-id="bf86a-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="bf86a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="bf86a-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="bf86a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="bf86a-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="bf86a-110">Applies to</span></span>

[<span data-ttu-id="bf86a-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="bf86a-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="bf86a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf86a-112">Remarks</span></span>

<span data-ttu-id="bf86a-113">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="bf86a-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="bf86a-114">El valor corresponde al campo **bmRateControlModes** del control de sondeo y confirmación de UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="bf86a-114">The value corresponds to the **bmRateControlModes** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf86a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf86a-115">Requirements</span></span>



| <span data-ttu-id="bf86a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf86a-116">Requirement</span></span> | <span data-ttu-id="bf86a-117">Value</span><span class="sxs-lookup"><span data-stu-id="bf86a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf86a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf86a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf86a-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf86a-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bf86a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf86a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf86a-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf86a-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bf86a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf86a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf86a-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf86a-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf86a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf86a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf86a-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf86a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf86a-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="bf86a-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




