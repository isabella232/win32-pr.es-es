---
description: Describe un evento de animación.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC estructura (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731813"
---
# <a name="d3dxevent_desc-structure"></a>D3DXEVENT \_ DESC (estructura)

Describe un evento de animación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXEVENT \_ TYPE**](./d3dxevent-type.md)**

</dd> <dd>

Tipo de evento, tal como se define en [**D3DXEVENT \_ TYPE**](./d3dxevent-type.md).

</dd> <dt>

**Pista**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de seguimiento de eventos.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Hora de inicio del evento en hora global.

</dd> <dt>

**Duración**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Duración del evento en tiempo global.

</dd> <dt>

**Transición**
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

</dd> <dd>

Estilo de transición del evento, tal como se define en [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Realizar un seguimiento del peso del evento.

</dd> <dt>

**Velocidad**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Realice un seguimiento de la velocidad del evento.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Realizar un seguimiento de la posición del evento.

</dd> <dt>

**Habilitación**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Habilitar marca.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
