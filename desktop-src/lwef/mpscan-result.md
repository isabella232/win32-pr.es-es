---
title: MPSCAN_RESULT estructura (MpClient. h)
description: Los resultados de un examen.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_RESULT características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274552"
---
# <a name="mpscan_result-structure"></a>Estructura del resultado de MPSCAN \_

Los resultados de un examen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ScanType**
</dt> <dd>

Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**

</dd> <dd>

Tipo de examen. Consulte [**\_ tipo de MPSCAN**](mpscan-type.md).

</dd> <dt>

**Origen**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origen de la exploración, como usuario o sistema iniciado. Vea [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificador de examen.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Hora de inicio del examen.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Hora de finalización del examen.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas relacionadas con amenazas. Consulte [**\_ estadísticas de MPTHREAT**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **\_ estadísticas de MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Estadísticas relacionadas con recursos. Consulte [**\_ estadísticas de MPRESOURCE**](mpresource-stats.md).

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión de la firma utilizada para el examen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**estadísticas de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**estadísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





