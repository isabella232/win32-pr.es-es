---
title: MPCALLBACK_DATA estructura (MpClient. h)
description: Datos pasados a la función de devolución de llamada.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCALLBACK_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150237"
---
# <a name="mpcallback_data-structure"></a>\_Estructura de datos MPCALLBACK

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

Notificación de cambio a informe.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de error, en caso de un error interno.

</dd> <dt>

**Indicaciones**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Marca de tiempo actual.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **MPCALLBACK \_ Type**](mpcallback-type.md)**

</dd> <dd>

Tipo de datos Especial de devolución de llamada.

</dd> <dt>

**Data**
</dt> <dd>

Datos especiales de devolución de llamada. El puntero a la estructura adecuada depende del valor de **tipo**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Tipo: **PMPSTATUS \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ status**. Vea [**MPSTATUS \_ Data**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Tipo: **PMPSCAN \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ scan**. Vea [**MPSCAN \_ Data**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Tipo: **PMPCLEAN \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ Clean**. Vea [**MPCLEAN \_ Data**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Tipo: **PMPCLEAN \_ comprobar \_ datos**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ precheck**. Vea [**MPCLEAN \_ precheck \_ Data**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Tipo: **PMPTHREAT \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ amenaza**. Vea [**MPTHREAT \_ Data**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Tipo: **PMPSIGUPDATE \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ SIGUPDATE**. Vea [**MPSIGUPDATE \_ Data**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Tipo: **PMPSAMPLE \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **\_ ejemplo de MPCALLBACK**. Vea [**MPSAMPLE \_ Data**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Tipo: **PMPRESERVED \_ Data**

</dd> <dd>

Cuando el **tipo**  ==  **MPCALLBACK está \_ reservado**. Vea [**MPRESERVED \_ Data**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Tipo: **PMPCONFIGURATION \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **\_ \_ notificación de configuración de MPCALLBACK**. Vea [**MPCONFIGURATION \_ Data**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Tipo: **PMPFASTPATH \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ FASTPATH**. Vea [**MPFASTPATH \_ Data**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Tipo: **PMPEXPIRATION \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **\_ \_ expiración del producto MPCALLBACK**. Vea [**MPEXPIRATION \_ Data**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Tipo: **PMPNIS \_ \_ datos privados**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ NIS \_ Private**. Vea [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**pHealthData**
</dt> <dd>

Tipo: **PMPHEALTH \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ Health**. Vea [**MPHEALTH \_ Data**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Tipo: **PMPENDOFLIFE \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ ENDOFLIFE**. Vea [**MPENDOFLIFE \_ Data**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Tipo: **PMPMALWARETOAST \_ Data**

</dd> <dd>

Cuando **Escriba**  ==  **MPCALLBACK \_ MALWARETOAST**. Vea [**MPMALWARETOAST \_ Data**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo MPCALLBACK**](mpcallback-type.md)
</dt> <dt>

[**datos de MPCLEAN \_**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN \_ comprobar \_ datos**](mpclean-precheck-data.md)
</dt> <dt>

[**datos de MPCONFIGURATION \_**](mpconfiguration-data.md)
</dt> <dt>

[**datos de MPENDOFLIFE \_**](mpendoflife-data.md)
</dt> <dt>

[**datos de MPEXPIRATION \_**](mpexpiration-data.md)
</dt> <dt>

[**datos de MPFASTPATH \_**](mpfastpath-data.md)
</dt> <dt>

[**datos de MPHEALTH \_**](mphealth-data.md)
</dt> <dt>

[**datos de MPMALWARETOAST \_**](mpmalwaretoast-data.md)
</dt> <dt>

[**MPNIS \_ \_ datos privados**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**datos de MPRESERVED \_**](mpreserved-data.md)
</dt> <dt>

[**datos de MPSAMPLE \_**](mpsample-data.md)
</dt> <dt>

[**datos de MPSCAN \_**](mpscan-data.md)
</dt> <dt>

[**datos de MPSIGUPDATE \_**](mpsigupdate-data.md)
</dt> <dt>

[**datos de MPSTATUS \_**](mpstatus-data.md)
</dt> <dt>

[**datos de MPTHREAT \_**](mpthreat-data.md)
</dt> </dl>

 

 





