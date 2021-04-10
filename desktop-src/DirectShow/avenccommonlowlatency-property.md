---
description: Especifica si el flujo de salida se debe estructurar para que la secuencia codificada tenga una latencia de descodificación baja.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propiedad AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274793"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="fc26c-103">Propiedad AVEncCommonLowLatency</span><span class="sxs-lookup"><span data-stu-id="fc26c-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="fc26c-104">Especifica si el flujo de salida se debe estructurar para que la secuencia codificada tenga una latencia de descodificación baja.</span><span class="sxs-lookup"><span data-stu-id="fc26c-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="fc26c-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fc26c-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc26c-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fc26c-106">Data type</span></span>

<span data-ttu-id="fc26c-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="fc26c-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fc26c-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="fc26c-108">Property GUID</span></span>

<span data-ttu-id="fc26c-109">**CODECAPI \_ AVEncCommonLowLatency**</span><span class="sxs-lookup"><span data-stu-id="fc26c-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc26c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc26c-110">Remarks</span></span>

<span data-ttu-id="fc26c-111">La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer.</span><span class="sxs-lookup"><span data-stu-id="fc26c-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="fc26c-112">Por ejemplo, si se establece esta propiedad en **Variant \_ true** en un codificador de vídeo MPEG, se limitan los tipos de estructuras GOP que el codificador puede utilizar.</span><span class="sxs-lookup"><span data-stu-id="fc26c-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc26c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc26c-113">Requirements</span></span>



| <span data-ttu-id="fc26c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc26c-114">Requirement</span></span> | <span data-ttu-id="fc26c-115">Value</span><span class="sxs-lookup"><span data-stu-id="fc26c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc26c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc26c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc26c-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="fc26c-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fc26c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc26c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc26c-119">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="fc26c-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fc26c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc26c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc26c-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc26c-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc26c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc26c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc26c-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="fc26c-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fc26c-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fc26c-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




