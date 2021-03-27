---
title: CheckAccessFullyMapped función)
description: Determina si todos los valores de una operación de ejemplo, recopilación o carga han tenido acceso a mosaicos asignados en un recurso en mosaico.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped de función HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793179"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped función)

Determina si todos los valores de una operación de **ejemplo**, **recopilación** o **carga** han tenido acceso a mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).

## <a name="syntax"></a>Sintaxis

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ de de\]
</dt> <dd>

Tipo: **\_ solo uint**

Valor de estado que se devuelve de una operación de **ejemplo**, de **recopilación** o de **carga** . Dado que no puede tener acceso directamente a este valor de estado, debe pasarlo a **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve un valor **booleano** que indica si todos los valores de una operación de **ejemplo**, **recopilación** o **carga** han tenido acceso a mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Devuelve **true** si todos los valores de la operación han tenido acceso a los mosaicos asignados; de lo contrario, devuelve **false** si se tomó algún valor de un mosaico sin asignar.

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 