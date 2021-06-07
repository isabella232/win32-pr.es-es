---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, dependiendo del valor de *InfinityMode* especificado, y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor.*
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
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418007"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="64d0c-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="64d0c-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="64d0c-104">Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, dependiendo del valor de *InfinityMode* especificado, y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="64d0c-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="64d0c-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="64d0c-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="64d0c-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="64d0c-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64d0c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64d0c-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="64d0c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="64d0c-108">Members</span></span>

`InputTensor`

<span data-ttu-id="64d0c-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64d0c-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64d0c-110">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="64d0c-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="64d0c-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64d0c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64d0c-112">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="64d0c-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="64d0c-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="64d0c-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="64d0c-114">Un [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determinar el signo del infinito que se debe comprobar.</span><span class="sxs-lookup"><span data-stu-id="64d0c-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="64d0c-115">Si **DML_IS_INFINITY_MODE_EITHER**, se devolverá 1 si el elemento es -inf o inf; en caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="64d0c-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="64d0c-116">Si **DML_IS_INFINITY_MODE_POSITIVE**, se devolverá 1 si el elemento es inf; de lo contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="64d0c-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="64d0c-117">Si **DML_IS_INFINITY_MODE_NEGATIVE**" , se devolverá 1 si el elemento es -inf; en caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="64d0c-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="64d0c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64d0c-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="64d0c-119">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="64d0c-119">Availability</span></span>
<span data-ttu-id="64d0c-120">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="64d0c-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="64d0c-121">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-121">Tensor constraints</span></span>
<span data-ttu-id="64d0c-122">*InputTensor* y *OutputTensor* deben tener los mismos *DimensionCount* y *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="64d0c-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="64d0c-123">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="64d0c-124">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="64d0c-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="64d0c-125">Tensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-125">Tensor</span></span> | <span data-ttu-id="64d0c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="64d0c-126">Kind</span></span> | <span data-ttu-id="64d0c-127">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="64d0c-127">Supported dimension counts</span></span> | <span data-ttu-id="64d0c-128">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="64d0c-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="64d0c-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-129">InputTensor</span></span> | <span data-ttu-id="64d0c-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d0c-130">Input</span></span> | <span data-ttu-id="64d0c-131">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="64d0c-131">1 to 8</span></span> | <span data-ttu-id="64d0c-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="64d0c-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="64d0c-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-133">OutputTensor</span></span> | <span data-ttu-id="64d0c-134">Resultados</span><span class="sxs-lookup"><span data-stu-id="64d0c-134">Output</span></span> | <span data-ttu-id="64d0c-135">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="64d0c-135">1 to 8</span></span> | <span data-ttu-id="64d0c-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="64d0c-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="64d0c-137">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="64d0c-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="64d0c-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-138">Tensor</span></span> | <span data-ttu-id="64d0c-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="64d0c-139">Kind</span></span> | <span data-ttu-id="64d0c-140">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="64d0c-140">Supported dimension counts</span></span> | <span data-ttu-id="64d0c-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="64d0c-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="64d0c-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-142">InputTensor</span></span> | <span data-ttu-id="64d0c-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d0c-143">Input</span></span> | <span data-ttu-id="64d0c-144">4</span><span class="sxs-lookup"><span data-stu-id="64d0c-144">4</span></span> | <span data-ttu-id="64d0c-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="64d0c-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="64d0c-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="64d0c-146">OutputTensor</span></span> | <span data-ttu-id="64d0c-147">Resultados</span><span class="sxs-lookup"><span data-stu-id="64d0c-147">Output</span></span> | <span data-ttu-id="64d0c-148">4</span><span class="sxs-lookup"><span data-stu-id="64d0c-148">4</span></span> | <span data-ttu-id="64d0c-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="64d0c-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="64d0c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d0c-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64d0c-151">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="64d0c-151">**Minimum supported client**</span></span> | <span data-ttu-id="64d0c-152">Windows 10, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="64d0c-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="64d0c-153">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="64d0c-153">**Minimum supported server**</span></span> | <span data-ttu-id="64d0c-154">Windows Server, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="64d0c-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="64d0c-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="64d0c-155">**Header**</span></span> | <span data-ttu-id="64d0c-156">directml.h</span><span class="sxs-lookup"><span data-stu-id="64d0c-156">directml.h</span></span> |