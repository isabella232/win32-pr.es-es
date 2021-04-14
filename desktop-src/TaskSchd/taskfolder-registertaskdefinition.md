---
title: TaskFolder. RegisterTaskDefinition, método
description: Para el scripting, registra (crea) una tarea en una ubicación especificada mediante el objeto TaskDefinition para definir una tarea.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Método RegisterTaskDefinition Programador de tareas
- Método RegisterTaskDefinition Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método RegisterTaskDefinition
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
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422442"
---
# <a name="taskfolderregistertaskdefinition-method"></a>TaskFolder. RegisterTaskDefinition, método

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

*ruta de acceso* \[ de\]
</dt> <dd>

Nombre de la tarea. Si este valor es **Nothing**, la tarea se registrará en la carpeta de tareas raíz y el nombre de la tarea será un valor GUID creado por el servicio Programador de tareas.

Un nombre de tarea no puede comenzar ni terminar con un carácter de espacio. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*definición* \[ de de\]
</dt> <dd>

Definición de la tarea que se registra.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Constante [**de \_ creación de tareas**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .



| Value                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**Tarea \_ de VALIDAR \_ solo**</dt> <dt>0x1</dt> </dl>                                                | El Programador de tareas comprueba la sintaxis del XML que describe la tarea, pero no registra la tarea. Esta constante no se puede combinar con la **tarea \_ crear**, **\_ Actualizar tarea** o **\_ crear \_ o \_ Actualizar** valores.<br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**Tarea \_ de CREAR**</dt> <dt>0X2</dt> </dl>                                                                      | El Programador de tareas registra la tarea como una nueva tarea.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**Tarea \_ de ACTUALIZAR**</dt> <dt>0x4</dt> </dl>                                                                      | El Programador de tareas registra la tarea como una versión actualizada de una tarea existente. Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.<br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**Tarea \_ de CREAR \_ o \_ Actualizar**</dt> <dt>0x6</dt> </dl>                                      | El Programador de tareas registra la tarea como una nueva tarea o como una versión actualizada si la tarea ya existe. Equivalente a TASK \_ Create \| Task \_ Update.<br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**Tarea \_ de Deshabilitar**</dt> <dt>0x8</dt> </dl>                                                                   | El Programador de tareas deshabilita la tarea existente.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**Tarea \_ de No \_ agregar \_ entidad \_**</dt> de seguridad principal <dt>0x10</dt> </dl>                  | El Programador de tareas no puede Agregar la entrada de permiso de control de acceso (ACE) para la entidad de seguridad del contexto. Cuando se llama a la función **TaskFolder. RegisterTaskDefinition** con esta marca para actualizar una tarea, el servicio Programador de tareas no agrega la ACE para la nueva entidad de seguridad de contexto y no quita la ACE de la entidad de seguridad de contexto anterior.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**Tarea \_ de OMITIr \_ \_ desencadenadores de registro**</dt> <dt>0x20</dt> </dl> | El Programador de tareas crea la tarea, pero omite los desencadenadores de registro de la tarea. Al omitir los desencadenadores de registro, la tarea no se ejecutará cuando se registre a menos que un desencadenador basado en el tiempo haga que se ejecute en el registro.<br/>                                                                                                         |



 

</dd> <dt>

*userId* \[ de\]
</dt> <dd>

Las credenciales de usuario que se usan para registrar la tarea. Si está presente, estas credenciales tienen prioridad sobre las credenciales especificadas en el objeto de definición de tarea al que apunta el parámetro de *definición* .

> [!Note]  
> Si la tarea se define como una tarea Programador de tareas 1,0, no use un nombre de grupo (en lugar de un nombre de usuario específico) en este parámetro userId. Una tarea se define como una tarea Programador de tareas 1,0 cuando la propiedad de [**compatibilidad**](tasksettings-compatibility.md) está establecida en 1 en la configuración de la tarea.

 

</dd> <dt>

*contraseña* \[ de de\]
</dt> <dd>

La contraseña de userId que se usa para registrar la tarea. Cuando se usa el tipo de inicio de sesión de la cuenta del servicio de inicio de sesión de tareas \_ \_ \_ , la contraseña debe ser un valor **Variant** vacío como **VT \_ null** o **VT \_ Empty**.

</dd> <dt>

*logonType* \[ de\]
</dt> <dd>

Define la técnica de inicio de sesión que se utiliza para ejecutar la tarea registrada.



| Value                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tarea \_ de LOGON \_ ninguno**</dt> <dt>0</dt> </dl>                                                                               | No se ha especificado el método Logon. Se usa para las credenciales que no son NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tarea \_ de \_Contraseña de inicio de sesión**</dt> <dt>1</dt> </dl>                                                                   | Use una contraseña para iniciar sesión en el usuario. La contraseña debe proporcionarse en el momento del registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tarea \_ de Inicio de sesión \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use un token interactivo existente para ejecutar una tarea. El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tarea \_ de \_ \_ Token interactivo de inicio de sesión**</dt> <dt>3</dt> </dl>                                       | El usuario ya debe haber iniciado sesión. La tarea se ejecutará solo en una sesión interactiva existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tarea \_ de \_Grupo de inicio de sesión**</dt> <dt>4</dt> </dl>                                                                            | Activación de grupos. El campo **GROUPID** especifica el grupo.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tarea \_ de \_ \_ Cuenta de servicio de inicio de sesión**</dt> <dt>5</dt> </dl>                                             | Indica que se utiliza un sistema local, servicio local o cuenta de servicio de red como contexto de seguridad para ejecutar la tarea.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tarea \_ de \_Token interactivo \_ de inicio \_ de sesión o \_ contraseña**</dt> <dt>6</dt> </dl> | En primer lugar, use el token interactivo. Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña. La contraseña debe especificarse cuando se registra una tarea. Esta marca no se recomienda para las nuevas tareas porque es menos confiable que la contraseña de inicio de sesión de la tarea \_ \_ .<br/> |



 

</dd> <dt>

*SDDL* \[ en, opcional\]
</dt> <dd>

Descriptor de seguridad asociado a la tarea registrada. Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una tarea.

> [!Note]  
> Si se deniega el acceso a la cuenta de sistema local a una tarea, el servicio de Programador de tareas puede generar resultados inesperados.

 

</dd> <dt>

*tarea* \[ de enuncia\]
</dt> <dd>

Objeto [**RegisteredTask**](registeredtask.md) que representa la nueva tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad [**LogonType**](principal-logontype.md) de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**.

Solo un miembro del grupo administradores puede crear una tarea con un desencadenador de arranque.

Puede registrar correctamente una tarea con un grupo especificado en el parámetro *userId* y 3 (**\_ \_ \_ símbolo interactivo de inicio de sesión de tarea**) especificado en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**, pero la tarea no se ejecutará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

 





