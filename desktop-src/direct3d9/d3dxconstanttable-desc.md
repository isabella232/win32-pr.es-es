---
description: Una descripción de la tabla de constantes.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: D3DXCONSTANTTABLE_DESC estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821151"
---
# <a name="d3dxconstanttable_desc-structure"></a>D3DXCONSTANTTABLE \_ DESC (estructura)

Una descripción de la tabla de constantes.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Creador**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre del creador de la tabla de constantes.

</dd> <dt>

**Versión**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versión del sombreador.

</dd> <dt>

**Constantes**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de constantes en la tabla de constantes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 
