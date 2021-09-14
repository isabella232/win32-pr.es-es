---
title: Contextos de seguridad para tareas
description: Las tareas se registran y ejecutan en un contexto de seguridad específico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886540"
---
# <a name="security-contexts-for-tasks"></a>Contextos de seguridad para tareas

Las tareas se registran y ejecutan en un contexto de seguridad específico. Los usuarios pueden crear aplicaciones que registren, actualicen, eliminen o ejecuten tareas correctamente, pero el usuario debe proporcionar las credenciales correctas cuando se registra una tarea y la aplicación debe ejecutarse en un proceso con los privilegios correctos.

## <a name="specifying-credentials"></a>Especificar credenciales

Puede especificar el contexto de seguridad de una tarea especificando las credenciales en los métodos [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para scripting) o asignando una entidad de seguridad a la propiedad Principal de [**ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) [**(TaskDefinition.Principal**](taskdefinition-principal.md) para scripting). Si se crea una entidad de seguridad para una definición de tarea y, a continuación, la definición de tarea se registra mediante el método **RegisterTaskDefinition** con credenciales diferentes especificadas en los parámetros del método , las credenciales especificadas en el método **RegisterTaskDefinition** sobrescribirán las credenciales de la entidad de seguridad. Si se crea una entidad de seguridad para una definición de tarea mediante XML y, a continuación, el XML de la tarea se registra mediante el método **RegisterTask** con credenciales diferentes especificadas en los parámetros del método , las credenciales especificadas en el método **RegisterTask** sobrescribirán las credenciales de la entidad de seguridad.

Se especifica una cuenta de usuario o un grupo al registrar una tarea o al especificar el principio de una tarea. El contexto de seguridad de la cuenta de usuario o grupo se usa para el contexto de seguridad de la tarea. En estos métodos y propiedades, también se define el tipo de inicio de sesión. El tipo de inicio de sesión se define mediante una de las constantes de la [**enumeración TASK \_ LOGON \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)

Las tareas registradas con la marca TASK LOGON PASSWORD o \_ \_ TASK LOGON \_ S4U solo se iniciarán si el usuario especificado tiene habilitado el privilegio Iniciar sesión \_ como lote. Los usuarios del grupo Administradores y Operadores de copia de seguridad tienen este privilegio habilitado de forma predeterminada.

Al llamar al método [**ITaskService::Conectar**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService.Conectar**](taskservice-connect.md) for scripting), las llamadas de método subsiguientes al servicio Programador de tareas usarán las credenciales que se pasaron al método **Conectar.** Esto es importante tener en cuenta al registrar tareas con un tipo de inicio de sesión interactivo. Cuando registra una tarea con el tipo de inicio de sesión igual a TASK LOGON INTERACTIVE TOKEN y la tarea no tiene credenciales especificadas en la propiedad Principal de la definición de tarea, especificadas en los parámetros \_ \_ para \_ [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)o [](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) [](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)especificadas en el XML que se pasa a RegisterTask , la tarea se registrará con las credenciales del usuario que llamó al método **Conectar.**

## <a name="user-account-control-uac-security-for-tasks"></a>Seguridad de Control de cuentas de usuario (UAC) para tareas

[El control de cuentas](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) de usuario (UAC) permite a los usuarios ejecutar funciones generales, como ejecutar programas y guardar y modificar datos sin exponer privilegios administrativos. De forma predeterminada, una tarea se ejecuta con privilegios de bajo nivel cuando UAC está activado. Las tareas pueden especificar que se ejecutarán con privilegios elevados o privilegios bajos estableciendo un nivel de privilegios de la enumeración [**TASK \_ RUNLEVEL \_ TYPE**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) para la propiedad RunLevel de [**IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) [**(Principal.RunLevel**](principal-runlevel.md) para scripting). El valor de la **propiedad RunLevel** determina el nivel de privilegios en el que se ejecutarán las acciones de una tarea. Si las acciones de una tarea deben tener privilegios elevados para ejecutarse, debe establecer la propiedad **RunLevel** en **TASK \_ RUNLEVEL \_ HIGHEST.** Si una tarea se registra mediante el grupo Administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad **RunLevel** en **TASK \_ RUNLEVEL \_ HIGHEST** si desea ejecutar la tarea. Si una tarea se registra mediante la cuenta de administrador integrada o las cuentas de sistema local o servicio local, se omitirá la propiedad \\ **RunLevel.** El valor de propiedad también se omitirá si el Control de cuentas de usuario (UAC) está desactivado. El valor de la **propiedad RunLevel** no afecta a los permisos necesarios para ejecutar o eliminar una tarea.

> [!Note]  
> Después de actualizar un sistema operativo de Windows XP a Windows Vista, las tareas registradas con la cuenta de administrador integrada en Windows XP tendrán la propiedad RunLevel establecida en \\ **TASK \_ RUNLEVEL \_ LUA**. [](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) Esto puede hacer que algunas tareas no se puedan realizar. Puede actualizar esta propiedad manualmente para asegurarse de que se ejecutarán todas las tareas.

 

Desde un proceso con pocos privilegios, no puede registrar una tarea con la propiedad [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **TASK \_ RUNLEVEL \_ HIGHEST,** pero puede registrar una tarea con la propiedad **RunLevel** igual a **TASK \_ RUNLEVEL \_ LUA**. Las acciones de tarea se ejecutarán con pocos privilegios. No se le permite registrar la tarea como Integrada/Administrador, Sistema local o para un grupo.

Desde un proceso con privilegios elevados, puede registrar una tarea con la propiedad [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **TASK \_ RUNLEVEL \_ HIGHEST** o **TASK \_ RUNLEVEL \_ LUA**. La tarea se ejecutará con un nivel de privilegios decidido por la propiedad **RunLevel** a menos que use la cuenta de administrador, en cuyo caso la tarea se ejecuta con privilegios elevados.

Desde un proceso con privilegios elevados, puede registrar una Programador de tareas 1.0. El Programador de tareas de ejecución establecerá el nivel de ejecución de la tarea en TASK RUNLEVEL HIGHEST y la tarea se ejecutará \_ \_ con privilegios elevados.

Desde un proceso con pocos privilegios, también puede registrar una Programador de tareas 1.0. El Programador de tareas de ejecución establecerá el nivel de ejecución de la tarea en TASK RUNLEVEL LUA y la tarea se ejecutará \_ \_ con pocos privilegios. Si esta tarea se actualiza desde un proceso con privilegios elevados, el nivel de ejecución de la tarea seguirá siendo TASK \_ RUNLEVEL \_ LUA.

## <a name="security-for-registering-tasks"></a>Seguridad para registrar tareas

Cuando registra una tarea desde una cuenta que es miembro del grupo Administradores, solo tiene que especificar una contraseña al registrar la tarea en las situaciones siguientes:

-   Si registra la tarea para que se ejecute en el contexto de seguridad de su cuenta o de otra cuenta de usuario y usa la marca TASK LOGON PASSWORD en el método \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
-   Si registra la tarea para que se ejecute en el contexto de seguridad de una cuenta de usuario diferente y usa la marca TASK LOGON S4U en el método \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

No se puede usar un grupo de usuarios como contexto de seguridad de una tarea al registrar la tarea mediante la marca TASK LOGON S4U o la marca TASK LOGON PASSWORD en el método RegisterTask o \_ \_ \_ \_ [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) [](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

Al registrar una tarea desde una cuenta de usuario que no es miembro del grupo Administradores, no es necesario especificar una contraseña al registrar la tarea si registra la tarea para que se ejecute en el contexto de seguridad de su cuenta y usa el tipo de inicio de sesión S4U o interactivo. De lo contrario, debe especificar una contraseña al registrar la tarea. Además, no se puede registrar la tarea mediante la cuenta de servicio local o mediante un grupo para el contexto de seguridad de la tarea.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Seguridad para leer, actualizar, eliminar y ejecutar tareas

De forma predeterminada, un usuario que crea una tarea puede leer, actualizar, eliminar y ejecutar la tarea. Un usuario debe tener permiso de escritura de archivos en un archivo de tarea para actualizar una tarea, permiso de lectura de archivos en un archivo de tarea para leer una tarea, eliminar permisos en un archivo de tarea para eliminar una tarea y permiso de ejecución de archivos en una tarea para ejecutar una tarea mediante los métodos [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) o [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) [**(RegisteredTask.Run**](registeredtask-run.md) y [**RunEx**](registeredtask-runex.md) para scripting). Los miembros del grupo Administradores o de la cuenta SYSTEM pueden leer, actualizar, eliminar y ejecutar cualquier tarea. Los miembros del grupo Usuarios, la cuenta LocalService y la cuenta NetworkService solo pueden leer, actualizar, eliminar y ejecutar las tareas que han creado. Este comportamiento predeterminado cambia cuando se cambia la DACL del archivo de tarea, en cuyo caso la DACL define qué usuarios tienen permiso de escritura, lectura, ejecución y eliminación de archivos. Para establecer permisos para un archivo de tareas, use el método IRegisteredTask.SetSecurityDescriptor (RegisteredTask.SetSecurityDescriptor para scripting) o establezca el descriptor de seguridad al registrar la tarea mediante los métodos [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Un usuario debe tener el permiso WriteDAC además de los permisos de lectura y escritura para actualizar una tarea si la actualización de la tarea requiere un cambio en la DACL de la tarea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de registro de tareas](task-registration-information.md)
</dt> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Protección de seguridad de tareas](task-security-hardening.md)
</dt> <dt>

[**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Propiedad principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**TIPO DE \_ INICIO DE SESIÓN DE \_ TAREA**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




