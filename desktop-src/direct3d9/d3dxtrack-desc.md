---
description: Describe una pista de animación y especifica el peso, la velocidad y la posición de fusión de la pista en un momento dado.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717727"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK \_ DESC (estructura)

Describe una pista de animación y especifica el peso, la velocidad y la posición de fusión de la pista en un momento dado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Prioridad**
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo de prioridad, tal y como se define en [**D3DXPRIORITY \_ Type**](./d3dxpriority-type.md).

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de peso. El peso determina la proporción de esta pista para mezclar con otras pistas.

</dd> <dt>

**Velocidad**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de velocidad. Se utiliza de forma similar a un multiplicador para escalar el período de la pista.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de hora de la pista, en el intervalo de tiempo local de su conjunto de animaciones actual.

</dd> <dt>

**Habilitar**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Seguimiento habilitar/deshabilitar. Para habilitarlo, establézcalo en **true**. Para deshabilitar, establezca en **false**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las pistas con la misma prioridad se mezclan juntas y los dos valores resultantes se combinan con el factor de mezcla de prioridad. Una pista debe tener una animación establecida (almacenada por separado) asociada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
