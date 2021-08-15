---
title: MPSTATUS_INFO estructura (MpClient.h)
description: Información de estado del administrador de protección contra malware.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO estructura heredada de Windows environment
- PMPSTATUS_INFO puntero de estructura heredado de Windows environment
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb93bd15fe05955c9e8d87828d4b94b08e3d577659c629b52b3f908cb045ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883306"
---
# <a name="mpstatus_info-structure"></a>Estructura DE INFORMACIÓN DE MPSTATUS \_

Información de estado del administrador de protección contra malware.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ProductStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado general del producto. Se trata de una combinación de marcas de bits de [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Tipo: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Resultados del último examen por parte del administrador de protección contra malware. Vea [**MPSCAN \_ RESULT**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Tipo: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Resultados del último examen completo por parte del administrador de protección contra malware. Vea [**MPSCAN \_ RESULT**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas de amenazas activas. Vea [**MPTHREAT \_ STATS**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Tipo: **[**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md) \[ MP THREAT STAT MAX \_ \_ \_ \_ VALUE+1\]**

</dd> <dd>

Datos de estadísticas de amenazas adicionales, como el número de amenazas. Vea [**DATOS DE ESTADÍSTICAS DE MPTHREAT \_ \_**](mpthreat-stats-data.md).

</dd> <dt>

**Componente**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ STATUS**](mpcomponent-status.md) \[ MPCOMPONENT \_ MAXVALUE+1\]**

</dd> <dd>

Matriz de estados para varios componentes. Use un valor de la [**enumeración MPCOMPONENT \_ ID**](mpcomponent-id.md) como índice en la matriz.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Marca de tiempo de expiración del producto en UNC. Esto solo es válido si se establece el estado de expiración.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Id. de \_ MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**ESTADO \_ DE MPCOMPONENT**](mpcomponent-status.md)
</dt> <dt>

[**MPSCAN \_ RESULT**](mpscan-result.md)
</dt> <dt>

[**MARCA \_ MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md)
</dt> <dt>

[**DATOS DE \_ ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats-data.md)
</dt> </dl>

 

 





