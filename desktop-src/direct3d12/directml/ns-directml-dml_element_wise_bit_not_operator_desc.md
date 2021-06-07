---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 3c8dddc3159ebcd857c7423b76856fbeba465d2e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417998"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="039e3-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="039e3-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="039e3-104">Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="039e3-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="039e3-105">El tensor de entrada y salida debe tener los mismos *dimensioncount* y *sizes,* aunque pueden diferir *en DataType.*</span><span class="sxs-lookup"><span data-stu-id="039e3-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="039e3-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="039e3-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="039e3-107">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="039e3-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="039e3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="039e3-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="039e3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="039e3-109">Members</span></span>

`InputTensor`

<span data-ttu-id="039e3-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="039e3-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="039e3-111">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="039e3-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="039e3-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="039e3-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="039e3-113">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="039e3-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="039e3-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="039e3-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="039e3-115">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="039e3-115">Availability</span></span>
<span data-ttu-id="039e3-116">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="039e3-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="039e3-117">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="039e3-117">Tensor constraints</span></span>
<span data-ttu-id="039e3-118">*InputTensor* y *OutputTensor* deben tener los mismos *dimensioncount* y *sizes.*</span><span class="sxs-lookup"><span data-stu-id="039e3-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="039e3-119">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="039e3-119">Tensor support</span></span>
| <span data-ttu-id="039e3-120">Tensor</span><span class="sxs-lookup"><span data-stu-id="039e3-120">Tensor</span></span> | <span data-ttu-id="039e3-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="039e3-121">Kind</span></span> | <span data-ttu-id="039e3-122">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="039e3-122">Supported dimension counts</span></span> | <span data-ttu-id="039e3-123">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="039e3-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="039e3-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="039e3-124">InputTensor</span></span> | <span data-ttu-id="039e3-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="039e3-125">Input</span></span> | <span data-ttu-id="039e3-126">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="039e3-126">1 to 8</span></span> | <span data-ttu-id="039e3-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="039e3-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="039e3-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="039e3-128">OutputTensor</span></span> | <span data-ttu-id="039e3-129">Resultados</span><span class="sxs-lookup"><span data-stu-id="039e3-129">Output</span></span> | <span data-ttu-id="039e3-130">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="039e3-130">1 to 8</span></span> | <span data-ttu-id="039e3-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="039e3-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="039e3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="039e3-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="039e3-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="039e3-133">**Header**</span></span> | <span data-ttu-id="039e3-134">directml.h</span><span class="sxs-lookup"><span data-stu-id="039e3-134">directml.h</span></span> |