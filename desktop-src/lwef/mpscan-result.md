---
title: MPSCAN_RESULT estructura (MpClient.h)
description: Resultados de un examen.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT estructura heredada de Windows environment
- PMPSCAN_RESULT puntero de estructura heredado Windows características del entorno
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358970"
---
# <a name="mpscan_result-structure"></a>Estructura DE RESULTADOS DE MPSCAN \_

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



## <a name="members"></a>Members

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

Estadísticas relacionadas con amenazas. Vea [**MPTHREAT \_ STATS**](mpthreat-stats.md).

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADÍSTICAS DE MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





