---
title: Constantes de DirectML
description: Las constantes siguientes se declaran en `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670215"
---
# <a name="directml-constants"></a>Constantes de DirectML

Las constantes siguientes se declaran en `DirectML.h` .

| Constante | Value | Descripción |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Los DirectML de tamaño máximo admiten un máximo de 5 dimensiones para el DML_FEATURE_LEVEL_3_0 de < de DML_TARGET_VERSION. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Los DirectMLs de tamaño máximo admiten un máximo de 8 dimensiones para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Los búferes temporales y persistentes deben tener una dirección base que se alinee con 256 bytes. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Los búferes temporales y persistentes deben tener una dirección base que se alinee con 256 bytes. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Los separadores de búfer tienen un requisito de alineación de dirección base mínimo de 16 bytes. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | D3D12. h |

## <a name="see-also"></a>Vea también

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
