---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Calcula los degradados de apropagamiento hacia atrás para el [clip por elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804494"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="3fb68-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="3fb68-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="3fb68-104">Calcula los degradados de apropagamiento hacia atrás para el [clip por elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="3fb68-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="3fb68-105">Este operador admite la ejecución en contexto, lo que significa que se `OutputTensor` permite el alias *InputTensor durante* el enlace.</span><span class="sxs-lookup"><span data-stu-id="3fb68-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fb68-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="3fb68-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="3fb68-107">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="3fb68-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb68-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb68-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="3fb68-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fb68-109">Members</span></span>

`InputTensor`

<span data-ttu-id="3fb68-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3fb68-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3fb68-111">Tensor de la característica de entrada.</span><span class="sxs-lookup"><span data-stu-id="3fb68-111">The input feature tensor.</span></span> <span data-ttu-id="3fb68-112">Suele ser el mismo tensor que se proporcionó que *inputTensor* para [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="3fb68-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="3fb68-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3fb68-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3fb68-114">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="3fb68-114">The incoming gradient tensor.</span></span> <span data-ttu-id="3fb68-115">Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="3fb68-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="3fb68-116">Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_OPERATOR_ELEMENT_WISE_CLIP **correspondiente** en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="3fb68-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="3fb68-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3fb68-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3fb68-118">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="3fb68-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="3fb68-119">Normalmente, este tensor tendría los  mismos tamaños que la entrada del DML_OPERATOR_ELEMENT_WISE_CLIP **en** el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="3fb68-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="3fb68-120">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fb68-120">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3fb68-121">Valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="3fb68-121">The minimum value.</span></span> <span data-ttu-id="3fb68-122">Si x está en o por debajo de este valor, el resultado del degradado es 0.</span><span class="sxs-lookup"><span data-stu-id="3fb68-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="3fb68-123">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fb68-123">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3fb68-124">Valor máximo.</span><span class="sxs-lookup"><span data-stu-id="3fb68-124">The maximum value.</span></span> <span data-ttu-id="3fb68-125">Si x está en o por encima de este valor, el resultado del degradado es 0.</span><span class="sxs-lookup"><span data-stu-id="3fb68-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="3fb68-126">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="3fb68-126">Availability</span></span>
<span data-ttu-id="3fb68-127">Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="3fb68-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3fb68-128">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-128">Tensor constraints</span></span>
<span data-ttu-id="3fb68-129">*InputGradientTensor,* *InputTensor* y *OutputGradientTensor* deben tener los mismos *tamaños datatype,* *dimensioncount* *y*.</span><span class="sxs-lookup"><span data-stu-id="3fb68-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3fb68-130">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-130">Tensor support</span></span>
| <span data-ttu-id="3fb68-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-131">Tensor</span></span> | <span data-ttu-id="3fb68-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fb68-132">Kind</span></span> | <span data-ttu-id="3fb68-133">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="3fb68-133">Supported dimension counts</span></span> | <span data-ttu-id="3fb68-134">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="3fb68-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3fb68-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-135">InputTensor</span></span> | <span data-ttu-id="3fb68-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="3fb68-136">Input</span></span> | <span data-ttu-id="3fb68-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="3fb68-137">1 to 8</span></span> | <span data-ttu-id="3fb68-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3fb68-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3fb68-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-139">InputGradientTensor</span></span> | <span data-ttu-id="3fb68-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="3fb68-140">Input</span></span> | <span data-ttu-id="3fb68-141">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="3fb68-141">1 to 8</span></span> | <span data-ttu-id="3fb68-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3fb68-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3fb68-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3fb68-143">OutputGradientTensor</span></span> | <span data-ttu-id="3fb68-144">Resultados</span><span class="sxs-lookup"><span data-stu-id="3fb68-144">Output</span></span> | <span data-ttu-id="3fb68-145">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="3fb68-145">1 to 8</span></span> | <span data-ttu-id="3fb68-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3fb68-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="3fb68-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb68-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3fb68-148">**Header**</span><span class="sxs-lookup"><span data-stu-id="3fb68-148">**Header**</span></span> | <span data-ttu-id="3fb68-149">directml.h</span><span class="sxs-lookup"><span data-stu-id="3fb68-149">directml.h</span></span> |
