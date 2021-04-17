---
title: Contextos de seguridad para tareas
description: Las tareas se registran y se ejecutan en un contexto de seguridad específico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420341"
---
# <a name="security-contexts-for-tasks"></a>Contextos de seguridad para tareas

Las tareas se registran y se ejecutan en un contexto de seguridad específico. Los usuarios pueden crear aplicaciones para registrar, actualizar, eliminar o ejecutar tareas correctamente, pero el usuario debe proporcionar las credenciales correctas cuando se registra una tarea y la aplicación debe ejecutarse en un proceso con los privilegios correctos.

## <a name="specifying-credentials"></a>Especificar credenciales

Puede especificar el contexto de seguridad para una tarea especificando credenciales en los métodos [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para scripting) o asignando una entidad de seguridad a la [**propiedad principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition. principal**](taskdefinition-principal.md) para scripting). Si se crea una entidad de seguridad para una definición de tarea y, después, la definición de la tarea se registra con el método **RegisterTaskDefinition** con credenciales diferentes especificadas en los parámetros del método, las credenciales especificadas en el método **RegisterTaskDefinition** sobrescribirán las credenciales de la entidad de seguridad. Si se crea una entidad de seguridad para una definición de tarea mediante XML y, a continuación, el XML de la tarea se registra con el método **RegisterTask** con credenciales diferentes especificadas en los parámetros del método, las credenciales especificadas en el método **RegisterTask** sobrescribirán las credenciales de la entidad de seguridad.

Especifique una cuenta de usuario o grupo al registrar una tarea o especificar el principio para una tarea. El contexto de seguridad de la cuenta de usuario o grupo se usa para el contexto de seguridad de la tarea. En estos métodos y propiedades, también se define el tipo de inicio de sesión. El tipo de inicio de sesión se define mediante una de las constantes de la enumeración de [**\_ \_ tipo de inicio de sesión de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .

Las tareas registradas con la marca de contraseña de inicio de sesión de tarea \_ \_ o de inicio de sesión de tarea \_ \_ S4U solo se iniciarán si el usuario especificado tiene habilitado el privilegio de inicio de sesión como batch. Los usuarios del grupo administradores y operadores de copia de seguridad tienen este privilegio habilitado de forma predeterminada.

Cuando se llama al método [**ITaskService:: Connect**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService. Connect**](taskservice-connect.md) para scripting), todas las llamadas de método posteriores al servicio Programador de tareas usarán las credenciales que se pasaron al método **Connect** . Es importante tener en cuenta a la hora de registrar tareas con un tipo de inicio de sesión interactivo. Cuando se registra una tarea con el tipo de inicio de sesión igual al \_ \_ \_ token interactivo de inicio de sesión de tarea y la tarea no tiene credenciales especificadas en la propiedad [**principal**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) de la definición de tarea, especificada en los parámetros de [**REGISTERTASKDEFINITION**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)o especificados en el XML que se pasa a [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask), la tarea se registrará con las credenciales del usuario que llamó al método **Connect** .

## <a name="user-account-control-uac-security-for-tasks"></a>Seguridad de control de cuentas de usuario (UAC) para tareas

[Control de cuentas de usuario](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) permite que los usuarios ejerzan funciones generales, como la ejecución de programas y el guardado y la modificación de datos sin exponer privilegios administrativos. De forma predeterminada, una tarea se ejecuta con privilegios de bajo nivel cuando UAC está activado. Las tareas pueden especificar que se ejecuten con privilegios elevados o privilegios bajos estableciendo un nivel de privilegios de la enumeración [**Task \_ nivel \_ Type**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) para la [**propiedad nivel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**principal. nivel**](principal-runlevel.md) para scripting). El valor de la propiedad **nivel** determina el nivel de privilegio en el que se ejecutarán las acciones de una tarea. Si las acciones de una tarea deben tener privilegios elevados para ejecutarse, debe establecer la propiedad **nivel** en la **tarea \_ nivel \_ más alta**. Si una tarea se registra mediante el grupo de administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad **nivel** en la **tarea \_ nivel \_ más alta** si desea ejecutar la tarea. Si una tarea se registra mediante la cuenta de \\ Administrador de Builtin o las cuentas de sistema local o de servicio local, se omitirá la propiedad **nivel** . También se omitirá el valor de propiedad si el control de cuentas de usuario (UAC) está desactivado. El valor de la propiedad **nivel** no afecta a los permisos necesarios para ejecutar o eliminar una tarea.

> [!Note]  
> Después de actualizar un sistema operativo de Windows XP a Windows Vista, las tareas que se registraron con la \\ cuenta de administrador de Builtin en Windows XP tendrán la propiedad [**nivel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) establecida en **Task \_ nivel \_ Lua**. Esto podría provocar errores en algunas tareas. Puede actualizar esta propiedad manualmente para asegurarse de que todas las tareas se ejecutarán.

 

Desde un proceso con pocos privilegios, no puede registrar una tarea con la propiedad [**nivel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a la **tarea \_ nivel \_ más alta**, pero puede registrar una tarea con la propiedad **nivel** igual a la **tarea \_ nivel \_ Lua**. Las acciones de tarea se ejecutarán con privilegios bajos. No tiene permiso para registrar la tarea como Builtin/administrador, sistema local o para un grupo.

Desde un proceso con privilegios elevados, puede registrar una tarea con la propiedad [**nivel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **Task \_ nivel \_ Highest** o la **tarea \_ nivel \_ Lua**. La tarea se ejecutará con un nivel de privilegio decidido por la propiedad **nivel** , a menos que esté usando la cuenta de administrador, en cuyo caso la tarea se ejecuta con privilegios elevados.

Desde un proceso con privilegios elevados, puede registrar una tarea Programador de tareas 1,0. El servicio Programador de tareas establecerá el nivel de ejecución de la tarea en la tarea \_ nivel \_ más alto y la tarea se ejecutará con privilegios elevados.

A partir de un proceso con pocos privilegios, también puede registrar una tarea Programador de tareas 1,0. El servicio Programador de tareas establecerá el nivel de ejecución de la tarea en la tarea \_ nivel \_ Lua y la tarea se ejecutará con privilegios bajos. Si esta tarea se actualiza a partir de un proceso con privilegios elevados, el nivel de ejecución de la tarea seguirá siendo TASK \_ nivel \_ Lua.

## <a name="security-for-registering-tasks"></a>Seguridad para registrar tareas

Cuando se registra una tarea desde una cuenta que es miembro del grupo administradores, solo es necesario especificar una contraseña mientras se registra la tarea en las siguientes situaciones:

-   Si registra la tarea para que se ejecute en el contexto de seguridad de su cuenta o de una cuenta de usuario diferente, use la marca de contraseña de inicio de sesión de tarea \_ \_ en el método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .
-   Si registra la tarea para que se ejecute en el contexto de seguridad de una cuenta de usuario diferente y utiliza la \_ marca de inicio de sesión de tarea \_ S4U en el método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

No se puede usar un grupo de usuarios como contexto de seguridad de una tarea al registrar la tarea mediante la \_ marca S4U de inicio de sesión de tarea \_ o la \_ \_ marca de contraseña de inicio de sesión de tarea en el método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Cuando se registra una tarea desde una cuenta de usuario que no es miembro del grupo administradores, no es necesario especificar una contraseña al registrar la tarea si se registra la tarea para que se ejecute en el contexto de seguridad de su cuenta y se usa el tipo de inicio de sesión de S4U o interactivo. De lo contrario, debe especificar una contraseña al registrar la tarea. Además, no puede registrar la tarea mediante la cuenta de servicio local o mediante un grupo para el contexto de seguridad de la tarea.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Seguridad para leer, actualizar, eliminar y ejecutar tareas

De forma predeterminada, un usuario que crea una tarea puede leer, actualizar, eliminar y ejecutar la tarea. Un usuario debe tener permiso de escritura en un archivo de tarea para actualizar una tarea, el permiso de lectura de archivo en un archivo de tarea para leer una tarea, el permiso delete en un archivo de tarea para eliminar una tarea y el permiso Execute File en una tarea para ejecutar una tarea mediante los métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) o [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask. Run**](registeredtask-run.md) y [**RunEx**](registeredtask-runex.md) para scripting). Los miembros del grupo administradores o la cuenta del sistema pueden leer, actualizar, eliminar y ejecutar cualquier tarea. Los miembros del grupo usuarios, la cuenta LocalService y la cuenta NetworkService solo pueden leer, actualizar, eliminar y ejecutar las tareas que han creado. Este comportamiento predeterminado se cambia cuando se cambia la DACL del archivo de tarea, en cuyo caso la DACL define qué usuarios tienen el permiso escribir, leer, ejecutar y eliminar archivos. Para establecer permisos para un archivo de tarea, use el método IRegisteredTask. SetSecurityDescriptor (RegisteredTask. SetSecurityDescriptor para scripting) o establezca el descriptor de seguridad al registrar la tarea mediante los métodos [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Un usuario debe tener el permiso WriteDAC además de los permisos de lectura y escritura para actualizar una tarea si la actualización de la tarea requiere un cambio en la DACL de la tarea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de registro de tareas](task-registration-information.md)
</dt> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Protección de la seguridad de tareas](task-security-hardening.md)
</dt> <dt>

[**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Propiedad principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**tipo de inicio de sesión de tarea \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




