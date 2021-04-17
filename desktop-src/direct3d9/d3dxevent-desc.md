---
description: Describe un evento de animación.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC estructura (D3dx9anim. h)
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
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698251"
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

Tipo: **[ **D3DXEVENT \_ Type**](./d3dxevent-type.md)**

</dd> <dd>

Tipo de evento, tal y como se define en [**D3DXEVENT \_ Type**](./d3dxevent-type.md).

</dd> <dt>

**Dar**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de la pista de eventos.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Hora de inicio del evento en tiempo global.

</dd> <dt>

**Duration**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Duración del evento en tiempo global.

</dd> <dt>

**Transición**
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**

</dd> <dd>

Estilo de transición del evento, tal y como se define en [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponderación del seguimiento del evento.

</dd> <dt>

**Velocidad**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocidad de seguimiento para el evento.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Seguimiento de la posición del evento.

</dd> <dt>

**Habilitar**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Habilitar marca.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
