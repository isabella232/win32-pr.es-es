---
title: Constantes de DirectML
description: Las siguientes constantes se declaran en `DirectML.h` .
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
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803406"
---
# <a name="directml-constants"></a>Constantes de DirectML

Las siguientes constantes se declaran en `DirectML.h` .

| Constante | Value | Descripción |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Los tensores de DirectML admiten un máximo de 5 dimensiones para DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Los tensores de DirectML admiten un máximo de 8 dimensiones para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Los búferes temporales y persistentes deben tener una dirección base alineada con 256 bytes. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Los búferes temporales y persistentes deben tener una dirección base alineada con 256 bytes. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Los tensores de búfer tienen un requisito mínimo de alineación de direcciones base de 16 bytes. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | DirectML.h |

## <a name="see-also"></a>Consulta también

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
