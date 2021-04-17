---
description: Establece el uso de vídeo para un codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Propiedad CODECAPI_AVEncVideoUsage (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652353"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="20b91-103">\_Propiedad AVEncVideoUsage de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="20b91-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="20b91-104">Establece el uso de vídeo para un codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="20b91-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="20b91-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="20b91-105">Data type</span></span>

<span data-ttu-id="20b91-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="20b91-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="20b91-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="20b91-107">Property GUID</span></span>

<span data-ttu-id="20b91-108">**CODECAPI \_ AVEncVideoUsage**</span><span class="sxs-lookup"><span data-stu-id="20b91-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="20b91-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20b91-109">Remarks</span></span>

<span data-ttu-id="20b91-110">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="20b91-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="20b91-111">[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades del codificador estático.</span><span class="sxs-lookup"><span data-stu-id="20b91-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="20b91-112">Una vez que se han establecido, solo surtirán efecto después de llamar a un tipo de medio establecido en el PIN de salida de la cámara.</span><span class="sxs-lookup"><span data-stu-id="20b91-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b91-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b91-113">Requirements</span></span>



| <span data-ttu-id="20b91-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b91-114">Requirement</span></span> | <span data-ttu-id="20b91-115">Value</span><span class="sxs-lookup"><span data-stu-id="20b91-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20b91-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b91-116">Minimum supported client</span></span><br/> | <span data-ttu-id="20b91-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="20b91-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="20b91-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b91-118">Minimum supported server</span></span><br/> | <span data-ttu-id="20b91-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="20b91-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="20b91-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20b91-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b91-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b91-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20b91-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="20b91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b91-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20b91-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

