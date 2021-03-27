---
title: 'RWByteAddressBuffer:: Load4 (uint, uint) (función)'
description: Obtiene cuatro valores y devuelve el estado de la operación.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
keywords:
- Load4 de función HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793743"
---
# <a name="load4uintuint-function"></a>Load4 (uint, uint) (función)

Obtiene cuatro valores y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **uint**

Ubicación del búfer.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint4**

Cuatro valores.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load4](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 