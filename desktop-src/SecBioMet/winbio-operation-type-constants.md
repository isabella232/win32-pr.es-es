---
title: Constantes de WINBIO_OPERATION_TYPE (Winbio \_ Types. h)
description: Especifique el tipo de operación asincrónica que se va a realizar.
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
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151224"
---
# <a name="winbio_operation_type-constants"></a>Constantes de tipo de \_ operación WINBIO \_

Las siguientes constantes pueden ser devueltas por el Plataforma de biometría de Windows en [**un \_ \_ resultado asincrónico de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para especificar el tipo de operación asincrónica que se va a realizar.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**operación de WINBIO \_ \_ ninguna**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



No se ha identificado ninguna operación.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operación WINBIO \_ abierta**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Se abrió una sesión biométrica. Para obtener más información, consulte [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**cierre de la \_ operación WINBIO \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Se cerró una sesión biométrica. Para obtener más información, vea [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**comprobación de la \_ operación WINBIO \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Se ha comprobado un ejemplo biométrico con respecto a una identidad de usuario. Para obtener más información, vea [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**identificación de la \_ operación WINBIO \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Se capturó un ejemplo biométrico y se comparaba con una plantilla existente. Para obtener más información, vea [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_operación WINBIO \_ Buscar \_ sensor**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Se recuperó el número de identificación de una unidad biométrica. Para obtener más información, vea [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**Inicio de la operación de WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Se inició una secuencia de inscripción biométrica. Para obtener más información, vea [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**captura de la operación de WINBIO de \_ \_ inscripción \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Se ha capturado una muestra biométrica y se ha agregado a la plantilla. Para obtener más información, vea [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**operación de inscripción de WINBIO de \_ \_ \_ confirmación**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Se finalizó una plantilla biométrica pendiente. Para obtener más información, vea [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**descartar la operación de WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Se descartó una plantilla biométrica pendiente. Para obtener más información, vea [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ inscripciones de enumeración de operación WINBIO \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Se enumeraron los subfactores de una plantilla determinada. Para obtener más información, vea [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ operación \_ eliminar \_ plantilla**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Se eliminó una plantilla biométrica del almacén. Para obtener más información, vea [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_ejemplo de \_ captura de operación de WINBIO \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Se capturó un ejemplo biométrico. Para obtener más información, vea [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_propiedad de operación \_ Get \_ de WINBIO**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Se recuperó una sesión biométrica, una unidad o una propiedad de plantilla. Para obtener más información, vea [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_propiedad de \_ conjunto de operación WINBIO \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Se estableció una sesión biométrica, una unidad, una plantilla o una propiedad de la cuenta. Para obtener más información, vea [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento get de operación WINBIO \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



No se utiliza.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unidad de \_ bloqueo de operación de WINBIO \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Una unidad biométrica se bloqueó para uso exclusivo de una sesión. Para obtener más información, vea [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unidad de \_ desbloqueo de operación WINBIO \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Se liberó el bloqueo de sesión en una unidad biométrica. Para obtener más información, vea [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unidad de \_ control de operación WINBIO \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Las operaciones definidas por el proveedor se realizaron en una unidad de control. Para obtener más información, vea [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_privilegio de \_ unidad de control de operación WINBIO \_ \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Las operaciones definidas por el proveedor con privilegios se realizaron en una unidad de control. Para obtener más información, vea [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**\_ \_ marco abierto de la operación WINBIO \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Se abrió un identificador del marco biométrico.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**marco de cierre de la \_ operación WINBIO \_ \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Se cerró un identificador del marco biométrico. Para obtener más información, vea [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_proveedores de \_ servicios de enumeración de operaciones WINBIO \_ \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Se enumeraron los proveedores de servicios biométricos instalados. Para obtener más información, vea [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO de \_ operación de \_ enumeración de \_ unidades biométricas \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Se enumeraron las unidades biométricas conectadas. Para obtener más información, vea [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_bases de \_ datos de enumeración de la operación WINBIO \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Se enumeraron las bases de datos registradas. Para obtener más información, vea [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**llegada de la \_ unidad de operación WINBIO \_ \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Se creó una unidad biométrica. Para obtener más información, vea [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**eliminación de la \_ unidad de operación WINBIO \_ \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Se eliminó una unidad biométrica. Para obtener más información, vea [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_identificación de la operación WINBIO \_ y el \_ \_ vale de versión \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Reservado. Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ comprobación de operación \_ de WINBIO y \_ vale de versión \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Reservado. Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presencia del \_ monitor de operación WINBIO \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Se activó el mecanismo de reconocimiento facial o de supervisión de iris. Para obtener más información, vea [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_operación de \_ inscripción de WINBIO \_**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Un individuo de un grupo de individuos que están representados por los datos del búfer de ejemplo se ha especificado como el individuo que se va a inscribir. Para obtener más información, vea [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Este valor se admite a partir de Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





