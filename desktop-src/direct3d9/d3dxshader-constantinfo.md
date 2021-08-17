---
description: Estructura CONSTANTINFO de D3DXSHADER \_
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: D3DXSHADER_CONSTANTINFO estructura (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 34a9238ac7ab401a25874d65390ccfacb4dba68a9ccc4438500a1171e25e5e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122835"
---
# <a name="d3dxshader_constantinfo-structure"></a>Estructura CONSTANTINFO de D3DXSHADER \_

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información constante.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Conjunto de registros. Vea [**D3DXREGISTER \_ SET**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice de registro.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de registros.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información [**\_ TYPEINFO de D3DXSHADER.**](d3dxshader-typeinfo.md)

</dd> <dt>

**Defaultvalue**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el valor predeterminado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
