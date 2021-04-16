---
description: Devuelve el número de fotogramas de vídeo que el codificador ha recibido.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propiedad AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659267"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="fd1e3-103">Propiedad AVEncStatVideoTotalFrames</span><span class="sxs-lookup"><span data-stu-id="fd1e3-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="fd1e3-104">Devuelve el número de fotogramas de vídeo que el codificador ha recibido.</span><span class="sxs-lookup"><span data-stu-id="fd1e3-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="fd1e3-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fd1e3-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd1e3-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fd1e3-106">Data type</span></span>

<span data-ttu-id="fd1e3-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fd1e3-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fd1e3-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="fd1e3-108">Property GUID</span></span>

<span data-ttu-id="fd1e3-109">**CODECAPI \_ AVEncStatVideoTotalFrames**</span><span class="sxs-lookup"><span data-stu-id="fd1e3-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="fd1e3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd1e3-110">Remarks</span></span>

<span data-ttu-id="fd1e3-111">Esta propiedad está disponible una vez completada la codificación.</span><span class="sxs-lookup"><span data-stu-id="fd1e3-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="fd1e3-112">El valor de esta propiedad es el número total de fotogramas enviados al codificador, incluidos los fotogramas que se quitaron.</span><span class="sxs-lookup"><span data-stu-id="fd1e3-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="fd1e3-113">Para obtener el número de Marcos codificados, lea la propiedad [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fd1e3-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1e3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd1e3-114">Requirements</span></span>



| <span data-ttu-id="fd1e3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1e3-115">Requirement</span></span> | <span data-ttu-id="fd1e3-116">Value</span><span class="sxs-lookup"><span data-stu-id="fd1e3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1e3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd1e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1e3-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="fd1e3-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fd1e3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd1e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1e3-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="fd1e3-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fd1e3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd1e3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1e3-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1e3-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1e3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd1e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1e3-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="fd1e3-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fd1e3-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fd1e3-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




