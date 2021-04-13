---
description: Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en la calidad.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: Propiedad MFPKEY_WMAENC_AVGBYTESPERSEC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543966"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a><span data-ttu-id="14385-103">\_ \_ Propiedad AVGBYTESPERSEC de MFPKEY WMAENC</span><span class="sxs-lookup"><span data-stu-id="14385-103">MFPKEY\_WMAENC\_AVGBYTESPERSEC Property</span></span>

<span data-ttu-id="14385-104">Especifica el promedio de bytes por segundo en una secuencia de audio de velocidad de bits variable (VBR) basada en la calidad.</span><span class="sxs-lookup"><span data-stu-id="14385-104">Specifies the average bytes per second in a quality-based variable-bit-rate (VBR) audio stream.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="14385-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="14385-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="14385-106">g \_ wszWMACAvgBytesPerSecond</span><span class="sxs-lookup"><span data-stu-id="14385-106">g\_wszWMACAvgBytesPerSecond</span></span>

## <a name="data-type"></a><span data-ttu-id="14385-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="14385-107">Data Type</span></span>

<span data-ttu-id="14385-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="14385-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="14385-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14385-109">Remarks</span></span>

<span data-ttu-id="14385-110">Puede obtener este valor desde el descodificador después de codificar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="14385-110">You can get this value from the decoder after the stream is encoded.</span></span>

<span data-ttu-id="14385-111">Este valor es necesario para que el descodificador de audio descomprima correctamente el contenido.</span><span class="sxs-lookup"><span data-stu-id="14385-111">This value is required by the audio decoder to properly decompress the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="14385-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14385-112">Requirements</span></span>



| <span data-ttu-id="14385-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="14385-113">Requirement</span></span> | <span data-ttu-id="14385-114">Value</span><span class="sxs-lookup"><span data-stu-id="14385-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14385-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14385-115">Minimum supported client</span></span><br/> | <span data-ttu-id="14385-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="14385-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="14385-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14385-117">Minimum supported server</span></span><br/> | <span data-ttu-id="14385-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="14385-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14385-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14385-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="14385-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14385-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14385-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="14385-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14385-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14385-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




