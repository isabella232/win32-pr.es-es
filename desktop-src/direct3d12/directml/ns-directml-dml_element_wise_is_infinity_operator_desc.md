---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, en función del *valor de InfinityMode* especificado y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803102"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="d5b4b-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d5b4b-104">Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, en función del *valor de InfinityMode* especificado y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="d5b4b-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="d5b4b-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d5b4b-106">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b4b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5b4b-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="d5b4b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d5b4b-108">Members</span></span>

`InputTensor`

<span data-ttu-id="d5b4b-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d5b4b-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d5b4b-110">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="d5b4b-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d5b4b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d5b4b-112">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="d5b4b-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="d5b4b-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="d5b4b-114">Un [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determinar el signo del infinito que se debe comprobar.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="d5b4b-115">Si **DML_IS_INFINITY_MODE_EITHER**, se devolverá 1 si el elemento es -inf o inf; en caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="d5b4b-116">Si **DML_IS_INFINITY_MODE_POSITIVE**, se devolverá 1 si el elemento es inf; de lo contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="d5b4b-117">Si **DML_IS_INFINITY_MODE_NEGATIVE**', se devolverá 1 si el elemento es -inf; en caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="d5b4b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5b4b-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="d5b4b-119">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="d5b4b-119">Availability</span></span>
<span data-ttu-id="d5b4b-120">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d5b4b-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d5b4b-121">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-121">Tensor constraints</span></span>
<span data-ttu-id="d5b4b-122">*InputTensor* y *OutputTensor* deben tener los mismos *dimensioncount* y *sizes.*</span><span class="sxs-lookup"><span data-stu-id="d5b4b-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d5b4b-123">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="d5b4b-124">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="d5b4b-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="d5b4b-125">Tensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-125">Tensor</span></span> | <span data-ttu-id="d5b4b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5b4b-126">Kind</span></span> | <span data-ttu-id="d5b4b-127">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-127">Supported dimension counts</span></span> | <span data-ttu-id="d5b4b-128">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d5b4b-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-129">InputTensor</span></span> | <span data-ttu-id="d5b4b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b4b-130">Input</span></span> | <span data-ttu-id="d5b4b-131">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d5b4b-131">1 to 8</span></span> | <span data-ttu-id="d5b4b-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d5b4b-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d5b4b-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-133">OutputTensor</span></span> | <span data-ttu-id="d5b4b-134">Resultados</span><span class="sxs-lookup"><span data-stu-id="d5b4b-134">Output</span></span> | <span data-ttu-id="d5b4b-135">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d5b4b-135">1 to 8</span></span> | <span data-ttu-id="d5b4b-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="d5b4b-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="d5b4b-137">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="d5b4b-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="d5b4b-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-138">Tensor</span></span> | <span data-ttu-id="d5b4b-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5b4b-139">Kind</span></span> | <span data-ttu-id="d5b4b-140">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-140">Supported dimension counts</span></span> | <span data-ttu-id="d5b4b-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d5b4b-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-142">InputTensor</span></span> | <span data-ttu-id="d5b4b-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b4b-143">Input</span></span> | <span data-ttu-id="d5b4b-144">4</span><span class="sxs-lookup"><span data-stu-id="d5b4b-144">4</span></span> | <span data-ttu-id="d5b4b-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d5b4b-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d5b4b-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d5b4b-146">OutputTensor</span></span> | <span data-ttu-id="d5b4b-147">Resultados</span><span class="sxs-lookup"><span data-stu-id="d5b4b-147">Output</span></span> | <span data-ttu-id="d5b4b-148">4</span><span class="sxs-lookup"><span data-stu-id="d5b4b-148">4</span></span> | <span data-ttu-id="d5b4b-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="d5b4b-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="d5b4b-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d5b4b-151">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="d5b4b-151">**Minimum supported client**</span></span> | <span data-ttu-id="d5b4b-152">Windows 10, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="d5b4b-153">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="d5b4b-153">**Minimum supported server**</span></span> | <span data-ttu-id="d5b4b-154">Windows Server, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="d5b4b-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="d5b4b-155">**Header**</span></span> | <span data-ttu-id="d5b4b-156">directml.h</span><span class="sxs-lookup"><span data-stu-id="d5b4b-156">directml.h</span></span> |