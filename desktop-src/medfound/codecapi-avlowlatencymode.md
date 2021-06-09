---
description: Habilita el modo de baja latencia en un códec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826909"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="2b8d6-103">Propiedad CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="2b8d6-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="2b8d6-104">Habilita el modo de baja latencia en un códec.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b8d6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2b8d6-105">Data type</span></span>

<span data-ttu-id="2b8d6-106">**ULONG** (**VT \_ BOOL**)</span><span class="sxs-lookup"><span data-stu-id="2b8d6-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2b8d6-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b8d6-107">Property GUID</span></span>

<span data-ttu-id="2b8d6-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="2b8d6-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="2b8d6-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b8d6-109">Property value</span></span>

<span data-ttu-id="2b8d6-110">Si el valor es distinto de cero, se habilita el modo de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="2b8d6-111">Si el valor es cero, el modo de baja latencia está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8d6-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b8d6-112">Remarks</span></span>

<span data-ttu-id="2b8d6-113">Esta propiedad se aplica tanto a los codificadores como a los descodificadores.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="2b8d6-114">El modo de baja latencia es útil para las comunicaciones en tiempo real o la captura en vivo, cuando se debe minimizar la latencia.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="2b8d6-115">Sin embargo, el modo de baja latencia también puede reducir la calidad de la codificación o la codificación.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="2b8d6-116">Se espera que el codificador no agregue ningún retraso de muestra debido a la reordenación de fotogramas en el proceso de codificación y que una muestra de entrada produzca una muestra de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="2b8d6-117">Los segmentos o fotogramas B pueden estar presentes siempre y cuando no introduzcan ninguna reordenación de fotogramas en el codificador.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="2b8d6-118">En la implementación actual, el descodificador Media Foundation H.264 usa el tipo **VT_UI4** para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="2b8d6-119">Todas las demás implementaciones, incluido el codificador H.264, usan el tipo **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="2b8d6-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8d6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8d6-120">Requirements</span></span>



| <span data-ttu-id="2b8d6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8d6-121">Requirement</span></span> | <span data-ttu-id="2b8d6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2b8d6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8d6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8d6-124">Windows 8 aplicaciones \[ de escritorio \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b8d6-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="2b8d6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8d6-126">Aplicaciones de escritorio de Windows Server 2012 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b8d6-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2b8d6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b8d6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b8d6-128"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d6-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8d6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8d6-130">Media Foundation propiedades</span><span class="sxs-lookup"><span data-stu-id="2b8d6-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2b8d6-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2b8d6-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

