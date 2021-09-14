---
description: Describe una clave de cuaternión para su uso en la animación de fotogramas clave. Una clave de cuaternión es un valor de cuaternión en un momento dado.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: D3DXKEY_QUATERNION estructura (D3dx9anim.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966759"
---
# <a name="d3dxkey_quaternion-structure"></a>D3DXKEY \_ QUATERNION (estructura)

Describe una clave de cuaternión para su uso en la animación de fotogramas clave. Una clave de cuaternión es un valor de cuaternión en un momento dado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Members

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de tiempo.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

[**Cuaternión D3DXQUATERNION**](d3dxquaternion.md) que proporciona valores de rotación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
