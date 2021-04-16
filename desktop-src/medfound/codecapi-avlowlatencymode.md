---
description: Habilita el modo de baja latencia en un códec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Propiedad CODECAPI_AVLowLatencyMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696167"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="66d87-103">\_Propiedad AVLowLatencyMode de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="66d87-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="66d87-104">Habilita el modo de baja latencia en un códec.</span><span class="sxs-lookup"><span data-stu-id="66d87-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="66d87-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="66d87-105">Data type</span></span>

<span data-ttu-id="66d87-106">**ULong** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="66d87-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="66d87-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="66d87-107">Property GUID</span></span>

<span data-ttu-id="66d87-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="66d87-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="66d87-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="66d87-109">Property value</span></span>

<span data-ttu-id="66d87-110">Si el valor es distinto de cero, el modo de latencia baja está habilitado.</span><span class="sxs-lookup"><span data-stu-id="66d87-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="66d87-111">Si el valor es cero, el modo de latencia baja está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="66d87-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d87-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d87-112">Remarks</span></span>

<span data-ttu-id="66d87-113">Esta propiedad se aplica a ambos codificadores y descodificadores.</span><span class="sxs-lookup"><span data-stu-id="66d87-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="66d87-114">El modo de baja latencia es útil para las comunicaciones en tiempo real o la captura en directo, cuando se debe minimizar la latencia.</span><span class="sxs-lookup"><span data-stu-id="66d87-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="66d87-115">Sin embargo, el modo de latencia baja también puede reducir la descodificación o la calidad de la codificación.</span><span class="sxs-lookup"><span data-stu-id="66d87-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="66d87-116">Se espera que el codificador no agregue ningún retraso de muestra debido a la reordenación de fotogramas en el proceso de codificación y una muestra de entrada generará un ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="66d87-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="66d87-117">Los segmentos y fotogramas B pueden estar presentes siempre y cuando no presenten ninguna reordenación de fotogramas en el codificador.</span><span class="sxs-lookup"><span data-stu-id="66d87-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d87-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d87-118">Requirements</span></span>



| <span data-ttu-id="66d87-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d87-119">Requirement</span></span> | <span data-ttu-id="66d87-120">Value</span><span class="sxs-lookup"><span data-stu-id="66d87-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66d87-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d87-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66d87-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="66d87-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="66d87-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d87-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66d87-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="66d87-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="66d87-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d87-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d87-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d87-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d87-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d87-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66d87-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="66d87-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="66d87-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

