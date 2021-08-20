---
description: Estadísticas de recursos recopiladas por ResourceManager D3DDEVINFO \_ cuando se usa el mecanismo de consulta asincrónico.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Estructura D3DRESOURCESTATS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc992c5b8246ce302cda8924b8521c923575c8914c83b35c8c1e789e4bc1c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527477"
---
# <a name="d3dresourcestats-structure"></a>Estructura D3DRESOURCESTATS

Estadísticas de recursos recopiladas por [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) cuando se usa el mecanismo de consulta asincrónico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**bThrashing**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Indica si se está produciendo el thrashing.

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número aproximado de bytes descargados por el administrador de recursos.

</dd> <dt>

**NumEvicts**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos expulsados.

</dd> <dt>

**NumVidCreates**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos creados en la memoria de vídeo.

</dd> <dt>

**LastPri**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Prioridad del último objeto expulsado.

</dd> <dt>

**NumUsed**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos establecidos en el dispositivo.

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos establecidos en el dispositivo, que ya están en memoria de vídeo.

</dd> <dt>

**WorkingSet**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos en la memoria de vídeo.

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes en memoria de vídeo.

</dd> <dt>

**TotalManaged**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de objetos administrados.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de bytes de objetos administrados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Notificación asincrónica (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
