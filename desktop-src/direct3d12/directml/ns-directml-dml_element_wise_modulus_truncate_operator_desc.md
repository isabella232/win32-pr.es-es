---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Calcula el operador de módulo de C para cada par de elementos correspondientes de los tensores de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.
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
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417981"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="1d64d-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="1d64d-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1d64d-104">Calcula el operador de módulo de C para cada par de elementos correspondientes de los tensores de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="1d64d-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="1d64d-105">Dado que el cociente se redondea hacia 0, el resultado tendrá el mismo signo que el dividendo.</span><span class="sxs-lookup"><span data-stu-id="1d64d-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="1d64d-106">Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede crear un alias de uno de los tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="1d64d-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d64d-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="1d64d-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="1d64d-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="1d64d-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d64d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d64d-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="1d64d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d64d-110">Members</span></span>

`ATensor`

<span data-ttu-id="1d64d-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1d64d-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1d64d-112">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="1d64d-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="1d64d-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1d64d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1d64d-114">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="1d64d-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="1d64d-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1d64d-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1d64d-116">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="1d64d-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="1d64d-117">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="1d64d-117">Availability</span></span>
<span data-ttu-id="1d64d-118">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="1d64d-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1d64d-119">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-119">Tensor constraints</span></span>
<span data-ttu-id="1d64d-120">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *DataType,* *DimensionCount* y *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="1d64d-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1d64d-121">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="1d64d-122">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="1d64d-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="1d64d-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-123">Tensor</span></span> | <span data-ttu-id="1d64d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d64d-124">Kind</span></span> | <span data-ttu-id="1d64d-125">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="1d64d-125">Supported dimension counts</span></span> | <span data-ttu-id="1d64d-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="1d64d-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1d64d-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-127">ATensor</span></span> | <span data-ttu-id="1d64d-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d64d-128">Input</span></span> | <span data-ttu-id="1d64d-129">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="1d64d-129">1 to 8</span></span> | <span data-ttu-id="1d64d-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1d64d-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-131">BTensor</span></span> | <span data-ttu-id="1d64d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d64d-132">Input</span></span> | <span data-ttu-id="1d64d-133">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="1d64d-133">1 to 8</span></span> | <span data-ttu-id="1d64d-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1d64d-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-135">OutputTensor</span></span> | <span data-ttu-id="1d64d-136">Resultados</span><span class="sxs-lookup"><span data-stu-id="1d64d-136">Output</span></span> | <span data-ttu-id="1d64d-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="1d64d-137">1 to 8</span></span> | <span data-ttu-id="1d64d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="1d64d-139">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="1d64d-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="1d64d-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-140">Tensor</span></span> | <span data-ttu-id="1d64d-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d64d-141">Kind</span></span> | <span data-ttu-id="1d64d-142">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="1d64d-142">Supported dimension counts</span></span> | <span data-ttu-id="1d64d-143">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="1d64d-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1d64d-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-144">ATensor</span></span> | <span data-ttu-id="1d64d-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d64d-145">Input</span></span> | <span data-ttu-id="1d64d-146">4</span><span class="sxs-lookup"><span data-stu-id="1d64d-146">4</span></span> | <span data-ttu-id="1d64d-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1d64d-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-148">BTensor</span></span> | <span data-ttu-id="1d64d-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d64d-149">Input</span></span> | <span data-ttu-id="1d64d-150">4</span><span class="sxs-lookup"><span data-stu-id="1d64d-150">4</span></span> | <span data-ttu-id="1d64d-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1d64d-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1d64d-152">OutputTensor</span></span> | <span data-ttu-id="1d64d-153">Resultados</span><span class="sxs-lookup"><span data-stu-id="1d64d-153">Output</span></span> | <span data-ttu-id="1d64d-154">4</span><span class="sxs-lookup"><span data-stu-id="1d64d-154">4</span></span> | <span data-ttu-id="1d64d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1d64d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="1d64d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d64d-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1d64d-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="1d64d-157">**Header**</span></span> | <span data-ttu-id="1d64d-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="1d64d-158">directml.h</span></span> |