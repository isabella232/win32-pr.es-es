---
title: Tareas
description: Una tarea es el trabajo programado que realiza Programador de tareas servicio.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tareas Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f6122bcf32e0c3e242b6dce119432a9014718d4b65d19c613ce27794355491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517115"
---
# <a name="tasks"></a>Tareas

Una tarea es el trabajo programado que realiza Programador de tareas servicio. Una tarea se compone de componentes diferentes, pero una tarea debe contener un desencadenador que el Programador de tareas usa para iniciar la tarea y una acción que describe el trabajo que el Programador de tareas realizará.

Cuando se crea una tarea, se almacena en una carpeta de tareas. Se puede acceder a las carpetas de tareas a través de la interfaz [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) [**(TaskFolder**](taskfolder.md) para scripting) y se puede acceder a las tareas a través de la interfaz [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) [**(RegisteredTask**](registeredtask.md) para scripting) cuando se crean. Puede cambiar las listas de control de acceso (ACL) de las tareas y carpetas de tareas para conceder o denegar a determinados usuarios y grupos acceso a una carpeta de tareas o tareas. Esto se puede hacer mediante el método [**IRegisteredTask::SetSecurityDescriptor,**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) el método [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) o especificando un descriptor de seguridad cuando se registra una tarea mediante el método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**RegisterTask.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

> [!Note]  
> Si se deniega el acceso a la cuenta del sistema local a un archivo de tareas o a una carpeta de tareas, el Programador de tareas servicio puede producir resultados inesperados.

 

## <a name="components-of-a-task"></a>Componentes de una tarea

En la ilustración siguiente se muestran los componentes de la tarea.

![componentes de tareas](images/taskcomponents.png)

La lista siguiente contiene una breve descripción de cada componente de tarea:

-   Desencadenadores: Programador de tareas desencadenadores basados en eventos o en tiempo para saber cuándo iniciar una tarea. Cada tarea puede especificar uno o varios desencadenadores para iniciar la tarea.

    Para obtener más información sobre los desencadenadores, vea [Desencadenadores de tareas.](task-triggers.md)

-   Acciones: estas son las acciones, el trabajo real, que realiza la tarea. Cada tarea puede especificar una o varias acciones para completar su trabajo.

    Para obtener más información sobre las acciones, vea [Acciones de tarea](task-actions.md).

-   Entidades de seguridad: las entidades de seguridad definen el contexto de seguridad en el que se ejecuta la tarea. Por ejemplo, una entidad de seguridad podría definir un usuario o grupo de usuarios específico que pueda ejecutar la tarea.

    Para obtener más información sobre las entidades de seguridad, vea [Contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

-   Configuración: esta es la configuración que el Programador de tareas usa para ejecutar la tarea con respecto a las condiciones externas a la propia tarea. Por ejemplo, esta configuración puede especificar la prioridad de la tarea con respecto a otras tareas, si se pueden ejecutar varias instancias de la tarea, cómo se controla la tarea cuando el equipo está en una condición inactiva y otras condiciones.

    Para obtener más información sobre la configuración de tareas, [**vea ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) [**(TaskSettings**](tasksettings.md) para scripting).

    > [!Note]  
    > De forma predeterminada, una tarea se detendrán 72 horas después de que empiece a ejecutarse. Para cambiar esto, cambie la opción [**ExecutionTimeLimit.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit)

     

-   Información de registro: se trata de información administrativa que se recopila cuando se registra la tarea. Por ejemplo, esta información describe el autor de la tarea, la fecha en que se registró la tarea, una descripción XML de la tarea y otra información.

    Para obtener más información sobre la información de registro de tareas, vea [Información de registro de tareas](task-registration-information.md).

-   Datos: se trata de documentación adicional sobre la tarea proporcionada por el autor de la tarea. Por ejemplo, estos datos pueden contener ayuda XML que los usuarios pueden usar al ejecutar la tarea.

## <a name="task-apis"></a>API de tareas

Programador de tareas 2.0 proporciona dos conjuntos de API: un conjunto de objetos de scripting e interfaces para Programador de tareas 2.0. Para obtener más información, [vea Programador de tareas referencia](task-scheduler-reference.md)de .

La compatibilidad de tareas, que se establece a través de la propiedad [**Compatibilidad,**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) solo debe establecerse en TASK COMPATIBILITY V1 si se debe tener acceso a una tarea o modificarla desde un equipo \_ Windows \_ XP, Windows Server 2003 o Windows 2000. De lo contrario, se recomienda usar la Programador de tareas 2.0 porque tiene más características.

A partir Programador de tareas 2.0, la interfaz [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) [**(TaskService**](taskservice.md) para scripting) se usa como punto de partida para crear tareas en carpetas especificadas. La [**interfaz ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) [**(TaskDefinition**](taskdefinition.md) para scripting) se usa para contener todos los componentes de una tarea, como la configuración, las acciones y los desencadenadores. Las [**API ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) proporcionan propiedades que luego se usan para definir los demás componentes de la tarea. Programador de tareas 1.0 proporciona la [**interfaz ITask,**](/windows/desktop/api/Mstask/nn-mstask-itask) que solo se admite por compatibilidad con versiones anteriores.

Para el scripting, las interfaces Programador de tareas se asignan a objetos de scripting que tienen nombres, propiedades y métodos similares. Por ejemplo, el objeto de scripting [**TaskService**](taskservice.md) tiene las mismas propiedades y métodos que la [**interfaz ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

Para obtener más información y ejemplos sobre cómo usar las interfaces Programador de tareas, los objetos de scripting y XML, vea [Using the Programador de tareas](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Programador de tareas 1.0 Tasks

Una Programador de tareas 1.0 es cualquier aplicación o tipo de archivo que el Programador de tareas pueda ejecutar. Estos pueden incluir cualquiera de los siguientes (según sea compatible con el sistema operativo en el que se ejecutará la tarea): aplicaciones Win32, aplicaciones Win16, aplicaciones del sistema operativo/2, aplicaciones MS-DOS, archivos por lotes (.bat), archivos de comandos ( .cmd) o cualquier tipo de archivo registrado \* \* correctamente.

Los datos que describen una tarea se mantienen en un archivo de tareas que se almacena en la carpeta Tareas programadas. Para obtener más información, vea [*Scheduled Tasks folder*](s.md). El nombre de estos archivos de tarea incluye el nombre de la tarea, seguido de una extensión de nombre de archivo .job.

Para obtener más información sobre cómo agregar Programador de tareas 1.0 tareas, vea [Agregar elementos de trabajo](adding-work-items.md).

Para obtener más información sobre cómo enumerar Programador de tareas tareas 1.0, vea [Enumeración de tareas](enumerating-tasks.md).

Para un equipo de Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo de Windows Vista, se deben completar las siguientes operaciones en el equipo de Windows Vista y el usuario que llama al método [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) debe ser miembro del grupo Administradores en el equipo Windows Vista remoto.

**Para habilitar la excepción "Compartir archivo e impresoras" en Windows Firewall**

1.  Haga clic en **Inicio** y, a continuación, en **Panel de control**.
2.  En **Panel de control**, haga clic en **Vista clásica y,** a continuación, haga doble clic **en el icono Windows Firewall.**
3.  En la ventana **Windows Firewall,** haga clic en la **pestaña Excepciones** y active la casilla **Excepción** de uso compartido de archivos e impresoras.

**Para habilitar el servicio "Registro remoto"**

-   Abra una ventana del símbolo del sistema y escriba el siguiente comando: **net start "Remote Registry".**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Acciones de tarea](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




