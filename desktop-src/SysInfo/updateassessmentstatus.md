---
description: Describe la actualización del sistema operativo en un dispositivo.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Enumeración UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666634"
---
# <a name="updateassessmentstatus-enumeration"></a>Enumeración UpdateAssessmentStatus

Describe la actualización del sistema operativo en un dispositivo. **UpdateAssessmentStatus** se usa en las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) y [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , en los miembros **assessmentForCurrent**, **assessmentForUpToDate** y **securityStatus** . Se devuelve exactamente una constante.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Más reciente**
</dt> <dd>

Este resultado en **assessmentForCurrent** implica que el dispositivo está en la actualización de características y la actualización de calidad más recientes disponibles para ese dispositivo. Dentro de **assessmentForUpToDate**, este resultado implica que el dispositivo está en la última actualización de calidad para la versión de Windows que se está ejecutando.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**
</dt> <dd>

No se ha instalado la actualización de características más reciente debido a una restricción temporal. Cuando se ha colocado una restricción de software en una actualización, la actualización no se instalará automáticamente. un usuario debe iniciar automáticamente la descarga dentro de la experiencia de actualización. Este estado solo se aplica a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**
</dt> <dd>

No se ha instalado la actualización de características más reciente debido a una restricción estricta. Cuando se ha colocado una restricción rígida en una actualización, la actualización no es aplicable al dispositivo. Este estado solo se aplica a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**
</dt> <dd>

El dispositivo no está en la actualización más reciente porque Microsoft ya no admite la actualización de características del dispositivo. Cuando Microsoft deja de admitir una versión de característica, este estado se devolverá para **assessmentForCurrent** y **assessmentForUpToDate**.

> [!Note]  
> Cuando se devuelve **UpdateAssessmentStatus \_ NotLatestEndOfSupport** , el **UpdateImpactLevel** de la evaluación siempre es **UpdateImpactLevel \_ alto**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**
</dt> <dd>

El dispositivo no está en la actualización de características más reciente porque el tren de mantenimiento del dispositivo limita el dispositivo a la actualización más reciente de las características. Por ejemplo: Si un dispositivo está en Rama actual para empresas (CBB) y se ha publicado una nueva actualización de características para Rama actual (CB), se devolverá. Este estado solo se aplica a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**
</dt> <dd>

No se ha instalado la actualización de características más reciente debido a que la Directiva de aplazamiento de actualizaciones de características empresariales Windows Update del dispositivo. La determinación de **daysOutOfDate** tiene en cuenta las directivas de aplazamiento; **daysOutOfDate** no comenzará a incrementar hasta que expire el período de aplazamiento. Este estado solo se aplica a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**
</dt> <dd>

El dispositivo no está en la última actualización de la calidad debido a la Windows Update del dispositivo para la Directiva de aplazamiento de actualizaciones de calidad empresarial. La determinación de **daysOutOfDate** tiene en cuenta las directivas de aplazamiento; **daysOutOfDate** no comenzará a incrementar hasta que expire el período de aplazamiento.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**
</dt> <dd>

El dispositivo no está en la actualización de características más reciente debido a que el dispositivo tiene actualizaciones de características en pausa. El hecho de que un dispositivo esté en pausa no se factoriza en el cálculo de **daysOutOfDate**. Este estado solo se aplica a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**
</dt> <dd>

El dispositivo no está en la última actualización de la calidad debido a que el dispositivo tiene actualizaciones de calidad en pausa. El hecho de que un dispositivo esté en pausa no se factoriza en el cálculo de **daysOutOfDate**. **daysOutOfDate** no Factoriza si un dispositivo está en pausa en su cálculo.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**
</dt> <dd>

El dispositivo no está en la actualización más reciente porque la aprobación de actualizaciones no se realiza a través de Windows Update.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**
</dt> <dd>

El dispositivo no está en la actualización más reciente debido a un motivo que no se puede determinar en la evaluación.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**
</dt> <dd>

El dispositivo no está en la última actualización de características debido a la Directiva de la versión de destino de la Windows Update del dispositivo. Esta Directiva mantiene el dispositivo en la versión de lanzamiento de la característica de destino.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa con mayor frecuencia con las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) y [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , que a su vez se usan con el método [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) para [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




