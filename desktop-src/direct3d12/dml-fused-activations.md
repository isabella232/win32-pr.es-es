---
title: Uso de operadores combinados para mejorar el rendimiento
description: Algunos operadores de DirectML admiten un concepto conocido como *fusión.* La fusión de operadores es una manera de mejorar el rendimiento mediante la combinación de un operador (normalmente, una función de activación) en un operador diferente para que se ejecuten juntos sin necesidad de un recorrido de ida y vuelta a la memoria.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803985"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="a0b47-104">Uso de operadores combinados para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="a0b47-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="a0b47-105">Algunos operadores de DirectML admiten un concepto conocido como *fusión.*</span><span class="sxs-lookup"><span data-stu-id="a0b47-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="a0b47-106">La fusión de operadores es una manera de mejorar el rendimiento mediante la combinación de un operador (normalmente, una función de activación) en un operador diferente para que se ejecuten juntos sin necesidad de un recorrido de ida y vuelta a la memoria.</span><span class="sxs-lookup"><span data-stu-id="a0b47-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="a0b47-107">Cuándo fusionar las activaciones</span><span class="sxs-lookup"><span data-stu-id="a0b47-107">When to fuse activations</span></span>

<span data-ttu-id="a0b47-108">Las activaciones fusionadas son una optimización del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a0b47-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="a0b47-109">Un escenario muy común en muchos modelos de aprendizaje automático (ML) es aplicar una no linealidad (una función de activación) a la salida de cada capa del modelo.</span><span class="sxs-lookup"><span data-stu-id="a0b47-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="a0b47-110">Normalmente, esto requiere un recorrido de ida y vuelta a la memoria de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a0b47-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="a0b47-111">Por ejemplo, si una convolución va seguida de una activación relu no fusionada, la GPU debe esperar a que los resultados de Convolution se escriban en la memoria de GPU antes de poder empezar a calcular la capa de activación relu.</span><span class="sxs-lookup"><span data-stu-id="a0b47-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="a0b47-112">Como la carga de trabajo de proceso de la mayoría de las funciones de activación tiende a ser pequeña, este recorrido de ida y vuelta a la memoria de gráficos puede ser un cuello de botella de rendimiento importante.</span><span class="sxs-lookup"><span data-stu-id="a0b47-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="a0b47-113">La fusión de operadores permite que la función de activación (Relu en el ejemplo anterior) se realice como parte del operador anterior (por ejemplo, Convolution).</span><span class="sxs-lookup"><span data-stu-id="a0b47-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="a0b47-114">Esto permite que la GPU calcule la función de activación sin esperar a que los resultados del operador anterior se escriban en la memoria y &mdash; esto mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a0b47-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="a0b47-115">Dado que las activaciones fusionadas producen el mismo resultado, pero son más rápidas en muchos casos, se recomienda eliminar las capas de activación al fusionarlas en su operador anterior siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="a0b47-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="a0b47-116">Cómo fusionar activaciones</span><span class="sxs-lookup"><span data-stu-id="a0b47-116">How to fuse activations</span></span>

<span data-ttu-id="a0b47-117">Los operadores que admiten activaciones fusionadas tienen un parámetro opcional adicional en su estructura de operador, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="a0b47-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="a0b47-118">Por ejemplo, Convolution admite la activación fusionada y tiene una *FusedActivation* correspondiente en su descripción del operador [(vea DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="a0b47-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="a0b47-119">Para fusionar una activación, cree [un DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) que describa el tipo de activación que se va a fusionar.</span><span class="sxs-lookup"><span data-stu-id="a0b47-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="a0b47-120">Por ejemplo, para fusionar una función Relu, el tipo de operador correcto [sería DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="a0b47-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="a0b47-121">Al construir la descripción del operador para la función de activación, debe establecer los parámetros *InputTensor* y *OutputTensor* para la función de activación en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a0b47-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="a0b47-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0b47-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="a0b47-123">Para obtener un ejemplo completo, el [ejemplo DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) usa activaciones fusionadas para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a0b47-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="a0b47-124">Operadores que admiten la activación fusionada</span><span class="sxs-lookup"><span data-stu-id="a0b47-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="a0b47-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="a0b47-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="a0b47-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="a0b47-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="a0b47-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="a0b47-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="a0b47-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** y **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="a0b47-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="a0b47-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="a0b47-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="a0b47-130">Activaciones que se admiten para la fusión</span><span class="sxs-lookup"><span data-stu-id="a0b47-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="a0b47-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="a0b47-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="a0b47-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="a0b47-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="a0b47-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="a0b47-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="a0b47-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="a0b47-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="a0b47-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="a0b47-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="a0b47-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="a0b47-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="a0b47-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="a0b47-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="a0b47-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="a0b47-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="a0b47-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="a0b47-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="a0b47-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="a0b47-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="a0b47-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="a0b47-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="a0b47-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="a0b47-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="a0b47-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="a0b47-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="a0b47-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="a0b47-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="a0b47-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="a0b47-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="a0b47-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="a0b47-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="a0b47-147">No se admiten los operadores que no están en esta lista para la activación fusionada.</span><span class="sxs-lookup"><span data-stu-id="a0b47-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0b47-148">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a0b47-148">See also</span></span>

* [<span data-ttu-id="a0b47-149">Ejemplo de DirectMLSuperResolution</span><span class="sxs-lookup"><span data-stu-id="a0b47-149">DirectMLSuperResolution sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [<span data-ttu-id="a0b47-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="a0b47-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
