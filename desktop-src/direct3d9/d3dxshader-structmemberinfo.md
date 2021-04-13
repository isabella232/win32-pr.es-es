---
description: Estructura auxiliar que contiene información sobre la estructura de los miembros.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362524"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>D3DXSHADER \_ estructura STRUCTMEMBERINFO

Estructura auxiliar que contiene información sobre la estructura de los miembros.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el nombre del miembro de estructura.

</dd> <dt>

**Requerida**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información de tipo. Consulte [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
