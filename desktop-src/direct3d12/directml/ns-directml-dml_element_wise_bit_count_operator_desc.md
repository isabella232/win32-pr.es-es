---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Calcula la operación NOT bit a bit para cada elemento de la tensores de entrada y escribe el resultado en el tensores de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721257"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="5661d-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5661d-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5661d-104">Calcula la operación NOT bit a bit para cada elemento de la tensores de entrada y escribe el resultado en el tensores de salida.</span><span class="sxs-lookup"><span data-stu-id="5661d-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="5661d-105">Los tensores de entrada y salida deben tener los mismos *DimensionCount*, *tamaños* y *tipo* de datos.</span><span class="sxs-lookup"><span data-stu-id="5661d-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="5661d-106">Este operador admite la ejecución en contexto, lo que significa que el tensores de salida tiene permiso para asignar un alias a la tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="5661d-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5661d-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="5661d-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5661d-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5661d-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5661d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5661d-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="5661d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5661d-110">Members</span></span>

`InputTensor`

<span data-ttu-id="5661d-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5661d-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5661d-112">Tensores de entrada del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="5661d-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="5661d-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5661d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5661d-114">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="5661d-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="5661d-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5661d-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="5661d-116">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5661d-116">Availability</span></span>
<span data-ttu-id="5661d-117">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5661d-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5661d-118">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="5661d-118">Tensor constraints</span></span>
<span data-ttu-id="5661d-119">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="5661d-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5661d-120">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="5661d-120">Tensor support</span></span>
| <span data-ttu-id="5661d-121">Tensores</span><span class="sxs-lookup"><span data-stu-id="5661d-121">Tensor</span></span> | <span data-ttu-id="5661d-122">Clase</span><span class="sxs-lookup"><span data-stu-id="5661d-122">Kind</span></span> | <span data-ttu-id="5661d-123">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="5661d-123">Supported dimension counts</span></span> | <span data-ttu-id="5661d-124">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="5661d-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5661d-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5661d-125">InputTensor</span></span> | <span data-ttu-id="5661d-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="5661d-126">Input</span></span> | <span data-ttu-id="5661d-127">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5661d-127">1 to 8</span></span> | <span data-ttu-id="5661d-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5661d-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5661d-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5661d-129">OutputTensor</span></span> | <span data-ttu-id="5661d-130">Output</span><span class="sxs-lookup"><span data-stu-id="5661d-130">Output</span></span> | <span data-ttu-id="5661d-131">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5661d-131">1 to 8</span></span> | <span data-ttu-id="5661d-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5661d-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5661d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5661d-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5661d-134">**Header**</span><span class="sxs-lookup"><span data-stu-id="5661d-134">**Header**</span></span> | <span data-ttu-id="5661d-135">directml. h</span><span class="sxs-lookup"><span data-stu-id="5661d-135">directml.h</span></span> |