---
description: Identifica los datos de memoria.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY estructura (D3dx9xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072807"
---
# <a name="d3dxf_fileloadmemory-structure"></a>Estructura FILELOADMEMORY de D3DXF \_

Identifica los datos de memoria.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Members

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a un bloque de memoria que se va a cargar.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del bloque de memoria que se va a cargar, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura identifica los datos que se cargarán desde la memoria cuando una aplicación use el [**método CreateEnumObject**](id3dxfile--createenumobject.md) y especifica la marca D3DXF \_ FILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de archivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
