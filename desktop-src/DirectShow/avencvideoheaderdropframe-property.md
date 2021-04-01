---
description: Especifica el valor de la marca de fotogramas en el encabezado grupo de imágenes (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propiedad AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906827"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="20885-103">Propiedad AVEncVideoHeaderDropFrame</span><span class="sxs-lookup"><span data-stu-id="20885-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="20885-104">Especifica el valor de la marca de fotogramas en el encabezado grupo de imágenes (GOP).</span><span class="sxs-lookup"><span data-stu-id="20885-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="20885-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="20885-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="20885-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="20885-106">Data type</span></span>

<span data-ttu-id="20885-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="20885-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="20885-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="20885-108">Property GUID</span></span>

<span data-ttu-id="20885-109">**CODECAPI \_ AVEncVideoHeaderDropFrame**</span><span class="sxs-lookup"><span data-stu-id="20885-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="20885-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="20885-110">Property value</span></span>

<span data-ttu-id="20885-111">El valor de esta propiedad puede ser 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="20885-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="20885-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20885-112">Remarks</span></span>

<span data-ttu-id="20885-113">El modo de marco de colocación se usa en vídeo NTSC para corregir la discrepancia entre el vídeo, que es 29,97 fotogramas por segundo, y la presentación del código de tiempo, que es 30 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="20885-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="20885-114">En el modo de marco de colocación, los números de fotogramas 00 y 01 se omiten al principio de cada minuto, excepto en los minutos que son incluso múltiplos de diez (00, 10, 20, etc.).</span><span class="sxs-lookup"><span data-stu-id="20885-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="20885-115">Solo se quitan los números de fotogramas del código de tiempo; no se quita ningún fotograma real.</span><span class="sxs-lookup"><span data-stu-id="20885-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="20885-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20885-116">Requirements</span></span>



| <span data-ttu-id="20885-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="20885-117">Requirement</span></span> | <span data-ttu-id="20885-118">Value</span><span class="sxs-lookup"><span data-stu-id="20885-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20885-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20885-119">Minimum supported client</span></span><br/> | <span data-ttu-id="20885-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="20885-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="20885-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20885-121">Minimum supported server</span></span><br/> | <span data-ttu-id="20885-122">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="20885-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="20885-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20885-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="20885-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="20885-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20885-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="20885-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20885-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="20885-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="20885-127">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="20885-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




