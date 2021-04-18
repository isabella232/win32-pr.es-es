---
description: Identifica los datos de recursos.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE estructura (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698249"
---
# <a name="d3dxf_fileloadresource-structure"></a>D3DXF \_ estructura FILELOADRESOURCE

Identifica los datos de recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
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

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a una cadena que especifica el nombre del recurso que se va a cargar. Por ejemplo, si el recurso es una malla, este miembro debe especificar el nombre del archivo de malla.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntero a una cadena que especifica el tipo definido por el usuario que identifica el recurso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el método [**CreateEnumObject**](id3dxfile--createenumobject.md) y especifica la marca [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de archivos de D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
