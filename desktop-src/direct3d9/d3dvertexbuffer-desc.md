---
description: Describe un búfer de vértices.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: D3DVERTEXBUFFER_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548006"
---
# <a name="d3dvertexbuffer_desc-structure"></a>D3DVERTEXBUFFER \_ DESC (estructura)

Describe un búfer de vértices.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie de los datos del búfer de vértices.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como un búfer de vértice.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinación de una o varias marcas de [**D3DUSAGE**](d3dusage.md) .

</dd> <dt>

**Grupo**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para este búfer de vértices.

</dd> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del búfer de vértices, en bytes.

</dd> <dt>

**FVF**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértice de los vértices de este búfer.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Búferes de vértices (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
