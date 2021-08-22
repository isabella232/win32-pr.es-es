---
title: MPSCAN_DATA estructura (MpClient.h)
description: Examinar los datos pasados a la devolución de llamada.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA estructura heredada de Windows environment
- PMPSCAN_DATA puntero de estructura heredado de Windows environment
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
ms.openlocfilehash: 5b7c00357b8f104fff42b94de552d52979c364dee64a82bb8e438946319c8c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975995"
---
# <a name="mpscan_data-structure"></a>Estructura DE DATOS DE MPSCAN \_

Examinar los datos pasados a la devolución de llamada.

Esta estructura contiene estadísticas acumulativas de amenazas y recursos. Estos campos de estadísticas siempre son válidos.

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

Tipo: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

</dd> <dd>

Tipo de examen.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Información de recursos. Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Estadísticas acumulativas relacionadas con recursos.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas de amenazas con finalizaciones de examen correctas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> <dt>

[**ESTADÍSTICAS DE MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





