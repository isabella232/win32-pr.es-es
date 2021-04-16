---
description: Identifica los datos de animación de fotogramas clave comprimidos.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Estructura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689868"
---
# <a name="xfilecompressedanimationset-structure"></a>Estructura XFILECOMPRESSEDANIMATIONSET

Identifica los datos de animación de fotogramas clave comprimidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CompressedBlockSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño total, en bytes, de los datos comprimidos en el búfer de datos de animación de fotogramas clave comprimidos.

</dd> <dt>

**TicksPerSec**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de TICs de fotogramas clave de animación que se producen por segundo.

</dd> <dt>

**PlaybackType**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo del bucle de reproducción establecido de la animación. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño mínimo del búfer, en bytes, necesario para contener datos de animación de fotogramas clave comprimidos. El valor es igual a ((CompressedBlockSize + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de archivos de D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
