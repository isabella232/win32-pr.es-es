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
# <a name="using-fused-operators-to-improve-performance"></a>Uso de operadores combinados para mejorar el rendimiento

Algunos operadores de DirectML admiten un concepto conocido como *fusión.* La fusión de operadores es una manera de mejorar el rendimiento mediante la combinación de un operador (normalmente, una función de activación) en un operador diferente para que se ejecuten juntos sin necesidad de un recorrido de ida y vuelta a la memoria.

## <a name="when-to-fuse-activations"></a>Cuándo fusionar las activaciones

Las activaciones fusionadas son una optimización del rendimiento. Un escenario muy común en muchos modelos de aprendizaje automático (ML) es aplicar una no linealidad (una función de activación) a la salida de cada capa del modelo.

Normalmente, esto requiere un recorrido de ida y vuelta a la memoria de gráficos. Por ejemplo, si una convolución va seguida de una activación relu no fusionada, la GPU debe esperar a que los resultados de Convolution se escriban en la memoria de GPU antes de poder empezar a calcular la capa de activación relu. Como la carga de trabajo de proceso de la mayoría de las funciones de activación tiende a ser pequeña, este recorrido de ida y vuelta a la memoria de gráficos puede ser un cuello de botella de rendimiento importante.

La fusión de operadores permite que la función de activación (Relu en el ejemplo anterior) se realice como parte del operador anterior (por ejemplo, Convolution). Esto permite que la GPU calcule la función de activación sin esperar a que los resultados del operador anterior se escriban en la memoria y &mdash; esto mejora el rendimiento.

Dado que las activaciones fusionadas producen el mismo resultado, pero son más rápidas en muchos casos, se recomienda eliminar las capas de activación al fusionarlas en su operador anterior siempre que sea posible.

## <a name="how-to-fuse-activations"></a>Cómo fusionar activaciones

Los operadores que admiten activaciones fusionadas tienen un parámetro opcional adicional en su estructura de operador, `const DML_OPERATOR_DESC* FusedActivation` . Por ejemplo, Convolution admite la activación fusionada y tiene una *FusedActivation* correspondiente en su descripción del operador [(vea DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Para fusionar una activación, cree [un DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) que describa el tipo de activación que se va a fusionar. Por ejemplo, para fusionar una función Relu, el tipo de operador correcto [sería DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Al construir la descripción del operador para la función de activación, debe establecer los parámetros *InputTensor* y *OutputTensor* para la función de activación en **NULL.**

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

Para obtener un ejemplo completo, el [ejemplo DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) usa activaciones fusionadas para mejorar el rendimiento.

## <a name="operators-that-support-fused-activation"></a>Operadores que admiten la activación fusionada

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

No se admiten los operadores que no están en esta lista para la activación fusionada.

## <a name="see-also"></a>Consulta también

* [Ejemplo de DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
