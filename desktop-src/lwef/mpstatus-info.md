---
title: MPSTATUS_INFO estructura (MpClient. h)
description: Información de estado para el administrador de protección contra malware de.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSTATUS_INFO características de entorno heredado de Windows
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
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801249"
---
# <a name="mpstatus_info-structure"></a>Estructura de información de MPSTATUS \_

Información de estado para el administrador de protección contra malware de.

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

Estado general del producto. Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**

</dd> <dd>

Resultados del último examen por parte del administrador de protección contra malware de. Vea [**el \_ resultado de MPSCAN**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**

</dd> <dd>

Resultados del último examen completo por parte del administrador de protección contra malware. Vea [**el \_ resultado de MPSCAN**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estadísticas de amenazas activas. Consulte [**\_ estadísticas de MPTHREAT**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Type: **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ STAT \_ Max \_ Value + 1\]**

</dd> <dd>

Datos adicionales de estadísticas de amenazas, como el número de amenazas. Consulte [**\_ \_ datos de estadísticas de MPTHREAT**](mpthreat-stats-data.md).

</dd> <dt>

**Componente**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MAXVALUE + 1\]**

</dd> <dd>

Una matriz de Estados para varios componentes. Use un valor de la enumeración [**MPCOMPONENT \_ ID**](mpcomponent-id.md) como un índice en la matriz.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Marca de tiempo de expiración del producto en UNC. Esto solo es válido si se ha establecido el estado de expiración.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**identificador de MPCOMPONENT \_**](mpcomponent-id.md)
</dt> <dt>

[**Estado de MPCOMPONENT \_**](mpcomponent-status.md)
</dt> <dt>

[**resultado de MPSCAN \_**](mpscan-result.md)
</dt> <dt>

[**\_marca MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**estadísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> <dt>

[**datos de estadísticas de MPTHREAT \_ \_**](mpthreat-stats-data.md)
</dt> </dl>

 

 





