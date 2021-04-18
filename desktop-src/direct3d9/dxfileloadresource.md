---
description: Identifica los datos de recursos. En desuso.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Estructura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649427"
---
# <a name="dxfileloadresource-structure"></a>Estructura DXFILELOADRESOURCE

Identifica los datos de recursos. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**hModule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador del módulo que contiene el recurso que se va a cargar. Si este miembro es **null**, el recurso se debe adjuntar al archivo ejecutable que lo usará.

</dd> <dt>

**lpName**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a una cadena que especifica el nombre del recurso que se va a cargar. Por ejemplo, si el recurso es una malla, este miembro debe especificar el nombre del archivo de malla.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a una cadena que especifica el tipo definido por el usuario que identifica el recurso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el método [**CreateEnumObject**](idirectxfile--createenumobject.md) y especifica DXFILELOAD \_ FROMRESOURCE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de archivos X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Constantes de DXFILE](dxfile.md)
</dt> </dl>

 

 
