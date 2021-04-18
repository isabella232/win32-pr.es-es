---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento de la tensores de entrada y escribe el resultado en el tensores de salida.
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
ms.openlocfilehash: 4b292b1b6e12f4643e928022f59603fd75e080fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721256"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="362b6-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="362b6-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="362b6-104">Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento de la tensores de entrada y escribe el resultado en el tensores de salida.</span><span class="sxs-lookup"><span data-stu-id="362b6-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="362b6-105">Los tensores de entrada y salida deben tener los mismos tamaños de *DimensionCount* y *tamaño*, aunque pueden diferir en el *tipo* de datos.</span><span class="sxs-lookup"><span data-stu-id="362b6-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="362b6-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="362b6-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="362b6-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="362b6-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="362b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="362b6-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="362b6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="362b6-109">Members</span></span>

`InputTensor`

<span data-ttu-id="362b6-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="362b6-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="362b6-111">Tensores de entrada del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="362b6-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="362b6-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="362b6-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="362b6-113">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="362b6-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="362b6-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="362b6-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="362b6-115">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="362b6-115">Availability</span></span>
<span data-ttu-id="362b6-116">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="362b6-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="362b6-117">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="362b6-117">Tensor constraints</span></span>
<span data-ttu-id="362b6-118">*InputTensor* y *OutputTensor* deben tener los mismos *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="362b6-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="362b6-119">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="362b6-119">Tensor support</span></span>
| <span data-ttu-id="362b6-120">Tensores</span><span class="sxs-lookup"><span data-stu-id="362b6-120">Tensor</span></span> | <span data-ttu-id="362b6-121">Clase</span><span class="sxs-lookup"><span data-stu-id="362b6-121">Kind</span></span> | <span data-ttu-id="362b6-122">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="362b6-122">Supported dimension counts</span></span> | <span data-ttu-id="362b6-123">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="362b6-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="362b6-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="362b6-124">InputTensor</span></span> | <span data-ttu-id="362b6-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="362b6-125">Input</span></span> | <span data-ttu-id="362b6-126">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="362b6-126">1 to 8</span></span> | <span data-ttu-id="362b6-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="362b6-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="362b6-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="362b6-128">OutputTensor</span></span> | <span data-ttu-id="362b6-129">Output</span><span class="sxs-lookup"><span data-stu-id="362b6-129">Output</span></span> | <span data-ttu-id="362b6-130">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="362b6-130">1 to 8</span></span> | <span data-ttu-id="362b6-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="362b6-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="362b6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="362b6-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="362b6-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="362b6-133">**Header**</span></span> | <span data-ttu-id="362b6-134">directml. h</span><span class="sxs-lookup"><span data-stu-id="362b6-134">directml.h</span></span> |