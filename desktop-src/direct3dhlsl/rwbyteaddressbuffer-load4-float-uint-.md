---
title: Función RWByteAddressBuffer::Load4(uint,uint)
description: Obtiene cuatro valores y devuelve el estado de la operación.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
keywords:
- Función Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f64fe84f17ee4cc1fed25b870b2142b474e753fa41e82cd0d385c9ef185ee9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672115"
---
# <a name="load4uintuint-function"></a>Función Load4(uint,uint)

Obtiene cuatro valores y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **uint**

Ubicación del búfer.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación Sample **,** **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint4**

Cuatro valores.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load4](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 