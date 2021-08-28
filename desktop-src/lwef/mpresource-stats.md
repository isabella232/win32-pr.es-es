---
title: MPRESOURCE_STATS estructura (MpClient.h)
description: Estadísticas relacionadas con recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS estructura heredada de Windows environment
- PMPRESOURCE_STATS puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72a21bf0ec020c1fc2cf5ba1394b4cd5ed04dc32721a4aac9f8349034907b49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848475"
---
# <a name="mpresource_stats-structure"></a>Estructura MPRESOURCE \_ STATS

Estadísticas relacionadas con recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PPMProgress**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Progreso aproximado del examen en ppm (partes por millón). Establezca en **MPPROGRESS \_ INVALID si** la información de progreso no está disponible.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de procesos analizados.

</dd> <dt>

**FileCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de archivos examinados.

</dd> <dt>

**FileBytesCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de bytes examinados en busca de archivos.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de RegKeys examinados.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **UINT64 \[ 4 \]**

</dd> <dd>

Campos reservados para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





