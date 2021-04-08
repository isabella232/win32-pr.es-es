---
description: Especifica la velocidad de bits media de la secuencia de audio codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Propiedad AVEncAudioMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e311686e6113003593c8a6dbe02a9fca1f30b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080052"
---
# <a name="avencaudiomeanbitrate-property"></a><span data-ttu-id="e3b51-104">Propiedad AVEncAudioMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="e3b51-104">AVEncAudioMeanBitRate property</span></span>

<span data-ttu-id="e3b51-105">Especifica la velocidad de bits media de la secuencia de audio codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e3b51-105">Specifies the average bit rate of the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="e3b51-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="e3b51-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="e3b51-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e3b51-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3b51-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e3b51-108">Data type</span></span>

<span data-ttu-id="e3b51-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="e3b51-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e3b51-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3b51-110">Property GUID</span></span>

<span data-ttu-id="e3b51-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="e3b51-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="e3b51-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3b51-112">Property value</span></span>

<span data-ttu-id="e3b51-113">Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.</span><span class="sxs-lookup"><span data-stu-id="e3b51-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b51-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b51-114">Requirements</span></span>



| <span data-ttu-id="e3b51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b51-115">Requirement</span></span> | <span data-ttu-id="e3b51-116">Value</span><span class="sxs-lookup"><span data-stu-id="e3b51-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b51-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b51-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="e3b51-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e3b51-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b51-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="e3b51-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e3b51-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b51-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3b51-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b51-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b51-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b51-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b51-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="e3b51-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e3b51-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e3b51-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




