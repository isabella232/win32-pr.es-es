---
description: Especifica el tipo de filtro de desacentuación que se debe usar al descodificar. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propiedad AVEncMPAEmphasisType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686358"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="6c03a-104">Propiedad AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="6c03a-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="6c03a-105">Especifica el tipo de filtro de desacentuación que se debe usar al descodificar.</span><span class="sxs-lookup"><span data-stu-id="6c03a-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="6c03a-106">Esta propiedad se aplica a los codificadores de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="6c03a-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="6c03a-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6c03a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c03a-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6c03a-108">Data type</span></span>

<span data-ttu-id="6c03a-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6c03a-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6c03a-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="6c03a-110">Property GUID</span></span>

<span data-ttu-id="6c03a-111">**CODECAPI \_ AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="6c03a-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="6c03a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6c03a-112">Property value</span></span>

<span data-ttu-id="6c03a-113">El valor de esta propiedad es un miembro de la enumeración [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .</span><span class="sxs-lookup"><span data-stu-id="6c03a-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c03a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c03a-114">Remarks</span></span>

<span data-ttu-id="6c03a-115">Esta propiedad establece los bits de énfasis en el encabezado del marco.</span><span class="sxs-lookup"><span data-stu-id="6c03a-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c03a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c03a-116">Requirements</span></span>



| <span data-ttu-id="6c03a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c03a-117">Requirement</span></span> | <span data-ttu-id="6c03a-118">Value</span><span class="sxs-lookup"><span data-stu-id="6c03a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c03a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c03a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c03a-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="6c03a-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6c03a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c03a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c03a-122">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="6c03a-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6c03a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c03a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c03a-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c03a-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c03a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c03a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c03a-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="6c03a-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6c03a-127">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6c03a-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

