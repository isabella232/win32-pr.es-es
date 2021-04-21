---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Realiza la función de activación de unidad lineal exponencial (CELU) que se diferencia continuamente en cada elemento de *InputTensor,* colocando el resultado en el elemento correspondiente de *OutputTensor*.
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
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803728"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="8f755-103">DML_ACTIVATION_CELU_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="8f755-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8f755-104">Realiza la función de activación de unidad lineal exponencial (CELU) que se diferencia continuamente en cada elemento de *InputTensor,* colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8f755-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="8f755-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="8f755-105">Where:</span></span>
* <span data-ttu-id="8f755-106">exp(x) es la función de exponenciación natural</span><span class="sxs-lookup"><span data-stu-id="8f755-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="8f755-107">max(a,b) devuelve el mayor de los dos valores a,b</span><span class="sxs-lookup"><span data-stu-id="8f755-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="8f755-108">min(a,b) devuelve el menor de los dos valores a,b</span><span class="sxs-lookup"><span data-stu-id="8f755-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="8f755-109">Este operador admite la ejecución en contexto, lo que significa que el tensor de salida puede usar el alias *InputTensor durante* el enlace.</span><span class="sxs-lookup"><span data-stu-id="8f755-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f755-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="8f755-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8f755-111">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="8f755-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f755-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f755-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="8f755-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f755-113">Members</span></span>

`InputTensor`

<span data-ttu-id="8f755-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f755-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f755-115">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="8f755-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="8f755-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f755-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f755-117">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="8f755-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="8f755-118">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="8f755-118">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="8f755-119">Coeficiente alfa.</span><span class="sxs-lookup"><span data-stu-id="8f755-119">The alpha coefficient.</span></span> <span data-ttu-id="8f755-120">Un valor predeterminado típico para este valor es 1.0.</span><span class="sxs-lookup"><span data-stu-id="8f755-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="8f755-121">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="8f755-121">Availability</span></span>
<span data-ttu-id="8f755-122">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="8f755-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8f755-123">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="8f755-123">Tensor constraints</span></span>
<span data-ttu-id="8f755-124">*InputTensor* y *OutputTensor* deben tener los mismos *valores de DataType,* *DimensionCount* y *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="8f755-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8f755-125">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="8f755-125">Tensor support</span></span>
| <span data-ttu-id="8f755-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="8f755-126">Tensor</span></span> | <span data-ttu-id="8f755-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f755-127">Kind</span></span> | <span data-ttu-id="8f755-128">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="8f755-128">Supported Dimension Counts</span></span> | <span data-ttu-id="8f755-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="8f755-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8f755-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8f755-130">InputTensor</span></span> | <span data-ttu-id="8f755-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f755-131">Input</span></span> | <span data-ttu-id="8f755-132">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="8f755-132">1 to 8</span></span> | <span data-ttu-id="8f755-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8f755-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8f755-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8f755-134">OutputTensor</span></span> | <span data-ttu-id="8f755-135">Resultados</span><span class="sxs-lookup"><span data-stu-id="8f755-135">Output</span></span> | <span data-ttu-id="8f755-136">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="8f755-136">1 to 8</span></span> | <span data-ttu-id="8f755-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8f755-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="8f755-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f755-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8f755-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="8f755-139">**Header**</span></span> | <span data-ttu-id="8f755-140">directml.h</span><span class="sxs-lookup"><span data-stu-id="8f755-140">directml.h</span></span> |