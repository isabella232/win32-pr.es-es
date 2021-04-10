---
description: Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Propiedad CODECAPI_AVEncH264SPSID (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153678"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="c380a-103">\_Propiedad AVEncH264SPSID de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="c380a-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="c380a-104">Establece el identificador del conjunto de parámetros de secuencia (SPS) en la unidad de capa de abstracción de red (NAL) de SPS de la secuencia de bits H. 264.</span><span class="sxs-lookup"><span data-stu-id="c380a-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c380a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c380a-105">Data type</span></span>

<span data-ttu-id="c380a-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="c380a-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c380a-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="c380a-107">Property GUID</span></span>

<span data-ttu-id="c380a-108">**CODECAPI \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="c380a-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="c380a-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c380a-109">Property value</span></span>

<span data-ttu-id="c380a-110">Especifica el valor del **\_ identificador de \_ conjunto \_ de parámetros SEQ** en la unidad nal de SPS.</span><span class="sxs-lookup"><span data-stu-id="c380a-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="c380a-111">El elemento de sintaxis **Seq \_ Parameter \_ set \_ ID** identifica el conjunto de parámetros Sequence.</span><span class="sxs-lookup"><span data-stu-id="c380a-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="c380a-112">El flujo de bits resultante se puede concatenar con otros flujos de bits para generar un flujo de bits más largo que contenga varios conjuntos de parámetros de secuencia con distintos identificadores de SPS.</span><span class="sxs-lookup"><span data-stu-id="c380a-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="c380a-113">El intervalo válido es 0 31, tal y como se especifica en la especificación H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="c380a-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="c380a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c380a-114">Requirements</span></span>



| <span data-ttu-id="c380a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c380a-115">Requirement</span></span> | <span data-ttu-id="c380a-116">Value</span><span class="sxs-lookup"><span data-stu-id="c380a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c380a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c380a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c380a-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c380a-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c380a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c380a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c380a-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c380a-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c380a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c380a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c380a-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c380a-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c380a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c380a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c380a-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c380a-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c380a-125">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c380a-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

