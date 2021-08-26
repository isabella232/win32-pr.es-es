---
title: Programador de tareas scripting de objetos
description: Los objetos de scripting que se describen en los temas siguientes proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas para los desarrolladores de scripts Visual Basic y Visual Basic de scripts.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Programador de tareas Programador de tareas , referencia, objetos de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f42eac1c9e8904933cedba54d1b51e5cc63919279de93286bfa658be1f60b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100115"
---
# <a name="task-scheduler-scripting-objects"></a>Programador de tareas scripting de objetos

Los objetos de scripting que se describen en los temas siguientes proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas para los desarrolladores de scripts Visual Basic y Visual Basic de scripts.


Los siguientes objetos se presentan en Programador de tareas 2.0.



| Object                                                         | Descripción                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acción**](action.md)                                       | Proporciona las propiedades comunes heredadas por todos los objetos de acción.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Contiene las acciones realizadas por la tarea.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se arranca el sistema.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Representa una acción que llama a un controlador.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Representa un desencadenador que inicia una tarea en función de una programación diaria.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Representa una acción que envía un mensaje de correo electrónico.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Representa una acción que ejecuta una operación de línea de comandos.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en una condición de inactividad.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Representa un desencadenador que inicia una tarea según una programación mensual del día de la semana.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Representa un desencadenador que inicia una tarea en función de una programación mensual.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Proporciona la configuración que el Programador de tareas utiliza para obtener un perfil de red.                                                                                                                                                               |
| [**Principal**](principal.md)                                 | Proporciona las credenciales de seguridad para una entidad de seguridad.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contiene todas las tareas registradas.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Proporciona la información administrativa que se puede usar para describir la tarea. Esta información incluye detalles como una descripción de la tarea, el autor de la tarea, la fecha en que se registra la tarea y el descriptor de seguridad de la tarea. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Representa un desencadenador que inicia una tarea cuando se registra la tarea.                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | Define la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Proporciona los métodos para obtener información de una tarea en ejecución y controlarla.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Se usa para recuperar una tarea en ejecución.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Se usa para desencadenar tareas para la conexión o desconexión de la consola, la conexión remota o la desconexión, o las notificaciones de bloqueo o desbloqueo de la estación de trabajo.                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Cuenta el número de carpetas de la colección y recupera una carpeta especificada de la colección.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Crea un par nombre-valor en el que el nombre está asociado al valor.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contiene una colección de pares nombre-valor de objeto [**TaskNamedValuePair.**](tasknamedvaluepair.md)                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Proporciona acceso al servicio Programador de tareas para administrar las tareas registradas.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Proporciona la configuración que el Programador de tareas utiliza para realizar la tarea.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Define variables de tarea que se pueden pasar como parámetros a controladores de tareas y ejecutables externos que inician las tareas.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Representa un desencadenador que inicia una tarea cuando se activa el desencadenador.                                                                                                                                                                                |
| [**detonante**](trigger.md)                                     | Proporciona las propiedades comunes heredadas por todos los objetos de desencadenador.                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | Se usa para agregar, quitar y recuperar los desencadenadores de una tarea.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Representa un desencadenador que inicia una tarea basada en una programación semanal.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas referencia](task-scheduler-reference.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 




