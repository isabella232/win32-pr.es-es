---
title: Objeto Action
description: Objeto de scripting que proporciona las propiedades comunes heredadas por todos los objetos de acción.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objeto action Programador de tareas
- Objeto de acción Programador de tareas , descrito
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739045"
---
# <a name="action-object"></a>Objeto Action

Objeto de scripting que proporciona las propiedades comunes heredadas por todos los objetos de acción. El método [**ActionCollection.Create**](actioncollection-create.md) crea un objeto action.

## <a name="members"></a>Miembros

El **objeto Action** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Action** tiene estas propiedades.



| Propiedad                               | Tipo de acceso           | Descripción                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Id**](action-id.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece el identificador de la acción.<br/> |
| [**Tipo**](action-type.md)<br/> | Solo lectura<br/>  | Obtiene el tipo de la acción.<br/>               |



 

## <a name="remarks"></a>Comentarios

Para obtener información sobre cómo funcionan conjuntamente las acciones y las tareas, vea [Acciones de tarea](task-actions.md). La tabla siguiente contiene los objetos de scripting que representan las acciones que se pueden realizar:



| API                                            | Descripción                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Representa una acción que llama a un controlador.                   |
| [**ExecAction**](execaction.md)               | Representa una acción que ejecuta una operación de línea de comandos. |
| [**EmailAction**](emailaction.md)             | Representa una acción que envía un mensaje de correo electrónico.            |
| [**ShowMessageAction**](showmessageaction.md) | Representa una acción que muestra un cuadro de mensaje.               |



 

Al leer o escribir XML, las acciones de una tarea se especifican en el [**elemento Actions**](taskschedulerschema-actions-tasktype-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting),](time-trigger-example--scripting-.md) Ejemplo de desencadenador de eventos [(scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Ejemplo de desencadenador diario [(scripting),](daily-trigger-example--scripting-.md)Ejemplo de desencadenador de registro [(scripting)](registration-trigger-example--scripting-.md), Ejemplo de desencadenador semanal [(scripting),](weekly-trigger-example--scripting-.md)Ejemplo de desencadenador de inicio de sesión [(scripting)](logon-trigger-example--scripting-.md)o Ejemplo de desencadenador de arranque [(scripting).](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas scripting de objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





