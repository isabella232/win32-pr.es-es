---
title: Enumeraciones de DirectML
description: Las enumeraciones siguientes se declaran en DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 6479b1bfe4216a5bdbe8aaee78c258f6f4a64f94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105707513"
---
# <a name="directml-enumerations"></a>Enumeraciones de DirectML

Las enumeraciones siguientes se declaran en DirectML. h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/direct3d12/directml/ne-directml-dml_axis_direction). Define constantes que especifican la dirección de una operación a lo largo del eje especificado para el operador (por ejemplo, la suma, la selección de los elementos de la parte superior y la selección del elemento mínimo). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Define constantes que especifican la naturaleza de los recursos a los que hace referencia una descripción de enlace [DML_BINDING_DESC estructura](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Define constantes que especifican una dirección para el operador de circunvolución DirectML (tal y como se describe en la [estructura DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Define constantes que especifican un modo para el operador de circunvolución DirectML (tal y como se describe en la [estructura DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Proporciona opciones de creación de dispositivos adicionales a [DMLCreateDevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice). |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/direct3d12/directml/ne-directml-dml_depth_space_order). Define constantes que controlan la transformación aplicada en los operadores DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) y **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Proporciona opciones para DirectML para controlar la ejecución de operadores. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Define un conjunto de características y funcionalidades opcionales que se pueden consultar desde el dispositivo DirectML. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_edge_type). Define constantes que especifican un tipo de borde del gráfico. Consulte [DML_GRAPH_EDGE_DESC](./directml/ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_node_type). Define constantes que especifican un tipo de nodo de gráfico. Consulte [DML_GRAPH_NODE_DESC](./directml/ns-directml-dml_graph_node_desc.md) para el uso de esta enumeración. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Define constantes que especifican un modo para el operador DirectML de ejemplo 2-D (como se describe en la [estructura DML_UPSAMPLE_2D_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)). |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Define constantes que especifican una transformación de matriz que se va a aplicar a un tensores de DirectML. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Define el tipo de una descripción del operador. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Define constantes que especifican un modo para el operador DirectML Pad (como se describe en la [estructura DML_PADDING_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)). |
| [**DML_RANDOM_GENERATOR_TYPE**](./directml/ne-directml-dml_random_generator_type.md). Define constantes que especifican los tipos de generador de números aleatorios aleatorios. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Define constantes que especifican una dirección para un operador DirectML recurrente. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Define constantes que especifican el algoritmo de reducción específico que se va a usar para el operador DirectML reduce (como se describe en la [estructura DML_REDUCE_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Especifica el tipo de datos de los valores de un tensores. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Especifica opciones adicionales en una descripción de tensores. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifica un tipo de descripción de tensores. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)