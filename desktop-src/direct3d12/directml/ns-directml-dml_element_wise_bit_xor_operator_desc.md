---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Calcula la operación XOR bit a bit (Exclusive o) entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: 73a811448b7c2b7839afd6e926acb0bf04a2ff44
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721230"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="fe6bb-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fe6bb-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fe6bb-104">Calcula la operación XOR bit a bit (Exclusive o) entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="fe6bb-105">Los tensores de entrada y salida deben tener los mismos *DimensionCount*, *tamaños* y *tipo* de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="fe6bb-106">Este operador admite la ejecución en contexto, lo que significa que el tensores de salida tiene permiso para asignar alias a uno o varios de los decenas de entradas durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe6bb-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="fe6bb-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fe6bb-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fe6bb-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6bb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe6bb-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="fe6bb-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe6bb-110">Members</span></span>

`ATensor`

<span data-ttu-id="fe6bb-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe6bb-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe6bb-112">Un tensores que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="fe6bb-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe6bb-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe6bb-114">Un tensores que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="fe6bb-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe6bb-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe6bb-116">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="fe6bb-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe6bb-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="fe6bb-118">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="fe6bb-118">Availability</span></span>
<span data-ttu-id="fe6bb-119">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="fe6bb-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fe6bb-120">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="fe6bb-120">Tensor constraints</span></span>
<span data-ttu-id="fe6bb-121">*ATensor*, *BTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="fe6bb-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fe6bb-122">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="fe6bb-122">Tensor support</span></span>
| <span data-ttu-id="fe6bb-123">Tensores</span><span class="sxs-lookup"><span data-stu-id="fe6bb-123">Tensor</span></span> | <span data-ttu-id="fe6bb-124">Clase</span><span class="sxs-lookup"><span data-stu-id="fe6bb-124">Kind</span></span> | <span data-ttu-id="fe6bb-125">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="fe6bb-125">Supported dimension counts</span></span> | <span data-ttu-id="fe6bb-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="fe6bb-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe6bb-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="fe6bb-127">ATensor</span></span> | <span data-ttu-id="fe6bb-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe6bb-128">Input</span></span> | <span data-ttu-id="fe6bb-129">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-129">1 to 8</span></span> | <span data-ttu-id="fe6bb-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe6bb-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="fe6bb-131">BTensor</span></span> | <span data-ttu-id="fe6bb-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe6bb-132">Input</span></span> | <span data-ttu-id="fe6bb-133">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-133">1 to 8</span></span> | <span data-ttu-id="fe6bb-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe6bb-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fe6bb-135">OutputTensor</span></span> | <span data-ttu-id="fe6bb-136">Output</span><span class="sxs-lookup"><span data-stu-id="fe6bb-136">Output</span></span> | <span data-ttu-id="fe6bb-137">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-137">1 to 8</span></span> | <span data-ttu-id="fe6bb-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe6bb-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="fe6bb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6bb-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe6bb-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="fe6bb-140">**Header**</span></span> | <span data-ttu-id="fe6bb-141">directml. h</span><span class="sxs-lookup"><span data-stu-id="fe6bb-141">directml.h</span></span> |