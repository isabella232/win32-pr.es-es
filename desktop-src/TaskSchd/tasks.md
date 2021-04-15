---
title: Tareas
description: Una tarea es el trabajo programado que realiza el servicio Programador de tareas.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Programador de tareas de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676229"
---
# <a name="tasks"></a>Tareas

Una tarea es el trabajo programado que realiza el servicio Programador de tareas. Una tarea se compone de distintos componentes, pero una tarea debe contener un desencadenador que el Programador de tareas utiliza para iniciar la tarea y una acción que describe el trabajo que realizará el Programador de tareas.

Cuando se crea una tarea, se almacena en una carpeta de tareas. Se puede tener acceso a las carpetas de tareas a través de la interfaz [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) para scripting) y se puede tener acceso a las tareas a través de la interfaz [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) para scripting) cuando se crean. Puede cambiar las listas de control de acceso (ACL) para tareas y carpetas de tareas con el fin de conceder o denegar el acceso de determinados usuarios y grupos a una carpeta de tareas o tareas. Esto se puede hacer mediante el método [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , el método [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) o especificando un descriptor de seguridad cuando una tarea se registra mediante el método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .

> [!Note]  
> Si se deniega el acceso a la cuenta de sistema local a un archivo de tarea o a una carpeta de tareas, el servicio Programador de tareas puede generar resultados inesperados.

 

## <a name="components-of-a-task"></a>Componentes de una tarea

En la ilustración siguiente se muestran los componentes de la tarea.

![componentes de tarea](images/taskcomponents.png)

La lista siguiente contiene una breve descripción de cada componente de tarea:

-   Desencadenadores: Programador de tareas usa desencadenadores basados en eventos o temporales para saber cuándo se debe iniciar una tarea. Cada tarea puede especificar uno o varios desencadenadores para iniciar la tarea.

    Para obtener más información acerca de los desencadenadores, vea [desencadenadores de tareas](task-triggers.md).

-   Acciones: estas son las acciones, el trabajo real, que realiza la tarea. Cada tarea puede especificar una o varias acciones para completar su trabajo.

    Para obtener más información sobre las acciones, vea [acciones de tarea](task-actions.md).

-   Entidades de seguridad: las entidades de seguridad definen el contexto de seguridad en el que se ejecuta la tarea. Por ejemplo, una entidad de seguridad podría definir un usuario o un grupo de usuarios específico que pueda ejecutar la tarea.

    Para obtener más información sobre las entidades de [seguridad, vea contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

-   Configuración: Estos son los valores que el Programador de tareas usa para ejecutar la tarea con respecto a las condiciones que son externas a la propia tarea. Por ejemplo, esta configuración puede especificar la prioridad de la tarea con respecto a otras tareas, si se pueden ejecutar varias instancias de la tarea, cómo se administra la tarea cuando el equipo está en una condición de inactividad y otras condiciones.

    Para obtener más información sobre la configuración de tareas, vea [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).

    > [!Note]  
    > De forma predeterminada, se detendrá una tarea 72 horas después de que empiece a ejecutarse. Puede cambiar esto cambiando el valor de [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .

     

-   Información de registro: se trata de información administrativa que se recopila cuando se registra la tarea. Por ejemplo, esta información describe el autor de la tarea, la fecha en la que se registró la tarea, una descripción XML de la tarea y otra información.

    Para obtener más información sobre la información de registro de tareas, vea [información de registro de tareas](task-registration-information.md).

-   Datos: se trata de documentación adicional acerca de la tarea proporcionada por el autor de la tarea. Por ejemplo, estos datos pueden contener ayuda XML que pueden usar los usuarios cuando ejecutan la tarea.

## <a name="task-apis"></a>API de tareas

Programador de tareas 2,0 proporciona dos conjuntos de API: un conjunto de interfaces y objetos de scripting para Programador de tareas 2,0. Para obtener más información, vea [referencia de programador de tareas](task-scheduler-reference.md).

La compatibilidad de tareas, que se establece a través de la propiedad de [**compatibilidad**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , solo se debe establecer en compatibilidad de tareas \_ \_ v1 si se debe tener acceso a una tarea o modificarla desde un equipo con Windows XP, Windows Server 2003 o Windows 2000. De lo contrario, se recomienda usar la compatibilidad con Programador de tareas 2,0 porque tiene más características.

A partir de Programador de tareas 2,0, la interfaz [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) para scripting) se usa como punto de partida para crear tareas en las carpetas especificadas. La interfaz [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) para scripting) se usa para contener todos los componentes de una tarea, como la configuración, las acciones y los desencadenadores. Las API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)y [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) proporcionan propiedades que se usan para definir los demás componentes de la tarea. Programador de tareas 1,0 proporciona la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , que solo se admite para la compatibilidad con versiones anteriores.

En el caso de scripting, las interfaces de Programador de tareas se asignan a objetos de scripting que tienen nombres, propiedades y métodos similares. Por ejemplo, el objeto de scripting [**TaskService**](taskservice.md) tiene las mismas propiedades y métodos que la interfaz [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

Para obtener más información y ejemplos sobre cómo usar las interfaces de Programador de tareas, los objetos de scripting y XML, vea [usar el programador de tareas](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Programador de tareas 1,0 tareas

Una tarea Programador de tareas 1,0 es cualquier tipo de aplicación o archivo que pueda ejecutar el Programador de tareas. Estos pueden incluir cualquiera de los siguientes elementos (tal y como lo admite el sistema operativo en el que se ejecutará la tarea): aplicaciones Win32, aplicaciones de Win16, sistema operativo/2, aplicaciones MS-DOS, archivos por lotes ( \* . bat), archivos de comandos ( \* . cmd) o cualquier tipo de archivo registrado correctamente.

Los datos que describen una tarea se guardan en un archivo de tareas que se almacena en la carpeta tareas programadas. Para obtener más información, vea [*tareas programadas (carpeta*](s.md)). El nombre de estos archivos de tarea incluye el nombre de la tarea, seguido de una extensión de nombre de archivo. Job.

Para obtener más información sobre cómo agregar Programador de tareas tareas de 1,0, vea [Agregar elementos de trabajo](adding-work-items.md).

Para obtener más información sobre la enumeración a través de Programador de tareas tareas 1,0, consulte [enumeración de tareas](enumerating-tasks.md).

En el caso de un equipo con Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo con Windows Vista, se deben completar las siguientes operaciones en el equipo con Windows Vista y el usuario que llama al método [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) debe ser miembro del grupo administradores en el equipo remoto de Windows Vista.

**Para habilitar la excepción "compartir archivos e impresoras" en firewall de Windows**

1.  Haga clic en **Inicio** y, a continuación, en **Panel de control**.
2.  En el **Panel de control**, haga clic en **vista clásica** y, a continuación, haga doble clic en el icono **firewall de Windows** .
3.  En la ventana **firewall de Windows** , haga clic en la pestaña **excepciones** y seleccione la casilla **excepción de uso compartido de archivos e impresoras** .

**Para habilitar el servicio "registro remoto"**

-   Abra una ventana del símbolo del sistema y escriba el siguiente comando: **net start "Remote Registry"**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
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

 

 




