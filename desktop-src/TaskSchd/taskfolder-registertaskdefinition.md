---
title: Método TaskFolder.RegisterTaskDefinition
description: Para el scripting, registra (crea) una tarea en una ubicación especificada mediante el objeto TaskDefinition para definir una tarea.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Método RegisterTaskDefinition Programador de tareas
- Método RegisterTaskDefinition Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas método , RegisterTaskDefinition
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10f9dfa36e576583e7e980902566a79855def0dcfbeab94ac6364f900cc81ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033845"
---
# <a name="taskfolderregistertaskdefinition-method"></a>Método TaskFolder.RegisterTaskDefinition

Para el scripting, registra (crea) una tarea en una ubicación especificada mediante el objeto [**TaskDefinition**](taskdefinition.md) para definir una tarea.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ruta de acceso* \[ En\]
</dt> <dd>

Nombre de la tarea. Si este valor es **Nothing**, la tarea se registrará en la carpeta de tareas raíz y el nombre de la tarea será un valor GUID creado por el servicio Programador de tareas tarea.

Un nombre de tarea no puede comenzar ni terminar con un carácter de espacio. El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..". no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*definición* \[ En\]
</dt> <dd>

Definición de la tarea registrada.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Constante [**TASK \_ CREATION.**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)



| Value                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**TASK \_ VALIDAR \_ SOLO**</dt> <dt>0x1</dt> </dl>                                                | El Programador de tareas comprueba la sintaxis del XML que describe la tarea, pero no la registra. Esta constante no se puede combinar con los valores **TASK \_ CREATE**, **TASK \_ UPDATE** o **TASK CREATE OR \_ \_ \_ UPDATE.**<br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**TASK \_ CREATE**</dt> <dt>0x2</dt> </dl>                                                                      | El Programador de tareas registra la tarea como una tarea nueva.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**TASK \_ Actualizar**</dt> <dt>0x4</dt> </dl>                                                                      | El Programador de tareas registra la tarea como una versión actualizada de una tarea existente. Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.<br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**TASK \_ Creación \_ o \_ actualización de**</dt> <dt>0x6</dt> </dl>                                      | El Programador de tareas registra la tarea como una tarea nueva o como una versión actualizada si la tarea ya existe. Equivalente a TASK \_ CREATE \| TASK \_ UPDATE.<br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**TASK \_ DESHABILITAR**</dt> <dt>0x8</dt> </dl>                                                                   | El Programador de tareas deshabilita la tarea existente.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**TASK \_ NO AGREGAR \_ ace \_ de entidad \_ de**</dt> <dt>seguridad 0x10</dt> </dl>                  | Se Programador de tareas la entrada de control de acceso (ACE) de permitir para la entidad de seguridad de contexto. Cuando se llama a la función **TaskFolder.RegisterTaskDefinition** con esta marca para actualizar una tarea, el servicio Programador de tareas no agrega la ACE para la nueva entidad de seguridad de contexto y no quita la ACE de la entidad de seguridad de contexto anterior.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**TASK \_ OMITIR \_ \_ DESENCADENADORES DE**</dt> <dt>REGISTRO 0x20</dt> </dl> | El Programador de tareas crea la tarea, pero omite los desencadenadores de registro de la tarea. Al omitir los desencadenadores de registro, la tarea no se ejecutará cuando se registre a menos que un desencadenador basado en el tiempo haga que se ejecute en el registro.<br/>                                                                                                         |



 

</dd> <dt>

*userId* \[ En\]
</dt> <dd>

Credenciales de usuario que se usan para registrar la tarea. Si están presentes, estas credenciales tienen prioridad sobre las credenciales especificadas en el objeto de definición de tarea al que apunta el *parámetro definition.*

> [!Note]  
> Si la tarea se define como una tarea Programador de tareas 1.0, no use un nombre de grupo (en lugar de un nombre de usuario específico) en este parámetro userId. Una tarea se define como una tarea Programador de tareas 1.0 cuando la propiedad [**Compatibility**](tasksettings-compatibility.md) se establece en 1 en la configuración de la tarea.

 

</dd> <dt>

*contraseña* \[ En\]
</dt> <dd>

Contraseña del userId que se usa para registrar la tarea. Cuando se usa el tipo de inicio de sesión TASK LOGON SERVICE ACCOUNT, la contraseña debe ser un valor VARIANT vacío, como \_ \_ VT \_ **\_ NULL** o **VT \_ EMPTY.** 

</dd> <dt>

*logonType* \[ En\]
</dt> <dd>

Define qué técnica de inicio de sesión se usa para ejecutar la tarea registrada.



| Value                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**TASK \_ INICIO \_ DE SESIÓN NINGUNO**</dt> <dt>0</dt> </dl>                                                                               | No se especifica el método logon. Se usa para credenciales que no son DE NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**TASK \_ CONTRASEÑA \_ DE INICIO DE**</dt> SESIÓN <dt>1</dt> </dl>                                                                   | Use una contraseña para iniciar sesión en el usuario. La contraseña debe proporcionarse en el momento del registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**TASK \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use un token interactivo existente para ejecutar una tarea. El usuario debe iniciar sesión con un servicio para el inicio de sesión del usuario (S4U). Cuando se usa un inicio de sesión S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**TASK \_ TOKEN \_ INTERACTIVO DE INICIO \_ DE**</dt> <dt>SESIÓN 3</dt> </dl>                                       | El usuario ya debe haber iniciado sesión. La tarea solo se ejecutará en una sesión interactiva existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**TASK \_ GRUPO DE \_ INICIO DE**</dt> SESIÓN <dt>4</dt> </dl>                                                                            | Activación de grupo. El **campo groupId** especifica el grupo.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**TASK \_ CUENTA DE \_ SERVICIO DE INICIO DE \_ SESIÓN**</dt> <dt>5</dt> </dl>                                             | Indica que se usa una cuenta de sistema local, servicio local o servicio de red como contexto de seguridad para ejecutar la tarea.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**TASK \_ TOKEN \_ INTERACTIVO DE INICIO DE SESIÓN O \_ \_ \_ CONTRASEÑA**</dt> <dt>6</dt> </dl> | En primer lugar, use el token interactivo. Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña. La contraseña debe especificarse cuando se registra una tarea. Esta marca no se recomienda para las nuevas tareas porque es menos confiable que TASK \_ LOGON \_ PASSWORD.<br/> |



 

</dd> <dt>

*sddl* \[ en, opcional\]
</dt> <dd>

Descriptor de seguridad asociado a la tarea registrada. Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea para permitir o denegar el acceso de determinados usuarios y grupos a una tarea.

> [!Note]  
> Si se deniega el acceso a una tarea a la cuenta del sistema local, el Programador de tareas servicio puede producir resultados inesperados.

 

</dd> <dt>

*tarea* \[ out\]
</dt> <dd>

Objeto [**RegisteredTask**](registeredtask.md) que representa la nueva tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para una tarea, que contiene una acción de cuadro de mensaje, el cuadro de mensaje se mostrará si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 ( TASK **\_ LOGON INTERACTIVE \_ \_ TOKEN**) o 4 (**TASK LOGON \_ \_ GROUP**) en la propiedad [**LogonType**](principal-logontype.md) de la entidad de seguridad de tarea o en el parámetro *logonType* de [**TaskFolder.RegisterTask**](taskfolder-registertask.md) **o TaskFolder.RegisterTaskDefinition**.

Solo un miembro del grupo Administradores puede crear una tarea con un desencadenador de arranque.

Puede registrar correctamente una tarea con un grupo especificado en el parámetro *userId* y 3 (**TASK LOGON INTERACTIVE \_ \_ \_ TOKEN**) especificado en el parámetro *logonType* de [**TaskFolder.RegisterTask**](taskfolder-registertask.md) o **TaskFolder.RegisterTaskDefinition**, pero la tarea no se ejecutará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

 





