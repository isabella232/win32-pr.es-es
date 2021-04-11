---
description: Especifica el modo de control de velocidad.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propiedad AVEncCommonRateControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274791"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="8a414-103">Propiedad AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="8a414-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="8a414-104">Especifica el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="8a414-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="8a414-105">Las aplicaciones pueden establecer esta propiedad para especificar el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="8a414-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="8a414-106">Los codificadores también pueden devolver esta propiedad como una capacidad.</span><span class="sxs-lookup"><span data-stu-id="8a414-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="8a414-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8a414-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a414-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8a414-108">Data type</span></span>

<span data-ttu-id="8a414-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8a414-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8a414-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a414-110">Property GUID</span></span>

<span data-ttu-id="8a414-111">**CODECAPI \_ AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="8a414-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="8a414-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a414-112">Property value</span></span>

<span data-ttu-id="8a414-113">El valor de esta propiedad es un miembro de la enumeración [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .</span><span class="sxs-lookup"><span data-stu-id="8a414-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a414-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a414-114">Remarks</span></span>

<span data-ttu-id="8a414-115">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="8a414-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="8a414-116">[CODECAPI \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)y CODECAPI \_ AVEncCommonRateControlMode son propiedades del codificador estático.</span><span class="sxs-lookup"><span data-stu-id="8a414-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="8a414-117">Una vez que se han establecido, solo surtirán efecto después de llamar a un tipo de medio establecido en el PIN de salida de la cámara.</span><span class="sxs-lookup"><span data-stu-id="8a414-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a414-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a414-118">Requirements</span></span>



| <span data-ttu-id="8a414-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a414-119">Requirement</span></span> | <span data-ttu-id="8a414-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a414-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a414-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a414-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a414-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="8a414-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8a414-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a414-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a414-124">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="8a414-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8a414-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a414-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a414-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a414-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a414-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a414-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a414-128">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="8a414-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8a414-129">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8a414-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

