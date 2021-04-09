---
description: Especifica el método que se va a utilizar para la coincidencia de movimiento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Propiedad MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001630"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="081dd-103">\_Propiedad MOTIONMATCHMETHOD de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="081dd-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="081dd-104">Especifica el método que se va a utilizar para la coincidencia de movimiento.</span><span class="sxs-lookup"><span data-stu-id="081dd-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="081dd-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="081dd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="081dd-106">g \_ wszWMVCMotionMatchMethod</span><span class="sxs-lookup"><span data-stu-id="081dd-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="081dd-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="081dd-107">Data Type</span></span>

<span data-ttu-id="081dd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="081dd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="081dd-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="081dd-109">Default Value</span></span>

<span data-ttu-id="081dd-110">0</span><span class="sxs-lookup"><span data-stu-id="081dd-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="081dd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="081dd-111">Remarks</span></span>

<span data-ttu-id="081dd-112">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="081dd-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="081dd-113">Value</span><span class="sxs-lookup"><span data-stu-id="081dd-113">Value</span></span> | <span data-ttu-id="081dd-114">Método usado</span><span class="sxs-lookup"><span data-stu-id="081dd-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="081dd-115">0</span><span class="sxs-lookup"><span data-stu-id="081dd-115">0</span></span>     | <span data-ttu-id="081dd-116">suma de diferencias absolutas (SAD)</span><span class="sxs-lookup"><span data-stu-id="081dd-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="081dd-117">1</span><span class="sxs-lookup"><span data-stu-id="081dd-117">1</span></span>     | <span data-ttu-id="081dd-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="081dd-118">Hadamard</span></span>                          |
| <span data-ttu-id="081dd-119">-1</span><span class="sxs-lookup"><span data-stu-id="081dd-119">-1</span></span>    | <span data-ttu-id="081dd-120">Adaptativo macrobloque: adaptable.</span><span class="sxs-lookup"><span data-stu-id="081dd-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="081dd-121">La suma de diferencias absolutas (SAD) es un método más rápido pero menos preciso que la transformación Hadamard.</span><span class="sxs-lookup"><span data-stu-id="081dd-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="081dd-122">La transformación Hadamard es más precisa pero es computacionalmente intensiva.</span><span class="sxs-lookup"><span data-stu-id="081dd-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="081dd-123">El modo de adaptación adaptativo macrobloque proporciona un compromiso razonable entre los dos métodos mediante la elección dinámica entre las dos transformaciones y la selección de la transformación Hadamard solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="081dd-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="081dd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="081dd-124">Requirements</span></span>



| <span data-ttu-id="081dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="081dd-125">Requirement</span></span> | <span data-ttu-id="081dd-126">Value</span><span class="sxs-lookup"><span data-stu-id="081dd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="081dd-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="081dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="081dd-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="081dd-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="081dd-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="081dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="081dd-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="081dd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="081dd-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="081dd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="081dd-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="081dd-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="081dd-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="081dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081dd-134">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="081dd-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




