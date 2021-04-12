---
description: Describe una clave cuaternión para su uso en la animación de fotogramas clave. Una clave cuaternión es un valor cuaternión en un momento dado.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: D3DXKEY_QUATERNION estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362561"
---
# <a name="d3dxkey_quaternion-structure"></a>\_Estructura del CUATERNIÓN D3DXKEY

Describe una clave cuaternión para su uso en la animación de fotogramas clave. Una clave cuaternión es un valor cuaternión en un momento dado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de tiempo.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

Cuaternión [**D3DXQUATERNION**](d3dxquaternion.md) que proporciona valores de rotación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
