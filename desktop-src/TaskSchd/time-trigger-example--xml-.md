---
title: Ejemplo de desencadenador de tiempo (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas en un momento determinado.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104358610"
---
# <a name="time-trigger-example-xml"></a>Ejemplo de desencadenador de tiempo (XML)

El XML de este ejemplo define una tarea que inicia el Bloc de notas en un momento determinado.

Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>Para definir una tarea para iniciar el Bloc de notas en un momento específico

En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de tiempo que inicia la tarea a una hora especificada y otras opciones de configuración de tareas que afectan al modo en que el Programador de tareas controla la tarea.


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

A continuación se muestran algunos elementos importantes que se deben tener en cuenta al usar este ejemplo:

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.
-   [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.
-   [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): define el desencadenador de tiempo. En este caso, se usan tres elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, y el límite de tiempo de ejecución que especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea. El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de hora.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.
-   [**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




