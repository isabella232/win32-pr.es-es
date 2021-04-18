---
description: Especifica si el audio de 2 canales se codifica como estéreo o dual mono.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propiedad AVEncAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666147"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="d3596-103">Propiedad AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="d3596-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="d3596-104">Especifica si el audio de 2 canales se codifica como estéreo o dual mono.</span><span class="sxs-lookup"><span data-stu-id="d3596-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="d3596-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d3596-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d3596-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d3596-106">Data type</span></span>

<span data-ttu-id="d3596-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d3596-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d3596-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="d3596-108">Property GUID</span></span>

<span data-ttu-id="d3596-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="d3596-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="d3596-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d3596-110">Property value</span></span>

<span data-ttu-id="d3596-111">El valor de esta propiedad es un miembro de la enumeración [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="d3596-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3596-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3596-112">Remarks</span></span>

<span data-ttu-id="d3596-113">Esta propiedad no se aplica a los codificadores de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="d3596-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="d3596-114">Para MPEG Audio, use la propiedad [**AVEncMPACodingMode**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d3596-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3596-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3596-115">Requirements</span></span>



| <span data-ttu-id="d3596-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3596-116">Requirement</span></span> | <span data-ttu-id="d3596-117">Value</span><span class="sxs-lookup"><span data-stu-id="d3596-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3596-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3596-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3596-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="d3596-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d3596-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3596-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3596-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="d3596-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d3596-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3596-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3596-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3596-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3596-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3596-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3596-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="d3596-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d3596-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d3596-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

