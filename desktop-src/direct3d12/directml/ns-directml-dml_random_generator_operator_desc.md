---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Rellena un tensores de salida con bits distribuidos de forma determinista, pseudoaleatorios y con un formato uniforme. Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721202"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="edcf7-104">DML_RANDOM_GENERATOR_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="edcf7-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="edcf7-105">Rellena un tensores de salida con bits distribuidos de forma determinista, pseudoaleatorios y con un formato uniforme.</span><span class="sxs-lookup"><span data-stu-id="edcf7-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="edcf7-106">Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="edcf7-107">Este operador es determinista y se comporta como si fuera una función pura &mdash; , su ejecución no produce efectos secundarios y no utiliza ningún estado global.</span><span class="sxs-lookup"><span data-stu-id="edcf7-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="edcf7-108">La salida pseudoaleatorios generada por este operador depende únicamente de los valores proporcionados en *InputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="edcf7-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="edcf7-109">Los generadores implementados por este operador no son seguros criptográficamente; por lo tanto, este operador no debe usarse para el cifrado, la generación de claves ni otras aplicaciones que requieren la generación de números aleatorios criptográficamente segura.</span><span class="sxs-lookup"><span data-stu-id="edcf7-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="edcf7-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="edcf7-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="edcf7-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="edcf7-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="edcf7-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edcf7-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="edcf7-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="edcf7-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="edcf7-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="edcf7-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="edcf7-115">Tensores de entrada que contiene el estado interno del generador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="edcf7-116">El tamaño y el formato de este tensores de entrada depende de la [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span><span class="sxs-lookup"><span data-stu-id="edcf7-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="edcf7-117">Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, este tensores debe ser de tipo **UINT32** y tener tamaños `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="edcf7-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="edcf7-118">Los primeros valores de 4 32 bits contienen un contador de 128 bits que aumenta de una vez.</span><span class="sxs-lookup"><span data-stu-id="edcf7-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="edcf7-119">Los últimos valores de 2 32 bits contienen el valor de clave de 64 bits para el generador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="edcf7-120">Al inicializar el estado de entrada del generador por primera vez, normalmente el contador de 128 bits (los primeros valores UINT32 de 4 32 bits) se debe inicializar en 0.</span><span class="sxs-lookup"><span data-stu-id="edcf7-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="edcf7-121">La clave se puede elegir arbitrariamente; los distintos valores de clave generarán diferentes secuencias de números.</span><span class="sxs-lookup"><span data-stu-id="edcf7-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="edcf7-122">Normalmente, el valor de la clave se genera mediante un valor de *inicialización* proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="edcf7-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="edcf7-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="edcf7-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="edcf7-124">Tensores de salida que contiene los valores pseudoaleatorios resultantes.</span><span class="sxs-lookup"><span data-stu-id="edcf7-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="edcf7-125">Este tensores puede tener cualquier tamaño.</span><span class="sxs-lookup"><span data-stu-id="edcf7-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="edcf7-126">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="edcf7-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="edcf7-127">Un tensores de salida opcional que contiene el estado de generador interno actualizado.</span><span class="sxs-lookup"><span data-stu-id="edcf7-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="edcf7-128">Si se proporciona, este operador usa *InputStateTensor* para calcular un estado de generador actualizado adecuado y escribe el resultado en el *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="edcf7-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="edcf7-129">Normalmente, los autores de la llamada guardan este resultado y lo suministran como estado de entrada en una ejecución subsiguiente de este operador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="edcf7-130">Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="edcf7-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="edcf7-131">Uno de los valores de la enumeración [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , que indica el tipo de generador que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="edcf7-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="edcf7-132">Actualmente, el único valor válido es **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, que genera números pseudoaleatorios según el [algoritmo PHILOX 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="edcf7-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="edcf7-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edcf7-133">Remarks</span></span>
<span data-ttu-id="edcf7-134">En cada ejecución de este operador, se debe incrementar el contador de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="edcf7-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="edcf7-135">Si se proporciona *OutputStateTensor* , este operador incrementa el contador con el valor correcto en su nombre y escribe el resultado en el *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="edcf7-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="edcf7-136">La cantidad que se debe incrementar depende del número de elementos de salida de 32 bits generados y del tipo del generador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="edcf7-137">Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, el contador de 128 bits debe incrementarse `ceil(outputSize / 4)` en cada ejecución, donde `outputSize` es el número de elementos de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="edcf7-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="edcf7-138">Considere un ejemplo en el que el valor del contador de 128 bits es actualmente `0x48656c6c'6f46726f'6d536561'74746c65` y el tamaño de OutputTensor es `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="edcf7-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="edcf7-139">Después de ejecutar este operador una vez, el contador debería incrementarse en 324.855 (el número de elementos de salida generado dividido por 4, redondeado hacia arriba), lo que da como resultado un valor de contador de `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="edcf7-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="edcf7-140">Este valor actualizado se debe proporcionar como entrada para la siguiente ejecución de este operador.</span><span class="sxs-lookup"><span data-stu-id="edcf7-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="edcf7-141">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="edcf7-141">Availability</span></span>
<span data-ttu-id="edcf7-142">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="edcf7-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="edcf7-143">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="edcf7-143">Tensor constraints</span></span>
<span data-ttu-id="edcf7-144">`InputStateTensor` y `OutputStateTensor` deben tener el mismo *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="edcf7-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="edcf7-145">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="edcf7-145">Tensor support</span></span>
| <span data-ttu-id="edcf7-146">Tensores</span><span class="sxs-lookup"><span data-stu-id="edcf7-146">Tensor</span></span> | <span data-ttu-id="edcf7-147">Clase</span><span class="sxs-lookup"><span data-stu-id="edcf7-147">Kind</span></span> | <span data-ttu-id="edcf7-148">Dimensions</span><span class="sxs-lookup"><span data-stu-id="edcf7-148">Dimensions</span></span> | <span data-ttu-id="edcf7-149">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="edcf7-149">Supported dimension counts</span></span> | <span data-ttu-id="edcf7-150">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="edcf7-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="edcf7-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="edcf7-151">InputStateTensor</span></span> | <span data-ttu-id="edcf7-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="edcf7-152">Input</span></span> | <span data-ttu-id="edcf7-153">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="edcf7-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="edcf7-154">4</span><span class="sxs-lookup"><span data-stu-id="edcf7-154">4</span></span> | <span data-ttu-id="edcf7-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="edcf7-155">UINT32</span></span> |
| <span data-ttu-id="edcf7-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="edcf7-156">OutputTensor</span></span> | <span data-ttu-id="edcf7-157">Output</span><span class="sxs-lookup"><span data-stu-id="edcf7-157">Output</span></span> | <span data-ttu-id="edcf7-158">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="edcf7-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="edcf7-159">4</span><span class="sxs-lookup"><span data-stu-id="edcf7-159">4</span></span> | <span data-ttu-id="edcf7-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="edcf7-160">UINT32</span></span> |
| <span data-ttu-id="edcf7-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="edcf7-161">OutputStateTensor</span></span> | <span data-ttu-id="edcf7-162">Salida opcional</span><span class="sxs-lookup"><span data-stu-id="edcf7-162">Optional output</span></span> | <span data-ttu-id="edcf7-163">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="edcf7-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="edcf7-164">4</span><span class="sxs-lookup"><span data-stu-id="edcf7-164">4</span></span> | <span data-ttu-id="edcf7-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="edcf7-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="edcf7-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edcf7-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="edcf7-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="edcf7-167">**Header**</span></span> | <span data-ttu-id="edcf7-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="edcf7-168">directml.h</span></span> |