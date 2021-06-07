---
title: Historial de nivel de característica de DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521221"
---
# <a name="directml-feature-level-history"></a>Historial de nivel de característica de DirectML

Para obtener información general sobre el historial de versiones de DirectML, [consulte Historial de versiones de DirectML.](./dml-version-history.md)

## <a name="dml_feature_level_3_1"></a>DML_FEATURE_LEVEL_3_1

Se introdujo en la versión 1.5.0 de DirectML.

Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)

* **DML_OPERATOR_ELEMENT_WISE_ATAN_YX**
* **DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**
* **DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**
* **DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_BATCH_NORMALIZATION_GRAD**

El número máximo de dimensiones admitidas para los operadores siguientes ha aumentado de 4 a 8.

* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_CAST**
* **DML_OPERATOR_JOIN**
* **DML_OPERATOR_LP_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_PADDING**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_TILE**
* **DML_OPERATOR_TOP_K**
* **DML_OPERATOR_TOP_K1**

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Se introdujo en la versión 1.4.0 de DirectML.

Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)

* **DML_OPERATOR_ELEMENT_WISE_BIT_AND**
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Se han agregado las siguientes mejoras.

* El número máximo de dimensiones de tensor ha aumentado de 5 a 8. Vea [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** y **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE**, cuando se **usa DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**
* Se han agregado los siguientes tipos de datos de 64 bits y son compatibles con operadores select.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Funcionalidad en desuso.

* **DML_REDUCE_FUNCTION_ARGMAX** y **DML_REDUCE_FUNCTION_ARGMIN** han quedado en desuso. Debe preferir usar los operadores **DML_OPERATOR_ARGMIN** y **DML_OPERATOR_ARGMAX** independientes en su lugar.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Se introdujo en la versión 1.2.0 de DirectML.

Se han agregado las siguientes API.

* [Interfaz IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice1)
* Compatibilidad con gráficos de operadores [(vea IDMLDevice1::CompileGraph)](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)

Se ha agregado compatibilidad con los operadores siguientes.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Se han agregado las siguientes mejoras.

* Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** y **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE**, cuando se usa una de las siguientes funciones de reducción.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Restricciones de formas de tensor relajadas **para DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Se introdujo en la versión 1.1.0 de DirectML.

Se han agregado las siguientes API.
* [Función DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [DML_FEATURE_LEVEL enumeración](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Consultas de nivel de característica (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Se ha agregado compatibilidad con los operadores siguientes.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Se han agregado las siguientes mejoras.

* Al enlazar un recurso de entrada para el envío de un [IDMLOperatorInitializer,](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)ahora es legal proporcionar un recurso con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (además de **D3D12_HEAP_TYPE_DEFAULT**), siempre que también se establezcan las propiedades de montón adecuadas. Vea [Enlace en DirectML.](./dml-binding.md)
* Los siguientes operadores booleanos lógicos ahora admiten tensores de salida **UINT8,** además de la compatibilidad existente con **UINT32**.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* Las funciones de activación 5D ahora admiten el uso de strides en sus tensores de entrada y salida.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Nivel de característica en el que se introdujo DirectML.

## <a name="see-also"></a>Vea también

* [Historial de versiones de DirectML](./dml-version-history.md)
* [DML_FEATURE_LEVEL enumeración](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Función DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [DML_FEATURE_QUERY_FEATURE_LEVELS estructura](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
