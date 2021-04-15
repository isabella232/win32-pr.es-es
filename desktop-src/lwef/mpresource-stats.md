---
title: MPRESOURCE_STATS estructura (MpClient. h)
description: Estadísticas relacionadas con recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESOURCE_STATS características de entorno heredado de Windows
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
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491549"
---
# <a name="mpresource_stats-structure"></a>MPRESOURCE ( \_ estructura de estadísticas)

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

Progreso aproximado para el examen en ppm (partes por millón). Establezca en **MPPROGRESS \_ no válido** si la información de progreso no está disponible.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de procesos examinados.

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

Número de bytes examinados para los archivos.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





