---
title: Ejemplo de desencadenador diario (XML)
description: En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas a las 8 00 A.M. todos los días.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "103785524"
---
# <a name="daily-trigger-example-xml"></a>Ejemplo de desencadenador diario (XML)

En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas a las 8:00 A.M. todos los días. En el ejemplo también se muestra cómo establecer un patrón de repetición para que el desencadenador repita la tarea.

Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>Para definir una tarea para iniciar el Bloc de notas todos los días a las 8:00 A.M.

En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de calendario (inicia la tarea todos los días a las 8:00 AM) y otras opciones de configuración de tareas que afectan al modo en que la tarea se controla mediante Programador de tareas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
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

Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contiene información de registro sobre la tarea.

-   [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md)

    Define el desencadenador que inicia la tarea.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Define el desencadenador de calendario diario. En este caso, se usan cuatro elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, la programación diaria y el patrón de repetición de la tarea. El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de calendario.

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Define la programación diaria. En este caso, el intervalo se establece para realizar la tarea cada día.

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración**](taskschedulerschema-settings-tasktype-element.md)

    Define la configuración de la tarea que Programador de tareas usa para realizar la tarea.

-   [**Acciones**](taskschedulerschema-actions-tasktype-element.md)

    Define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




