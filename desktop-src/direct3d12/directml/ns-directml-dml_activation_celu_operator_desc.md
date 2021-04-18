---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Realiza la función de activación de la unidad lineal exponencial (CELU) continuamente diferenciable en todos los elementos de *InputTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721216"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="035ba-103">DML_ACTIVATION_CELU_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="035ba-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="035ba-104">Realiza la función de activación de la unidad lineal exponencial (CELU) continuamente diferenciable en todos los elementos de *InputTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="035ba-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="035ba-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="035ba-105">Where:</span></span>
* <span data-ttu-id="035ba-106">exp (x) es la función de exponenciación natural</span><span class="sxs-lookup"><span data-stu-id="035ba-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="035ba-107">Max (a, b) devuelve el mayor de los dos valores a, b</span><span class="sxs-lookup"><span data-stu-id="035ba-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="035ba-108">min (a, b) devuelve el menor de los dos valores a, b</span><span class="sxs-lookup"><span data-stu-id="035ba-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="035ba-109">Este operador es compatible con la ejecución en contexto, lo que significa que el tensores de salida está permitido para el alias *InputTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="035ba-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="035ba-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="035ba-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="035ba-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="035ba-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="035ba-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="035ba-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="035ba-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="035ba-113">Members</span></span>

`InputTensor`

<span data-ttu-id="035ba-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="035ba-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="035ba-115">Tensores de entrada del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="035ba-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="035ba-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="035ba-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="035ba-117">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="035ba-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="035ba-118">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="035ba-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="035ba-119">Coeficiente alfa.</span><span class="sxs-lookup"><span data-stu-id="035ba-119">The alpha coefficient.</span></span> <span data-ttu-id="035ba-120">Un valor predeterminado típico para este valor es 1,0.</span><span class="sxs-lookup"><span data-stu-id="035ba-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="035ba-121">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="035ba-121">Availability</span></span>
<span data-ttu-id="035ba-122">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="035ba-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="035ba-123">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="035ba-123">Tensor constraints</span></span>
<span data-ttu-id="035ba-124">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="035ba-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="035ba-125">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="035ba-125">Tensor support</span></span>
| <span data-ttu-id="035ba-126">Tensores</span><span class="sxs-lookup"><span data-stu-id="035ba-126">Tensor</span></span> | <span data-ttu-id="035ba-127">Clase</span><span class="sxs-lookup"><span data-stu-id="035ba-127">Kind</span></span> | <span data-ttu-id="035ba-128">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="035ba-128">Supported Dimension Counts</span></span> | <span data-ttu-id="035ba-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="035ba-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="035ba-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="035ba-130">InputTensor</span></span> | <span data-ttu-id="035ba-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="035ba-131">Input</span></span> | <span data-ttu-id="035ba-132">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="035ba-132">1 to 8</span></span> | <span data-ttu-id="035ba-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="035ba-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="035ba-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="035ba-134">OutputTensor</span></span> | <span data-ttu-id="035ba-135">Output</span><span class="sxs-lookup"><span data-stu-id="035ba-135">Output</span></span> | <span data-ttu-id="035ba-136">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="035ba-136">1 to 8</span></span> | <span data-ttu-id="035ba-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="035ba-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="035ba-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="035ba-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="035ba-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="035ba-139">**Header**</span></span> | <span data-ttu-id="035ba-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="035ba-140">directml.h</span></span> |