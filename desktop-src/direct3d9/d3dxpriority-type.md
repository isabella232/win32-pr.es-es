---
description: Define el tipo de prioridad al que se asigna una pista de animación.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Enumeración D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424376"
---
# <a name="d3dxpriority_type-enumeration"></a>\_Enumeración de tipo D3DXPRIORITY

Define el tipo de prioridad al que se asigna una pista de animación.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ bajo**
</dt> <dd>

La pista debe combinarse con todas las pistas de prioridad baja antes de que la mezcla de prioridad baja se mezcle con la mezcla de prioridad alta.

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ alto**
</dt> <dd>

La pista debe combinarse con todas las pistas de prioridad alta antes de que la mezcla de prioridad alta se mezcle con la mezcla de prioridad baja.

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las pistas con la misma prioridad se mezclan juntas y los dos valores resultantes se combinan con el factor de mezcla de prioridad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




