---
description: Especifica los tipos de modos de presentación que se filtrarán.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Estructura D3DDISPLAYMODEFILTER (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f59e2e095f7f0f1c6ee73fc940733e932efaef9af7ec05807ff1b38f35fe5189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751065"
---
# <a name="d3ddisplaymodefilter-structure"></a>D3DDISPLAYMODEFILTER (estructura)

Especifica los tipos de modos de presentación que se filtrarán.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de esta estructura. Siempre debe establecerse en sizeof(D3DDISPLAYMODEFILTER).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato de modo de presentación que se filtrará. Vea [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Si la ordenación de la línea de digitalización está entrelazada o progresiva. Vea [**D3DSCANLINEORDERING.**](./d3dscanlineordering.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
