---
description: Describe una clave de devolución de llamada para su uso en la animación de fotogramas clave.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: D3DXKEY_CALLBACK estructura (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f488445bbb018b62445ff802abcf5a82c22b4e31c9d71618e61437efd5e36a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123073"
---
# <a name="d3dxkey_callback-structure"></a>Estructura de devolución de llamada \_ D3DXKEY

Describe una clave de devolución de llamada para su uso en la animación de fotogramas clave.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Marca de tiempo del fotograma clave.

</dd> <dt>

**pCallbackData**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a datos de devolución de llamada de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
