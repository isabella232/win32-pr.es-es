---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Realiza un desplazamiento lógico a la derecha de cada elemento de *ATensor* mediante una serie de bits dados por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418010"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="fba10-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="fba10-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fba10-104">Realiza un desplazamiento lógico a la derecha de cada elemento de *ATensor* mediante una serie de bits dados por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="fba10-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="fba10-105">Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede crear un alias de uno de los tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="fba10-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fba10-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="fba10-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="fba10-107">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="fba10-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fba10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba10-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="fba10-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fba10-109">Members</span></span>

`ATensor`

<span data-ttu-id="fba10-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fba10-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fba10-111">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="fba10-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="fba10-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fba10-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fba10-113">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="fba10-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="fba10-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fba10-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fba10-115">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="fba10-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="fba10-116">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="fba10-116">Availability</span></span>
<span data-ttu-id="fba10-117">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fba10-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fba10-118">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="fba10-118">Tensor constraints</span></span>
<span data-ttu-id="fba10-119">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *tamaños DataType,* *DimensionCount* y *.*</span><span class="sxs-lookup"><span data-stu-id="fba10-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fba10-120">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="fba10-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="fba10-121">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="fba10-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="fba10-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="fba10-122">Tensor</span></span> | <span data-ttu-id="fba10-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="fba10-123">Kind</span></span> | <span data-ttu-id="fba10-124">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="fba10-124">Supported dimension counts</span></span> | <span data-ttu-id="fba10-125">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="fba10-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fba10-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="fba10-126">ATensor</span></span> | <span data-ttu-id="fba10-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="fba10-127">Input</span></span> | <span data-ttu-id="fba10-128">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fba10-128">1 to 8</span></span> | <span data-ttu-id="fba10-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fba10-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="fba10-130">BTensor</span></span> | <span data-ttu-id="fba10-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="fba10-131">Input</span></span> | <span data-ttu-id="fba10-132">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fba10-132">1 to 8</span></span> | <span data-ttu-id="fba10-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fba10-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fba10-134">OutputTensor</span></span> | <span data-ttu-id="fba10-135">Resultados</span><span class="sxs-lookup"><span data-stu-id="fba10-135">Output</span></span> | <span data-ttu-id="fba10-136">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fba10-136">1 to 8</span></span> | <span data-ttu-id="fba10-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="fba10-138">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="fba10-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="fba10-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="fba10-139">Tensor</span></span> | <span data-ttu-id="fba10-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="fba10-140">Kind</span></span> | <span data-ttu-id="fba10-141">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="fba10-141">Supported dimension counts</span></span> | <span data-ttu-id="fba10-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="fba10-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fba10-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="fba10-143">ATensor</span></span> | <span data-ttu-id="fba10-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="fba10-144">Input</span></span> | <span data-ttu-id="fba10-145">4</span><span class="sxs-lookup"><span data-stu-id="fba10-145">4</span></span> | <span data-ttu-id="fba10-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fba10-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="fba10-147">BTensor</span></span> | <span data-ttu-id="fba10-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="fba10-148">Input</span></span> | <span data-ttu-id="fba10-149">4</span><span class="sxs-lookup"><span data-stu-id="fba10-149">4</span></span> | <span data-ttu-id="fba10-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fba10-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fba10-151">OutputTensor</span></span> | <span data-ttu-id="fba10-152">Resultados</span><span class="sxs-lookup"><span data-stu-id="fba10-152">Output</span></span> | <span data-ttu-id="fba10-153">4</span><span class="sxs-lookup"><span data-stu-id="fba10-153">4</span></span> | <span data-ttu-id="fba10-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fba10-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fba10-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba10-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fba10-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="fba10-156">**Header**</span></span> | <span data-ttu-id="fba10-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="fba10-157">directml.h</span></span> |