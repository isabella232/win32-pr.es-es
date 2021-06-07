---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para una unidad lineal (ReLU) rectificada.
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417946"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="f0cc1-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f0cc1-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f0cc1-104">Calcula los degradados de repropagación para una unidad lineal (ReLU) rectificada.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="f0cc1-105">Este operador realiza el siguiente cálculo por elemento.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="f0cc1-106">El operador forward-pass correspondiente es [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f0cc1-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0cc1-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="f0cc1-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f0cc1-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f0cc1-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0cc1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0cc1-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="f0cc1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0cc1-110">Members</span></span>

`InputTensor`

<span data-ttu-id="f0cc1-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f0cc1-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f0cc1-112">Tensor de entrada (característica).</span><span class="sxs-lookup"><span data-stu-id="f0cc1-112">The input (feature) tensor.</span></span> <span data-ttu-id="f0cc1-113">Esta suele ser la misma entrada que se proporcionó durante el paso hacia delante [(vea DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="f0cc1-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="f0cc1-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f0cc1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f0cc1-115">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-115">The incoming gradient tensor.</span></span> <span data-ttu-id="f0cc1-116">Esto se obtiene normalmente a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="f0cc1-117">Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f0cc1-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="f0cc1-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f0cc1-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f0cc1-119">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="f0cc1-120">Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f0cc1-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="f0cc1-121">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="f0cc1-121">Availability</span></span>
<span data-ttu-id="f0cc1-122">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f0cc1-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f0cc1-123">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-123">Tensor constraints</span></span>
<span data-ttu-id="f0cc1-124">*InputGradientTensor,* *InputTensor* y *OutputGradientTensor* deben tener los mismos *tamaños datatype,* *dimensioncount* *y*.</span><span class="sxs-lookup"><span data-stu-id="f0cc1-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f0cc1-125">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-125">Tensor support</span></span>
| <span data-ttu-id="f0cc1-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-126">Tensor</span></span> | <span data-ttu-id="f0cc1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0cc1-127">Kind</span></span> | <span data-ttu-id="f0cc1-128">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="f0cc1-128">Supported dimension counts</span></span> | <span data-ttu-id="f0cc1-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="f0cc1-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f0cc1-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-130">InputTensor</span></span> | <span data-ttu-id="f0cc1-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cc1-131">Input</span></span> | <span data-ttu-id="f0cc1-132">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f0cc1-132">1 to 8</span></span> | <span data-ttu-id="f0cc1-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f0cc1-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f0cc1-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-134">InputGradientTensor</span></span> | <span data-ttu-id="f0cc1-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cc1-135">Input</span></span> | <span data-ttu-id="f0cc1-136">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f0cc1-136">1 to 8</span></span> | <span data-ttu-id="f0cc1-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f0cc1-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f0cc1-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f0cc1-138">OutputGradientTensor</span></span> | <span data-ttu-id="f0cc1-139">Resultados</span><span class="sxs-lookup"><span data-stu-id="f0cc1-139">Output</span></span> | <span data-ttu-id="f0cc1-140">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f0cc1-140">1 to 8</span></span> | <span data-ttu-id="f0cc1-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f0cc1-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="f0cc1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0cc1-142">See also</span></span>
[<span data-ttu-id="f0cc1-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="f0cc1-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="f0cc1-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0cc1-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f0cc1-145">**Header**</span><span class="sxs-lookup"><span data-stu-id="f0cc1-145">**Header**</span></span> | <span data-ttu-id="f0cc1-146">directml.h</span><span class="sxs-lookup"><span data-stu-id="f0cc1-146">directml.h</span></span> |