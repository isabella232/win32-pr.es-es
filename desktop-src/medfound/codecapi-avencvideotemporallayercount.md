---
description: Establece el número de capas temporales de vídeo para un codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Propiedad CODECAPI_AVEncVideoTemporalLayerCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496840"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="1c0f6-103">\_Propiedad AVEncVideoTemporalLayerCount de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="1c0f6-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="1c0f6-104">Establece el número de capas temporales de vídeo para un codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1c0f6-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c0f6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c0f6-105">Data type</span></span>

<span data-ttu-id="1c0f6-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="1c0f6-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="1c0f6-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="1c0f6-107">Property GUID</span></span>

<span data-ttu-id="1c0f6-108">**CODECAPI \_ AVEncVideoTemporalLayerCount**</span><span class="sxs-lookup"><span data-stu-id="1c0f6-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c0f6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c0f6-109">Remarks</span></span>

<span data-ttu-id="1c0f6-110">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="1c0f6-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="1c0f6-111">CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades del codificador estático.</span><span class="sxs-lookup"><span data-stu-id="1c0f6-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="1c0f6-112">Una vez que se han establecido, solo surtirán efecto después de llamar a un tipo de medio establecido en el PIN de salida de la cámara.</span><span class="sxs-lookup"><span data-stu-id="1c0f6-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c0f6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c0f6-113">Requirements</span></span>



| <span data-ttu-id="1c0f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c0f6-114">Requirement</span></span> | <span data-ttu-id="1c0f6-115">Value</span><span class="sxs-lookup"><span data-stu-id="1c0f6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0f6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c0f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0f6-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c0f6-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1c0f6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c0f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0f6-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c0f6-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1c0f6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c0f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c0f6-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c0f6-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0f6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c0f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0f6-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c0f6-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

