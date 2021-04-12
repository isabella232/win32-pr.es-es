---
title: Programador de tareas objetos de scripting
description: Los objetos de scripting que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas para los programadores de scripts de Visual Basic y Visual Basic.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Programador de tareas Programador de tareas, referencia, objetos de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104271917"
---
# <a name="task-scheduler-scripting-objects"></a>Programador de tareas objetos de scripting

Los objetos de scripting que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas para los programadores de scripts de Visual Basic y Visual Basic.


Los objetos siguientes se incluyen en Programador de tareas 2,0.



| Object                                                         | Descripción                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acción**](action.md)                                       | Proporciona las propiedades comunes que heredan todos los objetos de acción.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Contiene las acciones realizadas por la tarea.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se inicia el sistema.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Representa una acción que activa un controlador.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Representa un desencadenador que inicia una tarea en función de una programación diaria.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Representa una acción que envía un mensaje de correo electrónico.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Representa una acción que ejecuta una operación de la línea de comandos.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Representa un desencadenador que inicia una tarea en una programación mensual de día de la semana.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Representa un desencadenador que inicia una tarea basada en una programación mensual.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Proporciona la configuración que usa el servicio de Programador de tareas para obtener un perfil de red.                                                                                                                                                               |
| [**Principal**](principal.md)                                 | Proporciona las credenciales de seguridad para una entidad de seguridad.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contiene todas las tareas que están registradas.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Proporciona la información administrativa que se puede utilizar para describir la tarea. Esta información incluye detalles como, por ejemplo, una descripción de la tarea, el autor de la tarea, la fecha de registro de la tarea y el descriptor de seguridad de la tarea. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Representa un desencadenador que inicia una tarea cuando se registra la tarea.                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | Define la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Proporciona los métodos para obtener información y controlar una tarea en ejecución.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Se utiliza para recuperar una tarea en ejecución.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Se usa para desencadenar tareas de conexión o desconexión de la consola, conexión remota o desconexión, o notificaciones de bloqueo o desbloqueo de la estación de trabajo.                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Cuenta el número de carpetas de la colección y recupera una carpeta especificada de la colección.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Crea un par nombre-valor en el que el nombre está asociado con el valor.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contiene una colección de pares de nombre y valor de objeto [**TaskNamedValuePair**](tasknamedvaluepair.md) .                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Proporciona acceso al servicio de Programador de tareas para administrar tareas registradas.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Proporciona la configuración que usa el Programador de tareas servicios para realizar la tarea.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Define las variables de tarea que se pueden pasar como parámetros a los controladores de tareas y los archivos ejecutables externos iniciados por las tareas.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se activa el desencadenador.                                                                                                                                                                                |
| [**Activado**](trigger.md)                                     | Proporciona las propiedades comunes que heredan todos los objetos de desencadenador.                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | Se utiliza para agregar, quitar y recuperar los desencadenadores de una tarea.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Representa un desencadenador que inicia una tarea basada en una programación semanal.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Programador de tareas](task-scheduler-reference.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 




