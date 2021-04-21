---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para [la normalización de la respuesta local.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804474"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="ac703-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ac703-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="ac703-104">Calcula los degradados de repropagación para [la normalización de la respuesta local.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="ac703-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="ac703-105">El tipo de datos y el tamaño de todos los tensores deben ser los mismos.</span><span class="sxs-lookup"><span data-stu-id="ac703-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac703-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="ac703-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="ac703-107">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ac703-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac703-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac703-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="ac703-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac703-109">Members</span></span>

`InputTensor`

<span data-ttu-id="ac703-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac703-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac703-111">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac703-111">The tensor containing the input data.</span></span> <span data-ttu-id="ac703-112">Los tamaños de  este tensor deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ac703-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="ac703-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac703-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac703-114">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="ac703-114">The incoming gradient tensor.</span></span> <span data-ttu-id="ac703-115">Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="ac703-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="ac703-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac703-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac703-117">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="ac703-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="ac703-118">Tipo: **[BOOL](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac703-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ac703-119">**TRUE** si la capa LRN suma entre canales; **FALSE** si la capa LRN suma entre dimensiones espaciales.</span><span class="sxs-lookup"><span data-stu-id="ac703-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="ac703-120">Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac703-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ac703-121">Número máximo de elementos que se suman por dimensión (la región local se recorta para que todos los elementos estén dentro de los límites).</span><span class="sxs-lookup"><span data-stu-id="ac703-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="ac703-122">Si *CrossChannel* es **TRUE**, este es el ancho y alto de la región local.</span><span class="sxs-lookup"><span data-stu-id="ac703-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="ac703-123">Si *CrossChannel* es **FALSE,** este es el número de elementos de la región local.</span><span class="sxs-lookup"><span data-stu-id="ac703-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="ac703-124">Este valor debe ser al menos 1.</span><span class="sxs-lookup"><span data-stu-id="ac703-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="ac703-125">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac703-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ac703-126">Valor del parámetro de escalado.</span><span class="sxs-lookup"><span data-stu-id="ac703-126">The value of the scaling parameter.</span></span> <span data-ttu-id="ac703-127">Se recomienda un valor de 0,0001 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ac703-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="ac703-128">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac703-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ac703-129">Valor del exponente.</span><span class="sxs-lookup"><span data-stu-id="ac703-129">The value of the exponent.</span></span> <span data-ttu-id="ac703-130">Se recomienda un valor de 0,75 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ac703-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="ac703-131">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac703-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ac703-132">Valor de sesgo.</span><span class="sxs-lookup"><span data-stu-id="ac703-132">The value of bias.</span></span> <span data-ttu-id="ac703-133">Se recomienda un valor de 1 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ac703-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="ac703-134">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="ac703-134">Availability</span></span>
<span data-ttu-id="ac703-135">Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="ac703-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ac703-136">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="ac703-136">Tensor constraints</span></span>
<span data-ttu-id="ac703-137">*InputGradientTensor,* *InputTensor* y *OutputGradientTensor* deben tener los mismos *datatype* y *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="ac703-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ac703-138">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="ac703-138">Tensor support</span></span>
| <span data-ttu-id="ac703-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="ac703-139">Tensor</span></span> | <span data-ttu-id="ac703-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac703-140">Kind</span></span> | <span data-ttu-id="ac703-141">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="ac703-141">Supported dimension counts</span></span> | <span data-ttu-id="ac703-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="ac703-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ac703-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ac703-143">InputTensor</span></span> | <span data-ttu-id="ac703-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac703-144">Input</span></span> | <span data-ttu-id="ac703-145">4</span><span class="sxs-lookup"><span data-stu-id="ac703-145">4</span></span> | <span data-ttu-id="ac703-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ac703-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ac703-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="ac703-147">InputGradientTensor</span></span> | <span data-ttu-id="ac703-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac703-148">Input</span></span> | <span data-ttu-id="ac703-149">4</span><span class="sxs-lookup"><span data-stu-id="ac703-149">4</span></span> | <span data-ttu-id="ac703-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ac703-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ac703-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="ac703-151">OutputGradientTensor</span></span> | <span data-ttu-id="ac703-152">Resultados</span><span class="sxs-lookup"><span data-stu-id="ac703-152">Output</span></span> | <span data-ttu-id="ac703-153">4</span><span class="sxs-lookup"><span data-stu-id="ac703-153">4</span></span> | <span data-ttu-id="ac703-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ac703-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="ac703-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac703-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ac703-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="ac703-156">**Header**</span></span> | <span data-ttu-id="ac703-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="ac703-157">directml.h</span></span> |
