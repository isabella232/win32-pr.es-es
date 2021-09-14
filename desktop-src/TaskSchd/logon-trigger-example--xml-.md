---
title: Ejemplo de desencadenador de inicio de sesión (XML)
description: El XML de este ejemplo define una tarea que se inicia Bloc de notas cuando un usuario inicia sesión.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886588"
---
# <a name="logon-trigger-example-xml"></a>Ejemplo de desencadenador de inicio de sesión (XML)

El XML de este ejemplo define una tarea que se inicia Bloc de notas cuando un usuario inicia sesión.

Para registrar una tarea definida en XML, puede usar la función [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (ubicada en el directorio C: Windows System32), puede usar el siguiente comando para registrar la \\ \\ tarea: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Para definir una tarea para iniciar Bloc de notas en el arranque del sistema

En el ejemplo XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (a partir de Bloc de notas), un desencadenador de inicio de sesión único que inicia la tarea cuando un usuario inicia sesión y otras opciones de configuración de tareas que afectan a cómo controla la tarea Programador de tareas.

> [!Note]  
> Establezca el valor del elemento **UserId** en un nombre de usuario en el equipo en el que está registrada la tarea.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Elementos de esquema TaskScheduler

Estos son algunos elementos importantes que hay que tener en cuenta al usar este ejemplo:

-   [**RegistrationInfo:**](taskschedulerschema-registrationinfo-tasktype-element.md)contiene información de registro sobre la tarea.
-   [**Desencadenadores:**](taskschedulerschema-triggers-tasktype-element.md)define el desencadenador que inicia la tarea.
-   [**LogonTrigger:**](taskschedulerschema-logontrigger-triggergroup-element.md)define el desencadenador de inicio de sesión. En este caso, se usan tres elementos secundarios: los límites inicial y final que especifican cuándo se activa y desactiva el desencadenador, y el [**elemento UserId**](taskschedulerschema-userid-logontriggertype-element.md) que identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.
-   [**Entidad**](taskschedulerschema-principal-principaltype-element.md)de seguridad: define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración:**](taskschedulerschema-settings-tasktype-element.md)define la configuración de la tarea que Programador de tareas utiliza para realizar la tarea.
-   [**Acciones:**](taskschedulerschema-actions-tasktype-element.md)define las acciones que realiza la tarea. En este caso, se ejecuta Bloc de notas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




