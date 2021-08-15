---
title: MPCALLBACK_DATA estructura (MpClient.h)
description: Datos pasados a la función de devolución de llamada.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA estructura heredada de Windows environment
- PMPCALLBACK_DATA puntero de estructura heredado Windows características del entorno
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883657"
---
# <a name="mpcallback_data-structure"></a>Estructura DE DATOS MPCALLBACK \_

Datos pasados a la función de devolución de llamada.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Notificar**
</dt> <dd>

Tipo: **[ **MPNOTIFY**](mpnotify.md)**

</dd> <dd>

Cambie la notificación a informe.

</dd> <dt>

**Hresult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de error, en caso de error interno.

</dd> <dt>

**Timestamp**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Marca de tiempo actual.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **MPCALLBACK \_ TYPE**](mpcallback-type.md)**

</dd> <dd>

Tipo de datos especial de devolución de llamada.

</dd> <dt>

**Datos**
</dt> <dd>

Datos especiales de devolución de llamada. El puntero a la estructura adecuada depende del valor de **Type**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ STATUS**. Vea [**DATOS DE MPSTATUS \_**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Tipo: **PMPSCAN \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ SCAN**. Vea [**MPSCAN \_ DATA**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Tipo: **PMPCLEAN \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ CLEAN**. Vea [**MPCLEAN \_ DATA**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Tipo: **PMPCLEAN \_ PRECHECK \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ PRECHECK**. Consulte [**MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Tipo: **PMPTHREAT \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ THREAT**. Vea [**MPTHREAT \_ DATA**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Tipo: **PMPSIGUPDATE \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ SIGUPDATE**. Vea [**MPSIGUPDATE \_ DATA**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Tipo: **PMPSAMPLE \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ SAMPLE**. Vea [**MPSAMPLE \_ DATA**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Tipo: **PMPRESERVED \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ RESERVED**. Vea [**MPRESERVED \_ DATA**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Tipo: **PMPCONFIGURATION \_ DATA**

</dd> <dd>

Cuando escriba  ==  **MPCALLBACK \_ CONFIGURATION \_ NOTIFICATION**. Vea [**DATOS DE MPCONFIGURATION \_**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Tipo: **PMPFASTPATH \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ FASTPATH**. Vea [**MPFASTPATH \_ DATA**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Tipo: **PMPEXPIRATION \_ DATA**

</dd> <dd>

Cuando escriba  ==  **MPCALLBACK \_ PRODUCT \_ EXPIRATION**. Vea [**MPEXPIRATION \_ DATA**](mpexpiration-data.md).

</dd> <dt>

**pIQUEPrivateData**
</dt> <dd>

Tipo: **DATOS PRIVADOS de \_ \_ PMPIQUE**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ NIS \_ PRIVATE.** Consulte [**DATOS PRIVADOS \_ DE \_ MPZON.**](mpnis-private-data.md)

</dd> <dt>

**pHealthData**
</dt> <dd>

Tipo: **PMPHEALTH \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ HEALTH**. Vea [**MPHEALTH \_ DATA**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Tipo: **PMPENDOFLIFE \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ ENDOFLIFE**. Vea [**MPENDOFLIFE \_ DATA**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Tipo: **PMPMALWARETOAST \_ DATA**

</dd> <dd>

Cuando **escriba**  ==  **MPCALLBACK \_ MALWARETOAST**. Vea [**MPMALWARETOAST \_ DATA**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO \_ MPCALLBACK**](mpcallback-type.md)
</dt> <dt>

[**DATOS \_ MPCLEAN**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md)
</dt> <dt>

[**DATOS DE \_ MPCONFIGURATION**](mpconfiguration-data.md)
</dt> <dt>

[**DATOS DE \_ MPENDOFLIFE**](mpendoflife-data.md)
</dt> <dt>

[**DATOS DE \_ MPEXPIRATION**](mpexpiration-data.md)
</dt> <dt>

[**DATOS DE \_ MPFASTPATH**](mpfastpath-data.md)
</dt> <dt>

[**DATOS DE \_ MPHEALTH**](mphealth-data.md)
</dt> <dt>

[**DATOS MPMALWARETOAST \_**](mpmalwaretoast-data.md)
</dt> <dt>

[**DATOS PRIVADOS DE MPNIS \_ \_**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**DATOS ALMACENADOS EN \_ MPRESERVED**](mpreserved-data.md)
</dt> <dt>

[**DATOS DE \_ MPSAMPLE**](mpsample-data.md)
</dt> <dt>

[**DATOS \_ DE MPSCAN**](mpscan-data.md)
</dt> <dt>

[**DATOS DE \_ MPSIGUPDATE**](mpsigupdate-data.md)
</dt> <dt>

[**DATOS DE \_ MPSTATUS**](mpstatus-data.md)
</dt> <dt>

[**DATOS DE \_ MPTHREAT**](mpthreat-data.md)
</dt> </dl>

 

 





