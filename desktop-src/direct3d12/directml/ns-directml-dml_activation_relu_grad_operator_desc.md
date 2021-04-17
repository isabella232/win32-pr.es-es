---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de una unidad lineal rectificada (ReLU).
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
ms.openlocfilehash: 567a1de50c1c91de83a9fda2978f83af8daf1a6e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721239"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="7c7f7-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7c7f7-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="7c7f7-104">Calcula los degradados de propagación de una unidad lineal rectificada (ReLU).</span><span class="sxs-lookup"><span data-stu-id="7c7f7-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="7c7f7-105">Este operador realiza el siguiente cálculo de elemento.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="7c7f7-106">El operador de paso adelante correspondiente es [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="7c7f7-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c7f7-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="7c7f7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="7c7f7-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7c7f7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7f7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c7f7-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="7c7f7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c7f7-110">Members</span></span>

`InputTensor`

<span data-ttu-id="7c7f7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7c7f7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7c7f7-112">La entrada (característica) tensores.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-112">The input (feature) tensor.</span></span> <span data-ttu-id="7c7f7-113">Normalmente, se trata de la misma entrada que se proporcionó durante el paso adelante (vea [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="7c7f7-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="7c7f7-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7c7f7-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7c7f7-115">Tensores de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-115">The incoming gradient tensor.</span></span> <span data-ttu-id="7c7f7-116">Normalmente se obtiene a partir de la salida de la propagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="7c7f7-117">Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="7c7f7-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7c7f7-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7c7f7-119">Tensores de salida que contiene los degradados retropagados.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="7c7f7-120">Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="7c7f7-121">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="7c7f7-121">Availability</span></span>
<span data-ttu-id="7c7f7-122">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="7c7f7-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7c7f7-123">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="7c7f7-123">Tensor constraints</span></span>
<span data-ttu-id="7c7f7-124">*InputGradientTensor*, *InputTensor* y *OutputGradientTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="7c7f7-125">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="7c7f7-125">Tensor support</span></span>
| <span data-ttu-id="7c7f7-126">Tensores</span><span class="sxs-lookup"><span data-stu-id="7c7f7-126">Tensor</span></span> | <span data-ttu-id="7c7f7-127">Clase</span><span class="sxs-lookup"><span data-stu-id="7c7f7-127">Kind</span></span> | <span data-ttu-id="7c7f7-128">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="7c7f7-128">Supported dimension counts</span></span> | <span data-ttu-id="7c7f7-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="7c7f7-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="7c7f7-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="7c7f7-130">InputTensor</span></span> | <span data-ttu-id="7c7f7-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c7f7-131">Input</span></span> | <span data-ttu-id="7c7f7-132">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="7c7f7-132">1 to 8</span></span> | <span data-ttu-id="7c7f7-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7c7f7-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="7c7f7-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="7c7f7-134">InputGradientTensor</span></span> | <span data-ttu-id="7c7f7-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c7f7-135">Input</span></span> | <span data-ttu-id="7c7f7-136">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="7c7f7-136">1 to 8</span></span> | <span data-ttu-id="7c7f7-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7c7f7-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="7c7f7-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="7c7f7-138">OutputGradientTensor</span></span> | <span data-ttu-id="7c7f7-139">Output</span><span class="sxs-lookup"><span data-stu-id="7c7f7-139">Output</span></span> | <span data-ttu-id="7c7f7-140">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="7c7f7-140">1 to 8</span></span> | <span data-ttu-id="7c7f7-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7c7f7-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="7c7f7-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c7f7-142">See also</span></span>
[<span data-ttu-id="7c7f7-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="7c7f7-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="7c7f7-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c7f7-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7c7f7-145">**Header**</span><span class="sxs-lookup"><span data-stu-id="7c7f7-145">**Header**</span></span> | <span data-ttu-id="7c7f7-146">directml. h</span><span class="sxs-lookup"><span data-stu-id="7c7f7-146">directml.h</span></span> |