---
title: Programador de tareas constantes de error y de éxito (WinError. h)
description: Si se produce un error, las API de Programador de tareas pueden devolver uno de los siguientes códigos de error como un valor HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Programador de tareas las constantes Programador de tareas, Reference, error y Success
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679059"
---
# <a name="task-scheduler-error-and-success-constants"></a>Programador de tareas las constantes de error y Success

Si se produce un error, las API de Programador de tareas pueden devolver uno de los siguientes códigos de error como un valor **HRESULT** .

Las constantes que comienzan por SCHEd \_ S \_ son constantes correctas y las constantes que comienzan por sched \_ e \_ son constantes de error.

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

Ejemplo de [código de C/C++: recuperar el estado](c-c-code-example-retrieving-task-status.md)de la tarea.

> [!Note]  
> Algunas API de Programador de tareas pueden devolver códigos de error del sistema y de la red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.

 

Para obtener más información sobre eventos y mensajes de error, consulte [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**tarea SCHEd \_ S \_ \_ lista**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



La tarea está lista para ejecutarse en la siguiente hora programada.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**tarea SCHEd \_ S en \_ \_ ejecución**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



La tarea está en ejecución.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**tarea SCHEd \_ S \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



La tarea no se ejecutará a las horas programadas porque se ha deshabilitado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**la \_ tarea sched \_ \_ no se ha \_ \_ ejecutado**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



La tarea aún no se ha ejecutado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**la \_ tarea sched S \_ \_ no hay \_ más \_ ejecuciones**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



No hay más ejecuciones programadas para esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**tarea SCHEd \_ S \_ \_ no \_ programada**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea en una programación.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_tarea esq \_ S \_ finalizada**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



El usuario finalizó la última ejecución de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**\_ \_ \_ no hay \_ \_ desencadenadores VÁLIDOs en la tarea sched S**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



La tarea no tiene desencadenadores o los desencadenadores existentes están deshabilitados o no se han establecido.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_ \_ desencadenador de evento sched S \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Los desencadenadores de eventos no tienen tiempos de ejecución establecidos.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ no \_ se encontró el desencadenador sched E**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



No se encuentra el desencadenador de una tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**tarea SCHEd \_ E \_ \_ no \_ preparada**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**tarea SCHEd \_ E \_ no se \_ \_ está ejecutando**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



No hay ninguna instancia en ejecución de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**el \_ servicio sched E \_ \_ no \_ está instalado**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



El servicio de Programador de tareas no está instalado en este equipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHEd \_ E \_ no puede \_ abrir la \_ tarea**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



No se pudo abrir el objeto de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHEd \_ E \_ tarea no válida \_**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



El objeto es un objeto de tarea no válido o no es un objeto de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_información de cuenta de E/s \_ \_ \_ no \_ establecida**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



No se encontró ninguna información de cuenta en la base de datos de Programador de tareas Security para la tarea indicada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ no se encontró el nombre \_ de cuenta de sched**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



No se puede establecer la existencia de la cuenta especificada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHEd \_ E \_ cuenta \_ dBase \_ dañada**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



Se detectaron daños en la base de datos de seguridad de Programador de tareas; la base de datos se ha restablecido.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHEd \_ E \_ sin \_ servicios de seguridad \_**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Programador de tareas servicios de seguridad solo están disponibles en Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**\_versión de \_ \_ objeto desconocido \_ de sched E**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



La versión del objeto de tarea no es compatible o no es válida.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opción de \_ cuenta no admitida de \_ sched E \_**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



La tarea se ha configurado con una combinación no admitida de opciones de tiempo de ejecución y configuración de cuenta.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**el \_ servicio sched E \_ no se \_ \_ está ejecutando**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



El servicio Programador de tareas no se está ejecutando.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHEd \_ E \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



El XML de la tarea contiene un nodo inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**espacio de nombres SCHEd \_ E \_**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



El XML de la tarea contiene un elemento o un atributo de un espacio de nombres inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHEd \_ E \_ INVALIDVALUE**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



El XML de la tarea contiene un valor que tiene un formato incorrecto o está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHEd \_ E \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



Falta un elemento o atributo obligatorio en el XML de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHEd \_ E \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



El XML de la tarea tiene un formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHEd \_ S \_ algunos \_ desencadenadores con \_ errores**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



La tarea está registrada, pero no todos los desencadenadores especificados iniciarán la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema de \_ Inicio de \_ sesión por lotes \_ de sched S**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



La tarea está registrada, pero puede que no se inicie. El privilegio de inicio de sesión por lotes debe estar habilitado para la entidad de seguridad de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHEd \_ E \_ demasiados \_ \_ nodos**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



El XML de la tarea contiene demasiados nodos del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_ \_ \_ límite final de sched E \_**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



No se puede iniciar la tarea después del límite final del desencadenador.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHEd \_ E \_ ya se \_ está ejecutando**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Ya se está ejecutando una instancia de esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHEd \_ E \_ usuario \_ sin \_ iniciar sesión \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



La tarea no se ejecutará porque el usuario no ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHEd \_ E \_ \_ \_ valor hash de tarea no válido**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



La imagen de tarea está dañada o se ha alterado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**el \_ servicio sched E \_ \_ no \_ está disponible**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



El servicio Programador de tareas no está disponible.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**el \_ servicio sched E está \_ \_ demasiado \_ ocupado**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



El servicio de Programador de tareas está demasiado ocupado para atender la solicitud. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**tarea SCHEd \_ E \_ \_ intentada**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



El servicio Programador de tareas intentó ejecutar la tarea, pero la tarea no se ejecutó debido a una de las restricciones de la definición de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**tarea SCHEd \_ S \_ \_ en cola**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



El servicio Programador de tareas solicitó la ejecución de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**tarea SCHEd \_ E \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



La tarea está deshabilitada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Tarea SCHEd \_ E \_ \_ no \_ \_ compatible v1**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



La tarea tiene propiedades que no son compatibles con versiones anteriores de Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHEd \_ E \_ Inicio \_ a \_ petición**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



La configuración de la tarea no permite que la tarea se inicie a petición.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





