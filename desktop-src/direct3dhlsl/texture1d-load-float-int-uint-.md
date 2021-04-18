---
title: 'Texture1D:: Load (int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture1D:: Load (int, int, uint) (función)'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986470"
---
# <a name="texture1dloadintintuint-function"></a>Texture1D:: Load (int, int, uint) (función)

Lee los datos de textura y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **int**

Las coordenadas de textura.

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Tipo: **int**

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture1D**](sm5-object-texture1d.md) .

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cargar métodos](texture1d-load.md)
</dt> <dt>

[**Texture1D**](sm5-object-texture1d.md)
</dt> </dl>

 

 
