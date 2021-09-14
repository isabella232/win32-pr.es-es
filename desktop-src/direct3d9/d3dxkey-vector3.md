---
description: Describe una clave vectorial para usarla en la animación de fotogramas clave. Especifica un vector en un momento dado. Se usa para las claves de escalado y traducción.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3 estructura (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966756"
---
# <a name="d3dxkey_vector3-structure"></a>Estructura D3DXKEY \_ VECTOR3

Describe una clave vectorial para usarla en la animación de fotogramas clave. Especifica un vector en un momento dado. Se usa para las claves de escalado y traducción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Members

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Marca de tiempo del fotograma clave.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

[**Vector 3D D3DXVECTOR3**](d3dxvector3.md) que proporciona valores de escala o traducción.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
