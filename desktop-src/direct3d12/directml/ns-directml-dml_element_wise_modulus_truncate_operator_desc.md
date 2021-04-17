---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Calcula el operador de C Modul para cada par de elementos correspondientes de los diez de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: f7cbfbf8613fb4309c6d336ccd807565d0dae53c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721209"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="e93ad-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e93ad-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e93ad-104">Calcula el operador de C Modul para cada par de elementos correspondientes de los diez de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e93ad-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="e93ad-105">Dado que el cociente se redondea hacia 0, el resultado tendrá el mismo signo que el dividendo.</span><span class="sxs-lookup"><span data-stu-id="e93ad-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="e93ad-106">Este operador admite la ejecución en contexto, lo que significa que se permite que *OutputTensor* alias a uno de los decenas de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="e93ad-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e93ad-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="e93ad-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e93ad-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e93ad-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e93ad-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e93ad-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="e93ad-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e93ad-110">Members</span></span>

`ATensor`

<span data-ttu-id="e93ad-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e93ad-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e93ad-112">Un tensores que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="e93ad-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="e93ad-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e93ad-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e93ad-114">Un tensores que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="e93ad-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="e93ad-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e93ad-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e93ad-116">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="e93ad-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e93ad-117">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e93ad-117">Availability</span></span>
<span data-ttu-id="e93ad-118">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e93ad-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e93ad-119">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="e93ad-119">Tensor constraints</span></span>
<span data-ttu-id="e93ad-120">*ATensor*, *BTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="e93ad-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e93ad-121">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="e93ad-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="e93ad-122">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e93ad-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="e93ad-123">Tensores</span><span class="sxs-lookup"><span data-stu-id="e93ad-123">Tensor</span></span> | <span data-ttu-id="e93ad-124">Clase</span><span class="sxs-lookup"><span data-stu-id="e93ad-124">Kind</span></span> | <span data-ttu-id="e93ad-125">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="e93ad-125">Supported dimension counts</span></span> | <span data-ttu-id="e93ad-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e93ad-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e93ad-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-127">ATensor</span></span> | <span data-ttu-id="e93ad-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="e93ad-128">Input</span></span> | <span data-ttu-id="e93ad-129">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e93ad-129">1 to 8</span></span> | <span data-ttu-id="e93ad-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e93ad-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-131">BTensor</span></span> | <span data-ttu-id="e93ad-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e93ad-132">Input</span></span> | <span data-ttu-id="e93ad-133">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e93ad-133">1 to 8</span></span> | <span data-ttu-id="e93ad-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e93ad-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-135">OutputTensor</span></span> | <span data-ttu-id="e93ad-136">Output</span><span class="sxs-lookup"><span data-stu-id="e93ad-136">Output</span></span> | <span data-ttu-id="e93ad-137">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e93ad-137">1 to 8</span></span> | <span data-ttu-id="e93ad-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e93ad-139">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e93ad-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="e93ad-140">Tensores</span><span class="sxs-lookup"><span data-stu-id="e93ad-140">Tensor</span></span> | <span data-ttu-id="e93ad-141">Clase</span><span class="sxs-lookup"><span data-stu-id="e93ad-141">Kind</span></span> | <span data-ttu-id="e93ad-142">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="e93ad-142">Supported dimension counts</span></span> | <span data-ttu-id="e93ad-143">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e93ad-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e93ad-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-144">ATensor</span></span> | <span data-ttu-id="e93ad-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="e93ad-145">Input</span></span> | <span data-ttu-id="e93ad-146">4</span><span class="sxs-lookup"><span data-stu-id="e93ad-146">4</span></span> | <span data-ttu-id="e93ad-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e93ad-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-148">BTensor</span></span> | <span data-ttu-id="e93ad-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="e93ad-149">Input</span></span> | <span data-ttu-id="e93ad-150">4</span><span class="sxs-lookup"><span data-stu-id="e93ad-150">4</span></span> | <span data-ttu-id="e93ad-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e93ad-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e93ad-152">OutputTensor</span></span> | <span data-ttu-id="e93ad-153">Output</span><span class="sxs-lookup"><span data-stu-id="e93ad-153">Output</span></span> | <span data-ttu-id="e93ad-154">4</span><span class="sxs-lookup"><span data-stu-id="e93ad-154">4</span></span> | <span data-ttu-id="e93ad-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e93ad-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e93ad-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e93ad-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e93ad-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="e93ad-157">**Header**</span></span> | <span data-ttu-id="e93ad-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="e93ad-158">directml.h</span></span> |