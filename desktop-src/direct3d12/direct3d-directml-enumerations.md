---
title: Enumeraciones de DirectML
description: Las enumeraciones siguientes se declaran en DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 2a761dba639ece37eba347115a831d3c6803a618
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359794"
---
# <a name="directml-enumerations"></a>Enumeraciones de DirectML

Las enumeraciones siguientes se declaran en DirectML.h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Define constantes que especifican la dirección de una operación a lo largo del eje especificado para el operador (por ejemplo, suma, selección de los elementos de la parte superior k y selección del elemento mínimo). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Define constantes que especifican la naturaleza de los recursos a los que hace referencia una descripción de [enlace DML_BINDING_DESC estructura](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Define constantes que especifican una dirección para el operador de convolución de DirectML (como se describe en la [estructura DML_CONVOLUTION_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Define constantes que especifican un modo para el operador de convolución de DirectML (como se describe en la [DML_CONVOLUTION_OPERATOR_DESC estructura](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Proporciona opciones de creación de dispositivos adicionales [a DMLCreateDevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice). |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Define constantes que controlan la transformación aplicada en los operadores de DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) y **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Proporciona opciones a DirectML para controlar la ejecución de operadores. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Define un conjunto de características y funcionalidades opcionales que se pueden consultar desde el dispositivo DirectML. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Define constantes que especifican un tipo de borde de grafo. Consulte [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) para el uso de esta enumeración. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Define constantes que especifican un tipo de nodo de grafo. Consulte [DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) para ver el uso de esta enumeración. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Define constantes que especifican un modo para el operador 2D upsample 2D de DirectML (como se describe en [la estructura DML_UPSAMPLE_2D_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc) |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Define constantes que especifican una transformación de matriz que se va a aplicar a un tensor de DirectML. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Define el tipo de descripción de un operador. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Define constantes que especifican un modo para el operador de panel de DirectML (como se describe en la [estructura DML_PADDING_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc) |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Define constantes que especifican tipos de generador de números aleatorios. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Define constantes que especifican una dirección para un operador directML recurrente. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Define constantes que especifican el algoritmo de reducción específico que se usará para el operador de reducción DirectML (como se describe en [la DML_REDUCE_OPERATOR_DESC estructura](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Especifica el tipo de datos de los valores de un tensor. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Especifica opciones adicionales en una descripción de tensor. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifica un tipo de descripción de tensor. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)