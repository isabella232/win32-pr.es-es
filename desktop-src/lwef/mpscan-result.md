---
title: MPSCAN_RESULT estructura (MpClient.h)
description: Resultados de un examen.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT estructura heredada de Windows entorno
- PMPSCAN_RESULT puntero de estructura Legacy Windows Environment Features
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
ms.openlocfilehash: a41efd40529976d4b7fe639c4907729ed39ae261f5ac644faf1a36e1a213a97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747156"
---
# <a name="mpscan_result-structure"></a>Estructura DE RESULTADOS de MPSCAN \_

Resultados de un examen.

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

Tipo: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

</dd> <dd>

Tipo de examen. Vea [**MPSCAN \_ TYPE**](mpscan-type.md).

</dd> <dt>

**Origen**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origen del examen, como el usuario o el sistema iniciado. Vea [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificador de examen.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Hora de inicio del examen.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Hora de finalización del examen.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas relacionadas con amenazas. Consulte [**MPTHREAT \_ STATS**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Estadísticas relacionadas con recursos. Consulte [**MPRESOURCE \_ STATS**](mpresource-stats.md).

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión de la firma usada para el examen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MPRESOURCE \_ STATS**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





