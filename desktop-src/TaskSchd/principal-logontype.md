---
title: Propiedad principal. LogonType
description: En el caso de scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Programador de tareas de la propiedad LogonType
- Propiedad LogonType Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491092"
---
# <a name="principallogontype-property"></a>Propiedad principal. LogonType

En el caso de scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valor de propiedad

Establezca en una de las siguientes constantes de enumeración de [**\_ tipo de inicio de sesión de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .



| Value                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tarea \_ de LOGON \_ ninguno**</dt> <dt>0</dt> </dl>                                                                               | No se ha especificado el método Logon. Se usa para las credenciales que no son NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tarea \_ de \_Contraseña de inicio de sesión**</dt> <dt>1</dt> </dl>                                                                   | Use una contraseña para iniciar sesión en el usuario. La contraseña debe proporcionarse en el momento del registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tarea \_ de Inicio de sesión \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use un token interactivo existente para ejecutar una tarea. El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tarea \_ de \_ \_ Token interactivo de inicio de sesión**</dt> <dt>3</dt> </dl>                                       | El usuario ya debe haber iniciado sesión. La tarea se ejecutará solo en una sesión interactiva existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tarea \_ de \_Grupo de inicio de sesión**</dt> <dt>4</dt> </dl>                                                                            | Activación de grupos. El campo userId especifica el grupo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tarea \_ de \_ \_ Cuenta de servicio de inicio de sesión**</dt> <dt>5</dt> </dl>                                             | Indica que se utiliza un sistema local, servicio local o cuenta de servicio de red como contexto de seguridad para ejecutar la tarea.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tarea \_ de \_Token interactivo \_ de inicio \_ de sesión o \_ contraseña**</dt> <dt>6</dt> </dl> | En primer lugar, use el token interactivo. Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña. La contraseña debe especificarse cuando se registra una tarea. Esta marca no se recomienda para las nuevas tareas porque es menos confiable que la contraseña de inicio de sesión de la tarea \_ \_ .<br/> |



 

## <a name="remarks"></a>Observaciones

Esta propiedad solo es válida cuando la propiedad [**userid**](principal-userid.md) especifica un identificador de usuario.

Al leer o escribir XML para una tarea, el tipo de inicio de sesión se especifica en el [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento del esquema de programador de tareas.

En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad **LogonType** de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

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

[**Principal**](principal.md)
</dt> </dl>

 

 





