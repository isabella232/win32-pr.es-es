---
description: Descripción de una constante en una tabla constante.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC estructura (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: bdb3b8276711f3165c0c138155eb6e628c19a124d6f9301de7638e5be24d1c1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952455"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT \_ DESC (estructura)

Descripción de una constante en una tabla constante.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de la constante.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Tipo: **[ **D3DXREGISTER \_ SET**](./d3dxregister-set.md)**

</dd> <dd>

Tipo de datos constante. Vea [**D3DXREGISTER \_ SET**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice de base cero de la constante de la tabla.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de registros que contienen datos.

</dd> <dt>

**Clase**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ (CLASE)**](./d3dxparameter-class.md)**

</dd> <dd>

Clase de parámetro. Vea [**D3DXPARAMETER \_ (CLASE).**](./d3dxparameter-class.md)

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parámetro. Vea [**D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de filas.

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de columnas.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos de la matriz.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de subámetros de miembro de estructura.

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de datos en número de bytes.

</dd> <dt>

**Defaultvalue**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero al valor predeterminado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
