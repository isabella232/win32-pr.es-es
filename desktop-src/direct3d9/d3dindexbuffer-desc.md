---
description: Describe un búfer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7a25e56ccb9877fad6b370f9ed81c6c7dcf0744a96734b1e17d6dc3abbc0535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804976"
---
# <a name="d3dindexbuffer_desc-structure"></a>Estructura DESC D3DINDEXBUFFER \_

Describe un búfer de índice.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de superficie de los datos del búfer de índice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Miembro del tipo [**enumerado D3DRESOURCETYPE,**](./d3dresourcetype.md) que identifica este recurso como búfer de índice.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinación de una o varias de las marcas siguientes, especificando el uso de este recurso.



| Value                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Se establece para indicar que el contenido del búfer de índice nunca requerirá recorte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ DYNAMIC**</dt> </dl>                                  | Se establece para indicar que el búfer de índice requiere el uso de memoria dinámica. Esto es útil para los controladores porque les permite decidir dónde colocar el búfer. En general, los búferes de índice estáticos se colocan en la memoria de vídeo y los búferes de índice dinámicos se colocan en la memoria de AGP. Tenga en cuenta que no hay ningún uso estático independiente; Si no especifica D3DUSAGE \_ DYNAMIC, el búfer de índice se hace estático. D3DUSAGE DYNAMIC se aplica estrictamente a través de las marcas de bloqueo \_ D3DLOCK DISCARD y \_ D3DLOCK \_ NOOVERWRITE. Como resultado, D3DLOCK DISCARD y D3DLOCK NOOVERWRITE solo son válidos en búferes de índice creados con \_ \_ D3DUSAGE DYNAMIC; no son marcas válidas en búferes de vértice \_ estáticos.<br/> Para obtener más información sobre el uso de búferes de índice dinámicos, vea [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).<br/> Tenga en cuenta que D3DUSAGE \_ DYNAMIC no se puede especificar en búferes de índice administrados. Para obtener más información, vea [Administración de recursos (Direct3D 9).](managing-resources.md)<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Se establece para indicar cuándo se va a usar el búfer de índice para dibujar primitivas de orden alto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Se establece para indicar cuándo se va a usar el búfer de índice para dibujar N revisiones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**PUNTOS D3DUSAGE \_**</dt> </dl>                                     | Se establece para indicar cuándo se va a usar el búfer de índice para dibujar sprites de punto o listas de puntos indizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Se establece para indicar que el búfer se va a usar con el procesamiento de software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informa al sistema de que la aplicación solo escribe en el búfer de índice. El uso de esta marca permite al controlador elegir la mejor ubicación de memoria para realizar operaciones de escritura y representación eficaces. Los intentos de leer desde un búfer de índice que se crea con esta funcionalidad pueden dar lugar a un rendimiento degradado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Grupo**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Miembro del [**tipo enumerado D3DPOOL,**](./d3dpool.md) especificando la clase de memoria asignada para este búfer de índice.

</dd> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del búfer de índice, en bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Búferes de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
