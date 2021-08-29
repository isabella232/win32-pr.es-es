---
title: Programador de tareas errores y constantes de éxito (WinError.h)
description: Si se produce un error, Programador de tareas API pueden devolver uno de los siguientes códigos de error como un valor HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Programador de tareas Programador de tareas , referencia, errores y constantes de éxito
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
ms.openlocfilehash: d9633282fd6a504a48db81ce852fad7a2aca16a4ee26a1d14ce4f052b6447ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080395"
---
# <a name="task-scheduler-error-and-success-constants"></a>Programador de tareas errores y constantes de éxito

Si se produce un error, Programador de tareas API pueden devolver uno de los siguientes códigos de error como **un valor HRESULT.**

Las constantes que comienzan con SCHED S son constantes de éxito y las constantes que comienzan por SCHED E son constantes \_ \_ de \_ \_ error.

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

Ejemplo de ejemplo [de código de C/C++: Recuperar el estado de la tarea](c-c-code-example-retrieving-task-status.md).

> [!Note]  
> Algunas Programador de tareas API pueden devolver códigos de error del sistema y de red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: El nombre de red especificado ya no está disponible.

 

Para obtener más información sobre los eventos y los mensajes de error, vea [Eventos y errores Centro de mensajes](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED \_ S \_ TASK \_ READY**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



La tarea está lista para ejecutarse en su próxima hora programada.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED \_ S \_ TASK \_ RUNNING**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



La tarea está en ejecución.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**TAREA SCHED \_ S \_ \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



La tarea no se ejecutará a las horas programadas porque se ha deshabilitado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**LA TAREA \_ SCHED S \_ NO SE \_ HA \_ \_ EJECUTADO**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



La tarea aún no se ha ejecutado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**TAREA SCHED \_ S \_ NO MÁS \_ \_ \_ EJECUCIONES**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



No hay más ejecuciones programadas para esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**TAREA \_ SCHED \_ NO \_ \_ PROGRAMADA**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea según una programación.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**TAREA SCHED \_ \_ FINALIZADA \_**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



El usuario finalizó la última ejecución de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**TAREA SCHED \_ S \_ SIN \_ \_ DESENCADENADORES \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



La tarea no tiene desencadenadores o los desencadenadores existentes están deshabilitados o no establecidos.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**DESENCADENADOR DE \_ EVENTOS \_ SCHED \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Los desencadenadores de eventos no tienen tiempos de ejecución establecidos.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**NO SE \_ ENCONTRÓ EL DESENCADENADOR SCHED E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



No se encuentra el desencadenador de una tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**TAREA SCHED \_ E \_ NO \_ \_ LISTA**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**TAREA SCHED \_ E \_ NO EN \_ \_ EJECUCIÓN**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



No hay ninguna instancia en ejecución de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED \_ E \_ SERVICE \_ NOT \_ INSTALLED**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



El Programador de tareas no está instalado en este equipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED \_ E NO PUEDE ABRIR \_ \_ TAREA \_**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



No se pudo abrir el objeto de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED \_ E \_ INVALID \_ TASK**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



El objeto es un objeto de tarea no válido o no es un objeto de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**NO SE \_ HA ESTABLECIDO LA INFORMACIÓN DE LA CUENTA \_ \_ \_ SCHED \_ E**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



No se encontró información de cuenta en la base de Programador de tareas de seguridad de la tarea indicada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**NO SE \_ ENCONTRÓ EL NOMBRE DE CUENTA \_ \_ \_ SCHED \_ E**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



No se puede establecer la existencia de la cuenta especificada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**DBASE DE \_ \_ CUENTA SCHED E \_ \_ DAÑADA**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



Se detectaron daños en la base de Programador de tareas de seguridad; se ha restablecido la base de datos.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ NO \_ SECURITY \_ SERVICES**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Programador de tareas servicios de seguridad solo están disponibles en Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED \_ E \_ UNKNOWN \_ OBJECT \_ VERSION**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



La versión del objeto de tarea no es compatible o no es válida.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**OPCIÓN DE \_ CUENTA NO \_ \_ ADMITIDA \_ DE SCHED E**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



La tarea se ha configurado con una combinación no admitida de opciones de configuración de cuenta y tiempo de ejecución.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED \_ E \_ SERVICE \_ NOT \_ RUNNING**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



El Programador de tareas no se está ejecutando.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED \_ E \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



El XML de tarea contiene un nodo inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**ESPACIO DE NOMBRES \_ SCHED E \_**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



El XML de tarea contiene un elemento o atributo de un espacio de nombres inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED \_ E \_ INVALIDVALUE**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



El XML de tarea contiene un valor con formato incorrecto o fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED \_ E \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



Falta un elemento o atributo necesario en el XML de la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED \_ E \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



El XML de la tarea tiene un formato anterior.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**ERROR EN \_ ALGUNOS \_ \_ DESENCADENADORES DE SCHED \_**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



La tarea está registrada, pero no todos los desencadenadores especificados iniciarán la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**PROBLEMA DE INICIO \_ DE \_ SESIÓN POR \_ LOTES DE \_ SCHED**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



La tarea está registrada, pero puede no iniciarse. El privilegio de inicio de sesión por lotes debe estar habilitado para la entidad de seguridad de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED \_ E \_ TOO \_ MANY \_ NODES**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



El XML de tarea contiene demasiados nodos del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**LÍMITE FINAL DE SCHED \_ E \_ PAST \_ \_**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



La tarea no se puede iniciar después del límite final del desencadenador.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E YA EN \_ \_ EJECUCIÓN**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Ya se está ejecutando una instancia de esta tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**USUARIO SCHED \_ E \_ NO INICIADO \_ \_ \_ SESIÓN**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



La tarea no se ejecutará porque el usuario no ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**HASH DE \_ TAREA SCHED E \_ INVALID \_ \_**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



La imagen de tarea está dañada o se ha alterado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**EL SERVICIO \_ SCHED E \_ NO ESTÁ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



El Programador de tareas no está disponible.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED \_ E \_ SERVICE \_ TOO \_ BUSY**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



El Programador de tareas está demasiado ocupado para controlar la solicitud. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**INTENTO DE \_ TAREA \_ SCHED E \_**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



El Programador de tareas intentó ejecutar la tarea, pero la tarea no se ha ejecutado debido a una de las restricciones de la definición de tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**TAREA SCHED \_ S \_ EN \_ COLA**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



El Programador de tareas ha solicitado que se ejecute la tarea.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**TAREA SCHED \_ E \_ \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



La tarea está deshabilitada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED \_ E \_ TASK \_ NOT \_ V1 \_ COMPAT**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



La tarea tiene propiedades que no son compatibles con versiones anteriores de Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED \_ E \_ START \_ ON \_ DEMAND**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



La configuración de la tarea no permite que la tarea se inicie a petición.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



 

 





