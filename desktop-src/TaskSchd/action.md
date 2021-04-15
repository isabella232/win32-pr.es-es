---
title: Action (objeto)
description: Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de acción.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objeto de acción Programador de tareas
- Objeto de acción Programador de tareas, descrito
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
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534624"
---
# <a name="action-object"></a>Action (objeto)

Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de acción. El método [**ActionCollection. Create**](actioncollection-create.md) crea un objeto de acción.

## <a name="members"></a>Miembros

El objeto de **acción** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **acción** tiene estas propiedades.



| Propiedad                               | Tipo de acceso           | Descripción                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Sesión**](action-id.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece el identificador de la acción.<br/> |
| [**Tipo**](action-type.md)<br/> | Solo lectura<br/>  | Obtiene el tipo de la acción.<br/>               |



 

## <a name="remarks"></a>Observaciones

Para obtener información sobre cómo funcionan conjuntamente las acciones y tareas, vea [acciones de tarea](task-actions.md). La tabla siguiente contiene los objetos de scripting que representan las acciones que se pueden realizar:



| API                                            | Descripción                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Representa una acción que activa un controlador.                   |
| [**ExecAction**](execaction.md)               | Representa una acción que ejecuta una operación de la línea de comandos. |
| [**EmailAction**](emailaction.md)             | Representa una acción que envía un mensaje de correo electrónico.            |
| [**ShowMessageAction**](showmessageaction.md) | Representa una acción que muestra un cuadro de mensaje.               |



 

Al leer o escribir XML, las acciones de una tarea se especifican en el elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) del esquema programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) , ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas objetos de scripting](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





