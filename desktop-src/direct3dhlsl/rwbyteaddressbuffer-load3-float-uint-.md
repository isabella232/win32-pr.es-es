---
title: 'RWByteAddressBuffer:: Load3 (uint, uint) (función)'
description: Obtiene tres valores y devuelve el estado de la operación.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
keywords:
- Load3 de función HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359253"
---
# <a name="load3uintuint-function"></a>Load3 (uint, uint) (función)

Obtiene tres valores y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
uint3 Load3(
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

Tipo: **UInt3**

Tres valores.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load3](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 