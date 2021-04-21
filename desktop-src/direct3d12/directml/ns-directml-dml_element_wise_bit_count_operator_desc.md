---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Calcula el VALOR NOT bit a bit para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.
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
ms.openlocfilehash: 070fc901c006ce1f18429e79eab635a5360c4af7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803236"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="6c10c-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="6c10c-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6c10c-104">Calcula el VALOR NOT bit a bit para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="6c10c-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="6c10c-105">El tensor de entrada y salida debe tener los mismos *valores de DimensionCount,* *Sizes* *y DataType.*</span><span class="sxs-lookup"><span data-stu-id="6c10c-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="6c10c-106">Este operador admite la ejecución en contexto, lo que significa que el tensor de salida puede crear un alias para el tensor de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="6c10c-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c10c-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="6c10c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="6c10c-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="6c10c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c10c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c10c-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="6c10c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c10c-110">Members</span></span>

`InputTensor`

<span data-ttu-id="6c10c-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6c10c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6c10c-112">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="6c10c-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="6c10c-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6c10c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6c10c-114">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="6c10c-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="6c10c-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c10c-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="6c10c-116">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6c10c-116">Availability</span></span>
<span data-ttu-id="6c10c-117">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6c10c-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6c10c-118">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="6c10c-118">Tensor constraints</span></span>
<span data-ttu-id="6c10c-119">*InputTensor* y *OutputTensor* deben tener los mismos *datatype,* *dimensioncount* y *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="6c10c-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6c10c-120">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="6c10c-120">Tensor support</span></span>
| <span data-ttu-id="6c10c-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="6c10c-121">Tensor</span></span> | <span data-ttu-id="6c10c-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c10c-122">Kind</span></span> | <span data-ttu-id="6c10c-123">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="6c10c-123">Supported dimension counts</span></span> | <span data-ttu-id="6c10c-124">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="6c10c-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6c10c-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6c10c-125">InputTensor</span></span> | <span data-ttu-id="6c10c-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c10c-126">Input</span></span> | <span data-ttu-id="6c10c-127">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="6c10c-127">1 to 8</span></span> | <span data-ttu-id="6c10c-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6c10c-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="6c10c-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6c10c-129">OutputTensor</span></span> | <span data-ttu-id="6c10c-130">Resultados</span><span class="sxs-lookup"><span data-stu-id="6c10c-130">Output</span></span> | <span data-ttu-id="6c10c-131">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="6c10c-131">1 to 8</span></span> | <span data-ttu-id="6c10c-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6c10c-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="6c10c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c10c-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6c10c-134">**Header**</span><span class="sxs-lookup"><span data-stu-id="6c10c-134">**Header**</span></span> | <span data-ttu-id="6c10c-135">directml.h</span><span class="sxs-lookup"><span data-stu-id="6c10c-135">directml.h</span></span> |