---
description: Estructura de aplicación auxiliar para administrar una tabla de constantes de sombreador. Esto también se puede hacer mediante ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717740"
---
# <a name="d3dxshader_constanttable-structure"></a>D3DXSHADER \_ estructura CONSTANTTABLE

Estructura de aplicación auxiliar para administrar una tabla de constantes de sombreador. Esto también se puede hacer mediante [**ID3DXConstantTable**](id3dxconstanttable.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de la estructura. Vea la sección Comentarios.

</dd> <dt>

**Creador**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el nombre del creador.

</dd> <dt>

**Versión**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versión del sombreador.

</dd> <dt>

**Constantes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de constantes.

</dd> <dt>

**ConstantInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de información constante, constantes de D3DXSHADER \_ CONSTANTINFO \[  \] . Vea [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

[D3DXSHADER](d3dxshader-flags.md) marca las marcas que se usan para compilar el sombreador.

</dd> <dt>

**Target**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento en la cadena que contiene el destino.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información de constantes del sombreador se incluye en una tabla de comentarios delimitada por tabuladores. Todos los desplazamientos se miden en bytes desde el principio de la estructura. Las entradas de la tabla Constant se ordenan por creador en orden ascendente.

Una tabla de constantes de sombreador se puede administrar con las interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) . Como alternativa, puede administrar la tabla de constantes con **D3DXSHADER \_ CONSTANTTABLE**.

Este miembro de tamaño se inicializa a menudo con lo siguiente:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
