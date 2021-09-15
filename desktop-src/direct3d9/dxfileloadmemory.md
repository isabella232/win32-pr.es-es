---
description: Identifica los datos de memoria. En desuso.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Estructura DXFILELOADMEMORY (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465386"
---
# <a name="dxfileloadmemory-structure"></a>Estructura DXFILELOADMEMORY

Identifica los datos de memoria. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Members

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a un bloque de memoria que se va a cargar.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del bloque de memoria que se va a cargar, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el [**método CreateEnumObject**](idirectxfile--createenumobject.md) y especifica DXFILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXFile.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de archivo X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Constantes DXFILE](dxfile.md)
</dt> </dl>

 

 
