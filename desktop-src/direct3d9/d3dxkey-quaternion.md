---
description: Describe una clave de cuaternión para usarla en la animación de fotogramas clave. Una clave de cuaternión es un valor de cuaternión en un momento dado.
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
ms.openlocfilehash: 088361835c8a15890887fef05cfa0a196e294406bf0c736d332f1a5ba1879740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986605"
---
# <a name="d3dxkey_quaternion-structure"></a>D3DXKEY \_ QUATERNION (estructura)

Describe una clave de cuaternión para usarla en la animación de fotogramas clave. Una clave de cuaternión es un valor de cuaternión en un momento dado.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
