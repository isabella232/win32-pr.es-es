---
description: Especifica el método utilizado para codificar la información del vector de movimiento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Propiedad MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544926"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="bcf64-103">\_Propiedad DELTAMVRANGEINDEX de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="bcf64-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="bcf64-104">Especifica el método utilizado para codificar la información del vector de movimiento.</span><span class="sxs-lookup"><span data-stu-id="bcf64-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bcf64-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="bcf64-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="bcf64-106">g \_ wszWMVCDeltaMVRangeIndex</span><span class="sxs-lookup"><span data-stu-id="bcf64-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="bcf64-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bcf64-107">Data Type</span></span>

<span data-ttu-id="bcf64-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="bcf64-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="bcf64-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bcf64-109">Default Value</span></span>

<span data-ttu-id="bcf64-110">0</span><span class="sxs-lookup"><span data-stu-id="bcf64-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf64-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcf64-111">Remarks</span></span>

<span data-ttu-id="bcf64-112">Si se establece esta propiedad, el codificador aumenta el intervalo de vector de movimiento Delta en los campos.</span><span class="sxs-lookup"><span data-stu-id="bcf64-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="bcf64-113">La información del vector de movimiento solo es válida para los campos entrelazados.</span><span class="sxs-lookup"><span data-stu-id="bcf64-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="bcf64-114">Esta propiedad se puede establecer en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="bcf64-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="bcf64-115">Value</span><span class="sxs-lookup"><span data-stu-id="bcf64-115">Value</span></span> | <span data-ttu-id="bcf64-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcf64-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf64-117">0</span><span class="sxs-lookup"><span data-stu-id="bcf64-117">0</span></span>     | <span data-ttu-id="bcf64-118">Use el intervalo de vector de movimiento Delta existente.</span><span class="sxs-lookup"><span data-stu-id="bcf64-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="bcf64-119">1</span><span class="sxs-lookup"><span data-stu-id="bcf64-119">1</span></span>     | <span data-ttu-id="bcf64-120">Doble el intervalo del vector de movimiento Delta en la dirección horizontal.</span><span class="sxs-lookup"><span data-stu-id="bcf64-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="bcf64-121">2</span><span class="sxs-lookup"><span data-stu-id="bcf64-121">2</span></span>     | <span data-ttu-id="bcf64-122">Duplique el intervalo del vector de movimiento Delta en dirección vertical.</span><span class="sxs-lookup"><span data-stu-id="bcf64-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="bcf64-123">3</span><span class="sxs-lookup"><span data-stu-id="bcf64-123">3</span></span>     | <span data-ttu-id="bcf64-124">Duplique el intervalo del vector de movimiento Delta en las direcciones horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="bcf64-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bcf64-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf64-125">Requirements</span></span>



| <span data-ttu-id="bcf64-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf64-126">Requirement</span></span> | <span data-ttu-id="bcf64-127">Value</span><span class="sxs-lookup"><span data-stu-id="bcf64-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf64-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf64-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bcf64-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bcf64-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf64-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcf64-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcf64-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcf64-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf64-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf64-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf64-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcf64-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf64-135">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcf64-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




