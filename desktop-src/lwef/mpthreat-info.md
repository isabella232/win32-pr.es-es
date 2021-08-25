---
title: MPTHREAT_INFO estructura (MpClient.h)
description: Contiene información sobre una amenaza.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO estructura heredada de Windows environment
- PMPTHREAT_INFO puntero de estructura Legacy Windows Environment Features
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
ms.openlocfilehash: b7be9b1f38a2771d7c6e4831e7716552de34492b30429084f3e087e0a3b49602
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943925"
---
# <a name="mpthreat_info-structure"></a>Estructura DE INFORMACIÓN \_ DE MPTHREAT

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

Tipo: **Id. \_ de MPTHREAT**

</dd> <dd>

Identificador de amenaza. El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**DetectionID**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Id. de detección.

</dd> <dt>

**Nombre**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nombre de la amenaza.

</dd> <dt>

**ThreatType**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ TYPE**](mpthreat-type.md)**

</dd> <dd>

Tipo de amenaza. Se usa para diferenciar entre distintos tipos de amenazas, como conocido como malo, desconocido o bueno conocido. Vea [**MPTHREAT \_ TYPE**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Tipo: **[ **GRAVEDAD DE \_ MPTHREAT**](mpthreat-severity.md)**

</dd> <dd>

Importancia de las amenazas. Consulte [**GRAVEDAD DE MPTHREAT. \_**](mpthreat-severity.md)

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ CATEGORY**](mpthreat-category.md)**

</dd> <dd>

Categoría de amenazas, como un troyano o un campo. Vea [**MPTHREAT \_ CATEGORY**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de descripción breve de amenazas.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de descripción del aviso de amenazas.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATUS**](mpthreat-status.md)**

</dd> <dd>

Estado de amenaza, como detectado, limpio o en cuarentena. Vea [**MPTHREAT STATUS ( \_ ESTADO DE MPTHREAT).**](mpthreat-status.md)

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de acciones sugeridas en **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Tipo: **[**SUGERENCIAS MÁXIMAS DE MPTHREAT \_ ACTION**](mpthreat-action.md) \[ \_ MP \_\]**

</dd> <dd>

Matriz de acciones sugeridas. Vea [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de recursos en **ResourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO \***

</dd> <dd>

Lista de recursos identificados con la amenaza. Consulte [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Hora a la que cambió por última vez el estado de la amenaza.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de estado asociado al estado de amenaza.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ DETECTION**](mpthreat-detection.md)**

</dd> <dd>

Tipo de detección de amenazas, como concreto, sospechoso o genérico. Consulte [**MPTHREAT \_ DETECTION**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Guid de cuarentena.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución de la amenaza, como no conocido, bloqueado o activo. Consulte [**MPEXECUTION \_ STATUS (ESTADO DE MPEXECUTION).**](mpexecution-status.md)

</dd> <dt>

**Datos**
</dt> <dd>

Información adicional. El puntero a la estructura adecuada depende del valor **de ThreatType**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ KNOWNBAD**. Vea [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ BEHAVIOR**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ BEHAVIOR**. Vea [**MPTHREAT \_ INFOEX BEHAVIOR (COMPORTAMIENTO DE INFOEX de MPTHREAT). \_**](mpthreat-infoex-behavior.md)

</dd> <dt>

**pUnknown**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ UNKNOWN**. Vea [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Cuando **ThreatType** == MPTHREAT \_ TYPE \_ KNOWNOPEN. Vea [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pIque**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Cuando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ NIS**. Consulte [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ STATE**](mpdetection-state.md)**

</dd> <dd>

Estado actual de la detección. Vea [**MPDETECTION \_ STATE**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

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

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nombre del proceso asociado a la detección.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ ORIGIN**](mpdetection-origin.md)**

</dd> <dd>

Origen de la detección, como local o red. Vea [**MPDETECTION \_ ORIGIN**](mpdetection-origin.md).

</dd> <dt>

**reserved1**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Metadatos reservados sobre la detección.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Hora de la detección inicial.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución justo antes de la corrección. Vea [**MPEXECUTION STATUS (ESTADO \_ DE MPEXECUTION).**](mpexecution-status.md)

</dd> <dt>

**CorrecciónTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Se produjo la corrección de la hora.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Estado de ejecución después de la corrección. Vea [**MPEXECUTION STATUS (ESTADO \_ DE MPEXECUTION).**](mpexecution-status.md)

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True si el error de corrección era crítico.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El motivo por el que el error de corrección no es crítico. No se garantiza que esto sea compatible en el futuro.

</dd> <dt>

**CorrecciónUsuario**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Usuario que solicitó la corrección, con el formato "dominio/usuario".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Recuento de recursos en **RemediationResourceList**.

</dd> <dt>

**CorrecciónResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO \[ RemediationResourceCount \]**

</dd> <dd>

Lista de recursos con errores durante la corrección. Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**Error Resuelto**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True si se ha resuelto el error de corrección. Esto moverá el cubo a una acción completa o adicional.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Tipo: **[ **MPRESOLVED \_ REASON**](mpresolved-reason.md)**

</dd> <dd>

Motivo por el que se resuelve el error de corrección. Esta es la razón por la que la detección pasó de no se pudo a una acción adicional o se finalizó. Vea [**MPRESOLVED \_ REASON**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Son acciones adicionales necesarias.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Cualquier acción adicional que se haya realizado.

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
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**MPDETECTION \_ ORIGIN**](mpdetection-origin.md)
</dt> <dt>

[**ESTADO DE \_ MPDETECTION**](mpdetection-state.md)
</dt> <dt>

[**ESTADO DE \_ MPEXECUTION**](mpexecution-status.md)
</dt> <dt>

[**MOTIVO DE \_ MPRESOLVED**](mpresolved-reason.md)
</dt> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**ACCIÓN \_ MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**CATEGORÍA \_ MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**DETECCIÓN DE \_ MPTHREAT**](mpthreat-detection.md)
</dt> <dt>

[**COMPORTAMIENTO DE \_ INFOEX DE MPTHREAT \_**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ SIN USAR**](mpthreat-infoex-unused.md)
</dt> <dt>

[**GRAVEDAD DE \_ MPTHREAT**](mpthreat-severity.md)
</dt> <dt>

[**ESTADO DE \_ MPTHREAT**](mpthreat-status.md)
</dt> <dt>

[**TIPO \_ MPTHREAT**](mpthreat-type.md)
</dt> </dl>

 

 





