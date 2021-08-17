---
description: Identifica los datos comprimidos de animación de fotogramas clave.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Estructura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh.h)
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
ms.openlocfilehash: 41c64ae7bb2ca4acf87e1b63de90f2ccfc78e8d769adf334aa1f68b9bf79de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518578"
---
# <a name="xfilecompressedanimationset-structure"></a>Estructura XFILECOMPRESSEDANIMATIONSET

Identifica los datos comprimidos de animación de fotogramas clave.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de tics de fotograma clave de animación que se producen por segundo.

</dd> <dt>

**PlaybackType**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo del bucle de reproducción del conjunto de animación. Vea [**D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño mínimo del búfer, en bytes, necesario para contener datos comprimidos de animación de fotogramas clave. El valor es igual a ( ( CompressedBlockSize + 3 ) / 4 ).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de archivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
