---
UID: NS:directml.DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
description: Calcula la operación and bit a bit entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.openlocfilehash: 9e8730eef1b2d98c2f3094fb2fa29ecfc571d877
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721305"
---
# <a name="dml_element_wise_bit_and_operator_desc-structure-directmlh"></a><span data-ttu-id="340a5-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="340a5-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="340a5-104">Calcula la operación and bit a bit entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.</span><span class="sxs-lookup"><span data-stu-id="340a5-104">Computes the bitwise AND between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="340a5-105">Los tensores de entrada y salida deben tener los mismos *DimensionCount*, *tamaños* y *tipo* de datos.</span><span class="sxs-lookup"><span data-stu-id="340a5-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="340a5-106">Este operador admite la ejecución en contexto, lo que significa que el tensores de salida tiene permiso para asignar alias a uno o varios de los decenas de entradas durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="340a5-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="340a5-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="340a5-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="340a5-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="340a5-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="340a5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="340a5-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="340a5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="340a5-110">Members</span></span>

`ATensor`

<span data-ttu-id="340a5-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="340a5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="340a5-112">Un tensores que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="340a5-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="340a5-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="340a5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="340a5-114">Un tensores que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="340a5-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="340a5-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="340a5-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="340a5-116">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="340a5-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="340a5-117">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="340a5-117">Availability</span></span>
<span data-ttu-id="340a5-118">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="340a5-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="340a5-119">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="340a5-119">Tensor constraints</span></span>
<span data-ttu-id="340a5-120">*ATensor*, *BTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="340a5-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="340a5-121">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="340a5-121">Tensor support</span></span>
| <span data-ttu-id="340a5-122">Tensores</span><span class="sxs-lookup"><span data-stu-id="340a5-122">Tensor</span></span> | <span data-ttu-id="340a5-123">Clase</span><span class="sxs-lookup"><span data-stu-id="340a5-123">Kind</span></span> | <span data-ttu-id="340a5-124">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="340a5-124">Supported dimension counts</span></span> | <span data-ttu-id="340a5-125">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="340a5-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="340a5-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="340a5-126">ATensor</span></span> | <span data-ttu-id="340a5-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="340a5-127">Input</span></span> | <span data-ttu-id="340a5-128">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="340a5-128">1 to 8</span></span> | <span data-ttu-id="340a5-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="340a5-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="340a5-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="340a5-130">BTensor</span></span> | <span data-ttu-id="340a5-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="340a5-131">Input</span></span> | <span data-ttu-id="340a5-132">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="340a5-132">1 to 8</span></span> | <span data-ttu-id="340a5-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="340a5-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="340a5-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="340a5-134">OutputTensor</span></span> | <span data-ttu-id="340a5-135">Output</span><span class="sxs-lookup"><span data-stu-id="340a5-135">Output</span></span> | <span data-ttu-id="340a5-136">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="340a5-136">1 to 8</span></span> | <span data-ttu-id="340a5-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="340a5-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="340a5-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="340a5-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="340a5-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="340a5-139">**Header**</span></span> | <span data-ttu-id="340a5-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="340a5-140">directml.h</span></span> |