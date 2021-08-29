---
title: Objeto TaskFolder
description: Objeto de scripting que proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- TaskFolder object Programador de tareas
- Objeto TaskFolder Programador de tareas , descrito
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521c45e0492507cba3dcf509b53b748d5068dd592c45ff7a17fa8766ff8ff85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010945"
---
# <a name="taskfolder-object"></a>Objeto TaskFolder

Objeto de scripting que proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.

## <a name="members"></a>Miembros

El **objeto TaskFolder** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto TaskFolder** tiene estos métodos.



| Método                                                              | Descripción                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | Crea una carpeta para las tareas relacionadas.<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | Elimina una subcarpeta de la carpeta primaria.<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | Elimina una tarea de la carpeta .<br/>                                                                                                     |
| [**Getfolder**](taskfolder-getfolder.md)                           | Obtiene una carpeta que contiene tareas en una ubicación especificada.<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | Obtiene todas las subcarpetas de la carpeta.<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | Obtiene el descriptor de seguridad de la carpeta.<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | Obtiene una tarea en una ubicación especificada de una carpeta.<br/>                                                                                    |
| [**GetTasks**](taskfolder-gettasks.md)                             | Obtiene todas las tareas de la carpeta.<br/>                                                                                                   |
| [**RegisterTask**](taskfolder-registertask.md)                     | Registra (crea) una nueva tarea en la carpeta mediante XML para definir la tarea.<br/>                                                          |
| [**RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) | Registra (crea) una tarea en una ubicación especificada mediante la [**interfaz ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) para definir una tarea.<br/> |
| [**SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)   | Establece el descriptor de seguridad de la carpeta.<br/>                                                                                        |



 

### <a name="properties"></a>Propiedades

El **objeto TaskFolder** tiene estas propiedades.



| Propiedad                                   | Tipo de acceso          | Descripción                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Nombre**](taskfolder-name.md)<br/> | Solo lectura<br/> | Obtiene el nombre que se usa para identificar la carpeta que contiene una tarea.<br/> |
| [**Ruta de acceso**](taskfolder-path.md)<br/> | Solo lectura<br/> | Obtiene la ruta de acceso a donde se almacena la carpeta.<br/>                            |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting),](time-trigger-example--scripting-.md)Ejemplo de desencadenador de eventos [(scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Ejemplo de desencadenador diario [(scripting),](daily-trigger-example--scripting-.md)Ejemplo de desencadenador de registro [(scripting)](registration-trigger-example--scripting-.md), Ejemplo de desencadenador semanal [(scripting)](weekly-trigger-example--scripting-.md), Ejemplo de desencadenador de inicio [(scripting)](logon-trigger-example--scripting-.md), Ejemplo de desencadenador de arranque [(scripting)](boot-trigger-example--scripting-.md)o Mostrar nombres y estados de tareas [(scripting).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





