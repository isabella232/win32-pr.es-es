---
description: Describe una pista de animación y especifica la combinación de peso, velocidad y posición de la pista en un momento dado.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC estructura (D3dx9anim.h)
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
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731122"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK \_ DESC (estructura)

Describe una pista de animación y especifica la combinación de peso, velocidad y posición de la pista en un momento dado.

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

Tipo: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo de prioridad, tal como se define [**en D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md).

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de peso. El peso determina la proporción de esta pista que se va a combinar con otras pistas.

</dd> <dt>

**Velocidad**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de velocidad. Esto se usa de forma similar a un multiplicador para escalar el período de la pista.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de hora de la pista, en el período de tiempo local de su conjunto de animación actual.

</dd> <dt>

**Habilitación**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Realice un seguimiento de la habilitación o deshabilitación. Para habilitarlo, establezca en **TRUE.** Para deshabilitarlo, establezca en **FALSE.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las pistas con la misma prioridad se combinan y los dos valores resultantes se mezclan con el factor de combinación de prioridad. Una pista debe tener un conjunto de animaciones (almacenado por separado) asociado a él.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
