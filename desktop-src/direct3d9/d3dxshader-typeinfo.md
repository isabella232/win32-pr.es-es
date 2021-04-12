---
description: Una estructura auxiliar que contiene información de tipo de miembro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: D3DXSHADER_TYPEINFO estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362542"
---
# <a name="d3dxshader_typeinfo-structure"></a>D3DXSHADER \_ TYPEINFO (estructura)

Una estructura auxiliar que contiene información de tipo de miembro.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Clase**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo de objeto de sombreador. Vea [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo de datos. Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de filas de la matriz (matrices).

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de columnas (vectores y matrices).

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensión de la matriz.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de miembros de estructura.

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de información de miembros de estructura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] . Vea [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información de tipo forma parte de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
