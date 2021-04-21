---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Calcula el XOR bit a bit (eXclusive OR) entre cada elemento correspondiente de los tensores de entrada y escribe el resultado en el tensor de salida.
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
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803192"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="e98fc-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e98fc-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e98fc-104">Calcula el XOR bit a bit (eXclusive OR) entre cada elemento correspondiente de los tensores de entrada y escribe el resultado en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="e98fc-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="e98fc-105">El tensor de entrada y salida debe tener los mismos *DimensionCount,* *Sizes* y *DataType.*</span><span class="sxs-lookup"><span data-stu-id="e98fc-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="e98fc-106">Este operador admite la ejecución en contexto, lo que significa que el tensor de salida puede crear un alias de uno o varios de los tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="e98fc-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e98fc-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="e98fc-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e98fc-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e98fc-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e98fc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e98fc-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e98fc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e98fc-110">Members</span></span>

`ATensor`

<span data-ttu-id="e98fc-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e98fc-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e98fc-112">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="e98fc-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="e98fc-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e98fc-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e98fc-114">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="e98fc-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="e98fc-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e98fc-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e98fc-116">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="e98fc-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="e98fc-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e98fc-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="e98fc-118">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e98fc-118">Availability</span></span>
<span data-ttu-id="e98fc-119">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e98fc-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e98fc-120">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-120">Tensor constraints</span></span>
<span data-ttu-id="e98fc-121">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *tamaños DataType,* *DimensionCount* y *.*</span><span class="sxs-lookup"><span data-stu-id="e98fc-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e98fc-122">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-122">Tensor support</span></span>
| <span data-ttu-id="e98fc-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-123">Tensor</span></span> | <span data-ttu-id="e98fc-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e98fc-124">Kind</span></span> | <span data-ttu-id="e98fc-125">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="e98fc-125">Supported dimension counts</span></span> | <span data-ttu-id="e98fc-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e98fc-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e98fc-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-127">ATensor</span></span> | <span data-ttu-id="e98fc-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98fc-128">Input</span></span> | <span data-ttu-id="e98fc-129">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e98fc-129">1 to 8</span></span> | <span data-ttu-id="e98fc-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e98fc-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e98fc-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-131">BTensor</span></span> | <span data-ttu-id="e98fc-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98fc-132">Input</span></span> | <span data-ttu-id="e98fc-133">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e98fc-133">1 to 8</span></span> | <span data-ttu-id="e98fc-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e98fc-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e98fc-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e98fc-135">OutputTensor</span></span> | <span data-ttu-id="e98fc-136">Resultados</span><span class="sxs-lookup"><span data-stu-id="e98fc-136">Output</span></span> | <span data-ttu-id="e98fc-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e98fc-137">1 to 8</span></span> | <span data-ttu-id="e98fc-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e98fc-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="e98fc-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e98fc-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e98fc-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="e98fc-140">**Header**</span></span> | <span data-ttu-id="e98fc-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="e98fc-141">directml.h</span></span> |