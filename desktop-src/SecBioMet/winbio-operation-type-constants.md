---
title: WINBIO_OPERATION_TYPE constantes (Winbio \_ types.h)
description: Especifique el tipo de operación asincrónica que se está realizando.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39dd6e2656ad73623df9d6a92d514e90371bc3761563e5f24c41211680c2455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909954"
---
# <a name="winbio_operation_type-constants"></a>Constantes DE \_ TIPO DE \_ OPERACIÓN WINBIO

El marco biométrico de Windows puede devolver las siguientes constantes en un RESULTADO [**\_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) de WINBIO para especificar el tipo de operación asincrónica que se está realizando.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**OPERACIÓN WINBIO \_ \_ NONE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



No se ha identificado ninguna operación.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**OPERACIÓN WINBIO \_ \_ ABIERTA**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Se ha abierto una sesión biométrica. Para obtener más información, [**vea WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**OPERACIÓN \_ WINBIO \_ CLOSE**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Se cerró una sesión biométrica. Para obtener más información, [**vea WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**COMPROBACIÓN DE \_ LA OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Se comprobó una muestra biométrica con una identidad de usuario. Para obtener más información, [**consulta WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**IDENTIFICACIÓN DE \_ LA OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Se capturó un ejemplo biométrico y se comparó con una plantilla existente. Para obtener más información, [**consulta WinBioIdentify.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**SENSOR DE \_ LOCALIZACIÓN DE \_ OPERACIÓN WINBIO \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Se recuperó el número de identificador de una unidad biométrica. Para obtener más información, [**consulta WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO \_ OPERATION \_ ENROLL \_ BEGIN**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Se inició una secuencia de inscripción biométrica. Para obtener más información, [**consulta WinBioEnrollBegin.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO \_ OPERATION \_ ENROLL \_ CAPTURE**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Se capturó una muestra biométrica y se agregó a la plantilla. Para obtener más información, [**consulta WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**CONFIRMACIÓN DE \_ INSCRIPCIÓN \_ DE OPERACIÓN WINBIO \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Se finalizó una plantilla biométrica pendiente. Para obtener más información, [**consulta WinBioEnrollCommit.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**DESCARTE DE \_ INSCRIPCIÓN DE \_ OPERACIÓN WINBIO \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Se ha descartado una plantilla biométrica pendiente. Para obtener más información, [**consulta WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**INSCRIPCIONES DE \_ \_ ENUMERACIÓN DE OPERACIONES WINBIO \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Se enumeraron los subfactores de una plantilla determinada. Para obtener más información, [**consulta WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**PLANTILLA DE \_ ELIMINACIÓN DE \_ OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Se eliminó una plantilla biométrica del almacén. Para obtener más información, [**vea WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**EJEMPLO DE CAPTURA \_ DE OPERACIÓN \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Se capturó una muestra biométrica. Para obtener más información, [**vea WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO \_ OPERATION \_ GET \_ PROPERTY**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Se recuperó una sesión biométrica, una unidad o una propiedad de plantilla. Para obtener más información, [**vea WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**PROPIEDAD SET \_ DE OPERACIÓN \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Se estableció una sesión biométrica, una unidad, una plantilla o una propiedad de cuenta. Para obtener más información, [**vea WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**EVENTO GET \_ DE OPERACIÓN \_ WINBIO \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



No se usa.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**UNIDAD DE BLOQUEO \_ DE \_ OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Una sesión bloqueó una unidad biométrica para su uso exclusivo. Para obtener más información, [**consulta WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**UNIDAD DE DESBLOQUEO \_ DE OPERACIÓN \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Se ha liberado el bloqueo de sesión en una unidad biométrica. Para obtener más información, [**consulta WinBioUnlockUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**UNIDAD DE \_ CONTROL DE \_ OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Las operaciones definidas por el proveedor se realizaron en una unidad de control. Para obtener más información, [**consulta WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**UNIDAD DE \_ CONTROL DE OPERACIONES WINBIO CON \_ \_ \_ PRIVILEGIOS**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Las operaciones definidas por el proveedor con privilegios se realizaron en una unidad de control. Para obtener más información, [**vea WinBioControlUnitPrivileged.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ OPERATION \_ OPEN \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Se ha abierto un identificador para el marco biométrico.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**MARCO DE \_ CIERRE DE OPERACIÓN \_ WINBIO \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Se cerró un identificador para el marco biométrico. Para obtener más información, [**vea WinBioCloseFramework.**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**PROVEEDORES DE \_ SERVICIOS DE ENUMERACIÓN DE OPERACIÓN \_ \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Se enumeraron los proveedores de servicios biométricos instalados. Para obtener más información, [**vea WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**UNIDADES \_ BIOMÉTRICAS DE WINBIO OPERATION \_ ENUM \_ \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Se enumeraron las unidades biométricas adjuntas. Para obtener más información, [**vea WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**BASES DE DATOS \_ DE ENUMERACIÓN DE OPERACIÓN \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Se enumeraron las bases de datos registradas. Para obtener más información, [**vea WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**LLEGADA DE LA \_ UNIDAD DE OPERACIÓN DE \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Se creó una unidad biométrica. Para obtener más información, [**vea WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**ELIMINACIÓN DE UNIDAD \_ DE \_ OPERACIÓN DE \_ WINBIO**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Se eliminó una unidad biométrica. Para obtener más información, [**vea WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**IDENTIFICACIÓN Y VALE DE LANZAMIENTO DE LA \_ \_ OPERACIÓN \_ \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Reservado. Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**COMPROBACIÓN Y LANZAMIENTO \_ DE LA OPERACIÓN \_ WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Reservado. Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**PRESENCIA DEL \_ MONITOR DE \_ OPERACIÓN \_ WINBIO**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Se ha activado el mecanismo de reconocimiento facial o supervisión de iris. Para obtener más información, [**vea WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ OPERATION \_ ENROLL \_ SELECT**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Se especificó un individuo de un grupo de individuos representados por datos en el búfer de ejemplo como el individuo que se inscribió. Para obtener más información, [**vea WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluye Winbio.h para aplicaciones cliente o Adaptadores de \_ Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





