---
title: Programador de tareas tipos enumerados
description: Enumera las enumeraciones usadas por las API de Programador de tareas.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Programador de tareas de Programador de tareas, referencia, tipos enumerados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533615"
---
# <a name="task-scheduler-enumerated-types"></a>Programador de tareas tipos enumerados

Describe los tipos enumerados que definen las constantes utilizadas por las API de Programador de tareas.


Los siguientes tipos enumerados se introducen en Programador de tareas 2,0.



| Enumeración                                                                  | Descripción                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de acción de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | Define el tipo de acciones que puede realizar una tarea.                                                             |
| [**compatibilidad de tareas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | Define qué versiones de Programador de tareas o el comando AT con el que es compatible la tarea.                      |
| [**creación de tareas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | Define cómo el servicio Programador de tareas crea, actualiza o deshabilita la tarea.                                   |
| [**\_marcas de enumeración de tareas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | Define cómo el Programador de tareas enumera a través de las tareas registradas.                                              |
| [**\_Directiva de instancias de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | Define cómo el Programador de tareas controla las instancias existentes de la tarea cuando inicia una nueva instancia de la tarea. |
| [**TIPO de inicio de sesión de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | Define la técnica de inicio de sesión necesaria para ejecutar una tarea.                                                          |
| [**TIPO de PROCESSTOKENSID de tareas \_**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | Define los tipos de SID de proceso que pueden usar las tareas.                                                         |
| [**\_marcas de ejecución de tareas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | Define cómo se ejecuta una tarea.                                                                                       |
| [**\_tipo de nivel de tareas \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | Define las marcas de elevación de LUA que especifican con qué nivel de privilegios se ejecutará la tarea.                         |
| [**\_tipo de \_ cambio de estado de sesión de tarea \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | Define qué tipos de Terminal Server cambio de estado de sesión puede usar para desencadenar la inicio de una tarea.               |
| [**Estado de la tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | Define los diferentes Estados en los que puede estar una tarea registrada.                                                   |
| [**\_Tipo2 de desencadenador de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | Define el tipo de desencadenadores que las tareas pueden usar.                                                          |



 


> [!WARNING]
> Las enumeraciones de Programador de tareas 1,0 solo están disponibles en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003. Están en desuso en Windows Vista y pueden quitarse completamente en el futuro. En su lugar, use las enumeraciones Programador de tareas 2,0 enumeradas anteriormente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[Referencia de Programador de tareas](task-scheduler-reference.md)
</dt> </dl>

 

 




