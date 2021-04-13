---
title: MPTHREAT_INFO estructura (MpClient. h)
description: Contiene información sobre una amenaza.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492629"
---
# <a name="mpthreat_info-structure"></a>Estructura de información de MPTHREAT \_

Contiene información sobre una amenaza.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID. de MPTHREAT**

</dd> <dd>

Identificador de amenaza. El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**DetectionID**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

IDENTIFICADOR de detección.

</dd> <dt>

**Nombre**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Nombre de amenaza.

</dd> <dt>

**ThreatType**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ Type**](mpthreat-type.md)**

</dd> <dd>

Tipo de amenaza. Se utiliza para diferenciar entre distintos tipos de amenazas, como los conocidos, los desconocidos o los conocidos. Consulte [**\_ tipo de MPTHREAT**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Tipo: **[ **\_ gravedad de MPTHREAT**](mpthreat-severity.md)**

</dd> <dd>

Importancia de las amenazas. Vea [**\_ gravedad de MPTHREAT**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Tipo: **[ **\_ categoría MPTHREAT**](mpthreat-category.md)**

</dd> <dd>

Categoría de amenazas, como un troyano o un registrador de virus. Vea [**la \_ categoría MPTHREAT**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

IDENTIFICADOR de descripción breve de amenaza.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

IDENTIFICADOR de descripción de aviso de amenazas.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Tipo: **[ **\_ Estado de MPTHREAT**](mpthreat-status.md)**

</dd> <dd>

Estado de amenaza, como detectado, limpiado o en cuarentena. Consulte [**\_ Estado de MPTHREAT**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de acciones sugeridas en **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Tipo: **[**MPTHREAT de \_ acción**](mpthreat-action.md)máxima del módulo de administración de acciones \[ \_ \_\]**

</dd> <dd>

Matriz de acciones sugeridas. Consulte [**la \_ acción MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de recursos en **ResourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \** _

</dd> <dd>

Lista de recursos identificados con la amenaza. Vea [_ *MPRESOURCE \_ info* *](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Hora en que se modificó por última vez el estado de la amenaza.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de estado asociado al estado de amenaza.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Tipo: **[ **\_ detección de MPTHREAT**](mpthreat-detection.md)**

</dd> <dd>

Tipo de detección de amenazas, como concreto, sospechoso o genérico. Consulte [**\_ detección de MPTHREAT**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

GUID de cuarentena.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución de la amenaza, como desconocido, bloqueado o activo. Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Data**
</dt> <dd>

Información adicional. El puntero a la estructura adecuada depende del valor de **ThreatType**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ no usado**

</dd> <dd>

When **ThreatType**  ==  **MPTHREAT \_ Type \_ KNOWNBAD**. Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**

</dd> <dd>

Cuando el comportamiento de tipo de **ThreatType**  ==  **MPTHREAT \_ \_**. Consulte [**MPTHREAT \_ INFOEX \_ Behavior**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ no usado**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ Type \_ Unknown**. Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ no usado**

</dd> <dd>

When **ThreatType** = = MPTHREAT \_ Type \_ KNOWNGOOD. Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ Type \_ NIS**. Consulte [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Tipo: **[ **\_ Estado de MPDETECTION**](mpdetection-state.md)**

</dd> <dd>

Estado actual de la detección. Consulte [**\_ Estado de MPDETECTION**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Usuario asociado a la detección, con el formato "dominio/usuario".

</dd> <dt>

**DetectionSource**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origen de la detección. Vea [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Nombre del proceso asociado a la detección.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ Origin**](mpdetection-origin.md)**

</dd> <dd>

El origen de la detección, como local o de red. Vea [**MPDETECTION \_ Origin**](mpdetection-origin.md).

</dd> <dt>

**reserved1**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Metadatos reservados sobre la detección.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Hora de la detección inicial.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución justo antes de la corrección. Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**RemediationTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

La corrección de tiempo que se ha producido.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución después de la corrección. Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True si el error de corrección era crítico.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Razón por la que el error de corrección no es crítico. No se garantiza que se admita en el futuro.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Usuario que solicitó la corrección, con el formato "dominio/usuario".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de recursos en **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**

</dd> <dd>

Lista de recursos con errores durante la corrección. Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> <dt>

**FailureResolved**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True si se ha resuelto el error de corrección. Esto moverá el cubo a completa o a una acción adicional.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Tipo: **[ **MPRESOLVED \_ Reason**](mpresolved-reason.md)**

</dd> <dd>

Motivo de la resolución de un error de corrección. Este es el motivo por el que la detección se ha pasado de no se pudo realizar una acción adicional o ha finalizado. Consulte [**MPRESOLVED \_ Reason**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Se requieren acciones adicionales.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Acciones adicionales que se han realizado.

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Información adicional sobre la detección de amenazas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**origen de MPDETECTION \_**](mpdetection-origin.md)
</dt> <dt>

[**Estado de MPDETECTION \_**](mpdetection-state.md)
</dt> <dt>

[**Estado de MPEXECUTION \_**](mpexecution-status.md)
</dt> <dt>

[**motivo de MPRESOLVED \_**](mpresolved-reason.md)
</dt> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_acción MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**\_categoría MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**detección de MPTHREAT \_**](mpthreat-detection.md)
</dt> <dt>

[**\_comportamiento de INFOEX de MPTHREAT \_**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ no usado**](mpthreat-infoex-unused.md)
</dt> <dt>

[**gravedad de MPTHREAT \_**](mpthreat-severity.md)
</dt> <dt>

[**Estado de MPTHREAT \_**](mpthreat-status.md)
</dt> <dt>

[**\_tipo MPTHREAT**](mpthreat-type.md)
</dt> </dl>

 

 





