---
description: Especifica el método de costo que usa el códec para determinar qué modo de adaptativo macrobloque debe usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Propiedad MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696940"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="a99eb-103">\_Propiedad MACROBLOCKMODECOSTMETHOD de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a99eb-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="a99eb-104">Especifica el método de costo que usa el códec para determinar qué modo de adaptativo macrobloque debe usar.</span><span class="sxs-lookup"><span data-stu-id="a99eb-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a99eb-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a99eb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a99eb-106">g \_ wszWMVCMacroblockModeCostMethod</span><span class="sxs-lookup"><span data-stu-id="a99eb-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="a99eb-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a99eb-107">Data Type</span></span>

<span data-ttu-id="a99eb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a99eb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a99eb-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a99eb-109">Default Value</span></span>

<span data-ttu-id="a99eb-110">0</span><span class="sxs-lookup"><span data-stu-id="a99eb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a99eb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a99eb-111">Remarks</span></span>

<span data-ttu-id="a99eb-112">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a99eb-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="a99eb-113">Value</span><span class="sxs-lookup"><span data-stu-id="a99eb-113">Value</span></span> | <span data-ttu-id="a99eb-114">Método usado</span><span class="sxs-lookup"><span data-stu-id="a99eb-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a99eb-115">0</span><span class="sxs-lookup"><span data-stu-id="a99eb-115">0</span></span>     | <span data-ttu-id="a99eb-116">SAD/Hadamard.</span><span class="sxs-lookup"><span data-stu-id="a99eb-116">SAD/Hadamard.</span></span> <span data-ttu-id="a99eb-117">Esta opción configura el códec para usar solo la distorsión al calcular el costo.</span><span class="sxs-lookup"><span data-stu-id="a99eb-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="a99eb-118">1</span><span class="sxs-lookup"><span data-stu-id="a99eb-118">1</span></span>     | <span data-ttu-id="a99eb-119">Costo de RD.</span><span class="sxs-lookup"><span data-stu-id="a99eb-119">RD cost.</span></span> <span data-ttu-id="a99eb-120">Esta opción configura el códec para que tenga en cuenta la tasa y la distorsión al calcular el costo.</span><span class="sxs-lookup"><span data-stu-id="a99eb-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a99eb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a99eb-121">Requirements</span></span>



| <span data-ttu-id="a99eb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99eb-122">Requirement</span></span> | <span data-ttu-id="a99eb-123">Value</span><span class="sxs-lookup"><span data-stu-id="a99eb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a99eb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a99eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a99eb-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a99eb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a99eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a99eb-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a99eb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a99eb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a99eb-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a99eb-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a99eb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a99eb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99eb-131">MFPKEY \_ MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="a99eb-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="a99eb-132">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a99eb-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




