---
title: Usar operadores combinados para mejorar el rendimiento
description: Algunos operadores DirectML admiten un concepto conocido como *fusión*. La fusión de operadores es una manera de mejorar el rendimiento mediante la combinación de un operador (normalmente, una función de activación) en un operador diferente para que se ejecuten juntos sin necesidad de un viaje de ida y vuelta a la memoria.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "104549200"
---
# <a name="using-fused-operators-to-improve-performance"></a>Usar operadores combinados para mejorar el rendimiento

Algunos operadores DirectML admiten un concepto conocido como *fusión*. La fusión de operadores es una manera de mejorar el rendimiento mediante la combinación de un operador (normalmente, una función de activación) en un operador diferente para que se ejecuten juntos sin necesidad de un viaje de ida y vuelta a la memoria.

## <a name="when-to-fuse-activations"></a>Cuándo se deben confundir las activaciones

Las activaciones con fusibles son una optimización del rendimiento. Un escenario muy común en muchos modelos de aprendizaje automático (ML) es aplicar una no linealidad (una función de activación) a la salida de cada capa del modelo.

Normalmente, esto requiere un viaje de ida y vuelta a la memoria de gráficos. Por ejemplo, si una circunvolución va seguida de una activación Relu sin fusibles, la GPU debe esperar a que los resultados de la circunvolución se escriban en la memoria de la GPU para poder comenzar a calcular la capa de activación de Relu. Dado que la carga de trabajo de proceso de la mayoría de las funciones de activación tiende a ser pequeña, este viaje de ida y vuelta a la memoria de gráficos puede ser un cuello de botella de rendimiento importante.

La fusión de operadores permite realizar la función de activación (Relu en el ejemplo anterior) como parte del operador anterior (convolución, por ejemplo). Esto permite que la GPU calcule la función de activación sin esperar a que los resultados del operador anterior se escriban en la memoria &mdash; y mejore el rendimiento.

Dado que las activaciones con fusible producen el mismo resultado, pero son más rápidas en muchos casos, se recomienda que elimine las capas de activación al separarlas en el operador anterior siempre que sea posible.

## <a name="how-to-fuse-activations"></a>Cómo confundir las activaciones

Los operadores que admiten activaciones con fusible tienen un parámetro opcional adicional en su struct de operador, `const DML_OPERATOR_DESC* FusedActivation` . La circunvolución, por ejemplo, admite la activación con fusible y tiene un *FusedActivation* correspondiente en la descripción del operador (vea [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Para confundir una activación, construya un [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) que describa el tipo de activación que se va a fusionar. Por ejemplo, para confundir una función Relu, el tipo de operador correcto sería [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Al construir la descripción del operador para la función de activación, debe establecer los parámetros *InputTensor* y *OutputTensor* para la función de activación en **null**.

## <a name="example"></a>Ejemplo

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

Para obtener un ejemplo completo, el [ejemplo DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) emplea activaciones con fusibles para mejorar el rendimiento.

## <a name="operators-that-support-fused-activation"></a>Operadores que admiten la activación con fusible

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** y **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Activaciones que se admiten para la fusión

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Los operadores que no estén en esta lista no se admiten para la activación con fusibles.

## <a name="see-also"></a>Consulte también

[Ejemplo de DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
