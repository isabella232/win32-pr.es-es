---
description: Especifica el tipo de habitación de una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propiedad AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152562"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="8d9f8-104">Propiedad AVEncDDProductionRoomType</span><span class="sxs-lookup"><span data-stu-id="8d9f8-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="8d9f8-105">Especifica el tipo de habitación de una secuencia de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="8d9f8-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="8d9f8-106">Esta propiedad se aplica a los codificadores de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="8d9f8-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="8d9f8-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8d9f8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8d9f8-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8d9f8-108">Data type</span></span>

<span data-ttu-id="8d9f8-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8d9f8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8d9f8-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d9f8-110">Property GUID</span></span>

<span data-ttu-id="8d9f8-111">**CODECAPI \_ AVEncDDProductionRoomType**</span><span class="sxs-lookup"><span data-stu-id="8d9f8-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="8d9f8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d9f8-112">Property value</span></span>

<span data-ttu-id="8d9f8-113">El valor de esta propiedad es un miembro de la enumeración [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .</span><span class="sxs-lookup"><span data-stu-id="8d9f8-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9f8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d9f8-114">Remarks</span></span>

<span data-ttu-id="8d9f8-115">*Tipo de sala* hace referencia al tamaño de la habitación utilizada durante la producción.</span><span class="sxs-lookup"><span data-stu-id="8d9f8-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="8d9f8-116">Si establece esta propiedad, establezca la propiedad [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="8d9f8-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9f8-117">Requirements</span></span>



| <span data-ttu-id="8d9f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9f8-118">Requirement</span></span> | <span data-ttu-id="8d9f8-119">Value</span><span class="sxs-lookup"><span data-stu-id="8d9f8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9f8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9f8-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="8d9f8-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8d9f8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9f8-123">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="8d9f8-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8d9f8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d9f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9f8-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f8-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9f8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d9f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9f8-127">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="8d9f8-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8d9f8-128">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8d9f8-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

