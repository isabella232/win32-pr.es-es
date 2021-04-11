---
description: Devuelve el número de fotogramas de vídeo que se han codificado.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propiedad AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152431"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="a459a-103">Propiedad AVEncStatVideoCodedFrames</span><span class="sxs-lookup"><span data-stu-id="a459a-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="a459a-104">Devuelve el número de fotogramas de vídeo que se han codificado.</span><span class="sxs-lookup"><span data-stu-id="a459a-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="a459a-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a459a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a459a-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a459a-106">Data type</span></span>

<span data-ttu-id="a459a-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a459a-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a459a-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="a459a-108">Property GUID</span></span>

<span data-ttu-id="a459a-109">**CODECAPI \_ AVEncStatVideoCodedFrames**</span><span class="sxs-lookup"><span data-stu-id="a459a-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="a459a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a459a-110">Remarks</span></span>

<span data-ttu-id="a459a-111">Esta propiedad está disponible una vez completada la codificación.</span><span class="sxs-lookup"><span data-stu-id="a459a-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="a459a-112">El valor de esta propiedad es igual a la propiedad [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) menos el número de fotogramas quitados.</span><span class="sxs-lookup"><span data-stu-id="a459a-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="a459a-113">El codificador podría quitar fotogramas para permanecer dentro de las restricciones de velocidad de bits especificadas.</span><span class="sxs-lookup"><span data-stu-id="a459a-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="a459a-114">También podría quitar fotogramas al final de la secuencia (vea la propiedad [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="a459a-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="a459a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a459a-115">Requirements</span></span>



| <span data-ttu-id="a459a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a459a-116">Requirement</span></span> | <span data-ttu-id="a459a-117">Value</span><span class="sxs-lookup"><span data-stu-id="a459a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a459a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a459a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a459a-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="a459a-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a459a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a459a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a459a-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="a459a-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a459a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a459a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a459a-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a459a-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a459a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a459a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a459a-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="a459a-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a459a-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a459a-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




