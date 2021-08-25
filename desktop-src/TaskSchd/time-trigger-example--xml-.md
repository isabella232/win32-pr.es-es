---
title: Ejemplo de desencadenador de tiempo (XML)
description: El XML de este ejemplo define una tarea que comienza Bloc de notas en un momento específico.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25c4cffb3764f96a191b1c5ad0d2999664d536f2df9be9862fa98f0335f3fe23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990815"
---
# <a name="time-trigger-example-xml"></a>Ejemplo de desencadenador de tiempo (XML)

El XML de este ejemplo define una tarea que comienza Bloc de notas en un momento específico.

Para registrar una tarea definida en XML, puede usar la función [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (ubicada en el directorio C: Windows System32), puede usar el siguiente comando para registrar la \\ \\ tarea: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>Para definir una tarea para iniciar Bloc de notas en un momento específico

En el ejemplo XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (a partir de Bloc de notas), un desencadenador de tiempo único que inicia la tarea en un momento especificado y otras configuraciones de tareas que afectan a cómo controla la tarea el Programador de tareas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
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
-   [**TimeTrigger:**](taskschedulerschema-timetrigger-triggergroup-element.md)define el desencadenador de hora. En este caso, se usan tres elementos secundarios: los límites inicial y final que especifican cuándo se activa y desactiva el desencadenador, y el límite de tiempo de ejecución que especifica la cantidad máxima de tiempo en la que el desencadenador puede iniciar la tarea. El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de tiempo.
-   [**Entidad**](taskschedulerschema-principal-principaltype-element.md)de seguridad: define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración:**](taskschedulerschema-settings-tasktype-element.md)define la configuración de la tarea que Programador de tareas utiliza para realizar la tarea.
-   [**Acciones:**](taskschedulerschema-actions-tasktype-element.md)define las acciones que realiza la tarea (en este caso, ejecutando Bloc de notas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




