---
description: Describe un búfer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC estructura (D3D9Types. h)
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
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003846"
---
# <a name="d3dindexbuffer_desc-structure"></a>D3DINDEXBUFFER \_ DESC (estructura)

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

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie de los datos del búfer de índice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como un búfer de índice.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinación de una o varias de las marcas siguientes, especificando el uso de este recurso.



| Value                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Se establece para indicar que el contenido del búfer de índice nunca requerirá un recorte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ dinámico**</dt> </dl>                                  | Se establece para indicar que el búfer de índice requiere el uso de memoria dinámica. Esto resulta útil para los controladores porque les permite decidir dónde colocar el búfer. En general, los búferes de índice estáticos se colocan en la memoria de vídeo y los búferes de índice dinámicos se colocan en la memoria AGP. Tenga en cuenta que no hay ningún uso estático independiente; Si no especifica D3DUSAGE Dynamic, \_ el búfer de índice se convierte en estático. D3DUSAGE \_ Dynamic se aplica estrictamente a través de las \_ marcas de bloqueo D3DLOCK discard y D3DLOCK \_ NOOVERWRITE. Como resultado, D3DLOCK \_ discard y D3DLOCK \_ NOOVERWRITE solo son válidos en los búferes de índice creados con D3DUSAGE \_ Dynamic; no son marcas válidas en los búferes de vértices estáticos.<br/> Para obtener más información sobre el uso de búferes de índice dinámicos, vea [usar búferes dinámicos y de índice](performance-optimizations.md).<br/> Tenga en cuenta que \_ no se puede especificar D3DUSAGE Dynamic en búferes de índice administrados. Para obtener más información, vea [administrar recursos (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Se establece para indicar si el búfer de índice se va a utilizar para dibujar primitivas de orden superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Se establece para indicar si el búfer de índice se va a utilizar para dibujar N revisiones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**\_Puntos D3DUSAGE**</dt> </dl>                                     | Se establece para indicar cuándo se va a utilizar el búfer de índice para los sprites de punto de dibujo o listas de puntos indizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Se establece para indicar que el búfer se va a utilizar con el procesamiento de software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informa al sistema de que la aplicación solo escribe en el búfer de índice. El uso de esta marca permite al controlador elegir la mejor ubicación de memoria para operaciones de escritura y representación eficientes. Los intentos de leer desde un búfer de índice creado con esta capacidad pueden dar lugar a un rendimiento degradado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Grupo**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para este búfer de índice.

</dd> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del búfer de índice, en bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Búferes de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
