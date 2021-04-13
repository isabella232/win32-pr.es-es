---
title: MPSCAN_DATA estructura (MpClient. h)
description: Examinar los datos pasados a la devolución de llamada.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493060"
---
# <a name="mpscan_data-structure"></a>\_Estructura de datos MPSCAN

Examinar los datos pasados a la devolución de llamada.

Esta estructura contiene estadísticas acumuladas de recursos y amenazas. Estos campos de STAT siempre son válidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ScanType**
</dt> <dd>

Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**

</dd> <dd>

Tipo de examen.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Información de recursos. Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **\_ estadísticas de MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Estadísticas acumulativas relacionadas con recursos.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas de amenazas con finalizaciones de análisis correctas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**estadísticas de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> <dt>

[**estadísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





