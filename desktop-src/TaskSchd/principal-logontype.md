---
title: Principal.LogonType, propiedad
description: Para el scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Propiedad LogonType Programador de tareas
- Propiedad LogonType Programador de tareas , objeto Principal
- Objeto principal Programador de tareas propiedad , LogonType
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
ms.openlocfilehash: ec67a00b55510aecb980fd8bd8a5b2fa4ad6c73e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885650"
---
# <a name="principallogontype-property"></a>Principal.LogonType, propiedad

Para el scripting, obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valor de propiedad

Establezca en una de las siguientes [**constantes de \_ enumeración TASK LOGON TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**TASK \_ INICIO \_ DE SESIÓN NINGUNO**</dt> <dt>0</dt> </dl>                                                                               | No se especifica el método logon. Se usa para credenciales que no son NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**TASK \_ CONTRASEÑA \_ DE INICIO DE**</dt> SESIÓN <dt>1</dt> </dl>                                                                   | Use una contraseña para iniciar sesión en el usuario. La contraseña debe proporcionarse en el momento del registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**TASK \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use un token interactivo existente para ejecutar una tarea. El usuario debe iniciar sesión con un servicio para el inicio de sesión del usuario (S4U). Cuando se usa un inicio de sesión S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**TASK \_ TOKEN \_ INTERACTIVO DE INICIO \_ DE**</dt> <dt>SESIÓN 3</dt> </dl>                                       | El usuario ya debe haber iniciado sesión. La tarea se ejecutará solo en una sesión interactiva existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**TASK \_ GRUPO DE \_ INICIO DE**</dt> SESIÓN <dt>4</dt> </dl>                                                                            | Activación de grupo. El campo userId especifica el grupo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**TASK \_ CUENTA DE \_ SERVICIO DE INICIO DE \_ SESIÓN**</dt> <dt>5</dt> </dl>                                             | Indica que se usa una cuenta de sistema local, servicio local o servicio de red como contexto de seguridad para ejecutar la tarea.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**TASK \_ TOKEN \_ INTERACTIVO DE INICIO DE SESIÓN O \_ \_ \_ CONTRASEÑA**</dt> <dt>6</dt> </dl> | En primer lugar, use el token interactivo. Si el usuario no ha iniciado sesión (no hay ningún token interactivo disponible), se usa la contraseña. La contraseña debe especificarse cuando se registra una tarea. Esta marca no se recomienda para las nuevas tareas porque es menos confiable que TASK \_ LOGON \_ PASSWORD.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta propiedad solo es válida cuando la propiedad [**UserId**](principal-userid.md) especifica un identificador de usuario.

Al leer o escribir XML para una tarea, el tipo de inicio de sesión se especifica en el elemento [**&lt; LogonType &gt;**](taskschedulerschema-logontype-principaltype-element.md) del Programador de tareas esquema.

Para una tarea, que contiene una acción de cuadro de mensaje, el cuadro de mensaje se mostrará si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 ( TASK **\_ LOGON INTERACTIVE \_ \_ TOKEN**) o 4 (**TASK LOGON \_ \_ GROUP**) en la propiedad **LogonType** de la entidad de seguridad de tarea o en el parámetro *logonType* de [**TaskFolder.RegisterTask**](taskfolder-registertask.md) [**o TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Entidad de seguridad**](principal.md)
</dt> </dl>

 

 





