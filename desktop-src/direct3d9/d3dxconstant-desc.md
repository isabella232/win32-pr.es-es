---
description: Descripción de una constante en una tabla de constantes.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC estructura (D3dx9shader. h)
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
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718446"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT \_ DESC (estructura)

Descripción de una constante en una tabla de constantes.

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

Tipo: **[ **D3DXREGISTER \_ set**](./d3dxregister-set.md)**

</dd> <dd>

Tipo de datos constante. Vea [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice de base cero de la constante de la tabla.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de registros que contienen datos.

</dd> <dt>

**Clase**
</dt> <dd>

Type: **[ **\_ clase D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Clase de parámetro. Vea [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parámetro. Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de filas.

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de columnas.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos de la matriz.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de subparámetros de miembro de estructura.

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de los datos en número de bytes.

</dd> <dt>

**DefaultValue**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero al valor predeterminado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
