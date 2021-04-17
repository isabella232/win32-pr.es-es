---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Comprueba cada elemento de *InputTensor* para IEEE-754-inf, INF, o ambos, según el *InfinityMode* determinado y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: b4f3f07fcbe303e86b422206a8f07eb75fb09d70
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721211"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="0f8b5-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0f8b5-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0f8b5-104">Comprueba cada elemento de *InputTensor* para IEEE-754-inf, INF, o ambos, según el *InfinityMode* determinado y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="0f8b5-105">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="0f8b5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0f8b5-106">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f8b5-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="0f8b5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f8b5-108">Members</span></span>

`InputTensor`

<span data-ttu-id="0f8b5-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0f8b5-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0f8b5-110">Tensores de entrada del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="0f8b5-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0f8b5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0f8b5-112">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="0f8b5-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="0f8b5-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="0f8b5-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) que determina el signo del infinito que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="0f8b5-115">Si **DML_IS_INFINITY_MODE_EITHER**, se devolverá 1 si el elemento es-inf o INF; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="0f8b5-116">Si **DML_IS_INFINITY_MODE_POSITIVE**, se devolverá 1 si el elemento es INF; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="0f8b5-117">Si **DML_IS_INFINITY_MODE_NEGATIVE**', se devolverá 1 si el elemento es-INF; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="0f8b5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f8b5-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="0f8b5-119">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="0f8b5-119">Availability</span></span>
<span data-ttu-id="0f8b5-120">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="0f8b5-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0f8b5-121">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-121">Tensor constraints</span></span>
<span data-ttu-id="0f8b5-122">*InputTensor* y *OutputTensor* deben tener los mismos *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="0f8b5-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0f8b5-123">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="0f8b5-124">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="0f8b5-125">Tensores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-125">Tensor</span></span> | <span data-ttu-id="0f8b5-126">Clase</span><span class="sxs-lookup"><span data-stu-id="0f8b5-126">Kind</span></span> | <span data-ttu-id="0f8b5-127">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="0f8b5-127">Supported dimension counts</span></span> | <span data-ttu-id="0f8b5-128">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="0f8b5-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0f8b5-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0f8b5-129">InputTensor</span></span> | <span data-ttu-id="0f8b5-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8b5-130">Input</span></span> | <span data-ttu-id="0f8b5-131">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0f8b5-131">1 to 8</span></span> | <span data-ttu-id="0f8b5-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0f8b5-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0f8b5-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0f8b5-133">OutputTensor</span></span> | <span data-ttu-id="0f8b5-134">Output</span><span class="sxs-lookup"><span data-stu-id="0f8b5-134">Output</span></span> | <span data-ttu-id="0f8b5-135">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0f8b5-135">1 to 8</span></span> | <span data-ttu-id="0f8b5-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="0f8b5-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="0f8b5-137">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="0f8b5-138">Tensores</span><span class="sxs-lookup"><span data-stu-id="0f8b5-138">Tensor</span></span> | <span data-ttu-id="0f8b5-139">Clase</span><span class="sxs-lookup"><span data-stu-id="0f8b5-139">Kind</span></span> | <span data-ttu-id="0f8b5-140">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="0f8b5-140">Supported dimension counts</span></span> | <span data-ttu-id="0f8b5-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="0f8b5-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0f8b5-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0f8b5-142">InputTensor</span></span> | <span data-ttu-id="0f8b5-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8b5-143">Input</span></span> | <span data-ttu-id="0f8b5-144">4</span><span class="sxs-lookup"><span data-stu-id="0f8b5-144">4</span></span> | <span data-ttu-id="0f8b5-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0f8b5-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0f8b5-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0f8b5-146">OutputTensor</span></span> | <span data-ttu-id="0f8b5-147">Output</span><span class="sxs-lookup"><span data-stu-id="0f8b5-147">Output</span></span> | <span data-ttu-id="0f8b5-148">4</span><span class="sxs-lookup"><span data-stu-id="0f8b5-148">4</span></span> | <span data-ttu-id="0f8b5-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="0f8b5-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="0f8b5-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f8b5-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0f8b5-151">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="0f8b5-151">**Minimum supported client**</span></span> | <span data-ttu-id="0f8b5-152">Windows 10, versión 2004 (10,0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="0f8b5-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="0f8b5-153">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="0f8b5-153">**Minimum supported server**</span></span> | <span data-ttu-id="0f8b5-154">Windows Server, versión 2004 (10,0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="0f8b5-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="0f8b5-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="0f8b5-155">**Header**</span></span> | <span data-ttu-id="0f8b5-156">directml. h</span><span class="sxs-lookup"><span data-stu-id="0f8b5-156">directml.h</span></span> |