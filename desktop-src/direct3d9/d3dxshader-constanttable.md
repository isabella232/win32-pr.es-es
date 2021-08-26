---
description: Estructura auxiliar para administrar una tabla constante de sombreador. Esto también se puede hacer mediante ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE estructura (D3dx9shader.h)
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
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027295"
---
# <a name="d3dxshader_constanttable-structure"></a>Estructura CONSTANTTABLE de D3DXSHADER \_

Estructura auxiliar para administrar una tabla constante de sombreador. Esto también se puede hacer mediante [**ID3DXConstantTable**](id3dxconstanttable.md).

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

Matriz de información constante, constantes CONSTANTINFO de D3DXSHADER \_ \[  \] . Vea [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Marcas [D3DXSHADER usadas](d3dxshader-flags.md) para compilar el sombreador.

</dd> <dt>

**Target**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento en la cadena que contiene el destino.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La información constante del sombreador se incluye en una tabla de comentarios delimitada por tabulaciones. Todos los desplazamientos se miden en bytes desde el principio de la estructura . Las entradas de la tabla constante se ordenan por Creator en orden ascendente.

Una tabla constante de sombreador se puede administrar con las interfaces [**ID3DXConstantTable.**](id3dxconstanttable.md) Como alternativa, puede administrar la tabla constante con **D3DXSHADER \_ CONSTANTTABLE**.

Este miembro de tamaño se inicializa a menudo con lo siguiente:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
