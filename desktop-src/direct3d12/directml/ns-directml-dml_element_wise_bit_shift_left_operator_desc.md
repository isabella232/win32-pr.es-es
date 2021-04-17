---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
description: Realiza un desplazamiento lógico a la izquierda de cada elemento de *ATensor* por un número de bits proporcionado por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_left_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.openlocfilehash: 24f58a5c235b6d67ca2dee712398dacc828d8f51
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721287"
---
# <a name="dml_element_wise_bit_shift_left_operator_desc-structure-directmlh"></a><span data-ttu-id="e3785-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e3785-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e3785-104">Realiza un desplazamiento lógico a la izquierda de cada elemento de *ATensor* por un número de bits proporcionado por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e3785-104">Performs a logical left shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a << b)
```

<span data-ttu-id="e3785-105">Este operador admite la ejecución en contexto, lo que significa que se permite que *OutputTensor* alias a uno de los decenas de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="e3785-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3785-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="e3785-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e3785-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e3785-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3785-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3785-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="e3785-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3785-109">Members</span></span>

`ATensor`

<span data-ttu-id="e3785-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3785-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3785-111">Un tensores que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="e3785-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="e3785-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3785-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3785-113">Un tensores que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="e3785-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="e3785-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3785-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3785-115">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="e3785-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e3785-116">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e3785-116">Availability</span></span>
<span data-ttu-id="e3785-117">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e3785-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e3785-118">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="e3785-118">Tensor constraints</span></span>
<span data-ttu-id="e3785-119">*ATensor*, *BTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="e3785-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e3785-120">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="e3785-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="e3785-121">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e3785-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="e3785-122">Tensores</span><span class="sxs-lookup"><span data-stu-id="e3785-122">Tensor</span></span> | <span data-ttu-id="e3785-123">Clase</span><span class="sxs-lookup"><span data-stu-id="e3785-123">Kind</span></span> | <span data-ttu-id="e3785-124">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="e3785-124">Supported dimension counts</span></span> | <span data-ttu-id="e3785-125">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e3785-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e3785-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="e3785-126">ATensor</span></span> | <span data-ttu-id="e3785-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3785-127">Input</span></span> | <span data-ttu-id="e3785-128">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3785-128">1 to 8</span></span> | <span data-ttu-id="e3785-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e3785-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="e3785-130">BTensor</span></span> | <span data-ttu-id="e3785-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3785-131">Input</span></span> | <span data-ttu-id="e3785-132">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3785-132">1 to 8</span></span> | <span data-ttu-id="e3785-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e3785-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e3785-134">OutputTensor</span></span> | <span data-ttu-id="e3785-135">Output</span><span class="sxs-lookup"><span data-stu-id="e3785-135">Output</span></span> | <span data-ttu-id="e3785-136">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3785-136">1 to 8</span></span> | <span data-ttu-id="e3785-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e3785-138">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e3785-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="e3785-139">Tensores</span><span class="sxs-lookup"><span data-stu-id="e3785-139">Tensor</span></span> | <span data-ttu-id="e3785-140">Clase</span><span class="sxs-lookup"><span data-stu-id="e3785-140">Kind</span></span> | <span data-ttu-id="e3785-141">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="e3785-141">Supported dimension counts</span></span> | <span data-ttu-id="e3785-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e3785-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e3785-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="e3785-143">ATensor</span></span> | <span data-ttu-id="e3785-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3785-144">Input</span></span> | <span data-ttu-id="e3785-145">4</span><span class="sxs-lookup"><span data-stu-id="e3785-145">4</span></span> | <span data-ttu-id="e3785-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e3785-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="e3785-147">BTensor</span></span> | <span data-ttu-id="e3785-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3785-148">Input</span></span> | <span data-ttu-id="e3785-149">4</span><span class="sxs-lookup"><span data-stu-id="e3785-149">4</span></span> | <span data-ttu-id="e3785-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e3785-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e3785-151">OutputTensor</span></span> | <span data-ttu-id="e3785-152">Output</span><span class="sxs-lookup"><span data-stu-id="e3785-152">Output</span></span> | <span data-ttu-id="e3785-153">4</span><span class="sxs-lookup"><span data-stu-id="e3785-153">4</span></span> | <span data-ttu-id="e3785-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3785-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e3785-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3785-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e3785-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="e3785-156">**Header**</span></span> | <span data-ttu-id="e3785-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="e3785-157">directml.h</span></span> |