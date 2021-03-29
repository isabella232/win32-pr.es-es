---
description: Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Propiedad AVDecVideoAcceleration_H264 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906798"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="ee0b7-103">\_Propiedad H264 de AVDecVideoAcceleration</span><span class="sxs-lookup"><span data-stu-id="ee0b7-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="ee0b7-104">Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="ee0b7-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="ee0b7-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ee0b7-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee0b7-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ee0b7-106">Data type</span></span>

<span data-ttu-id="ee0b7-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ee0b7-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ee0b7-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="ee0b7-108">Property GUID</span></span>

<span data-ttu-id="ee0b7-109">**CODECAPI \_ AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="ee0b7-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee0b7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee0b7-110">Remarks</span></span>

<span data-ttu-id="ee0b7-111">Si el valor es cero, el descodificador no usa DirectX video Acceleration (DXVA) para la descodificación de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="ee0b7-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="ee0b7-112">En el caso de los filtros DirectShow, establezca esta propiedad antes de que se conecte el PIN de salida del descodificador.</span><span class="sxs-lookup"><span data-stu-id="ee0b7-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0b7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee0b7-113">Requirements</span></span>



| <span data-ttu-id="ee0b7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee0b7-114">Requirement</span></span> | <span data-ttu-id="ee0b7-115">Value</span><span class="sxs-lookup"><span data-stu-id="ee0b7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0b7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee0b7-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="ee0b7-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ee0b7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ee0b7-119">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="ee0b7-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ee0b7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee0b7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee0b7-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee0b7-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0b7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee0b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0b7-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="ee0b7-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ee0b7-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ee0b7-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




