---
title: ActionCollection. Create (método)
description: En el caso de scripting, crea y agrega una nueva acción a la colección.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Crear método Programador de tareas
- Create Method Programador de tareas, ActionCollection Object
- Programador de tareas de objeto ActionCollection, Create (método)
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534618"
---
# <a name="actioncollectioncreate-method"></a>ActionCollection. Create (método)

En el caso de scripting, crea y agrega una nueva acción a la colección.

## <a name="syntax"></a>Sintaxis


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Este parámetro se establece en una de las siguientes constantes de enumeración de [**\_ \_ tipo de acción de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tarea \_ de ACCIÓN \_ exec**</dt> <dt>0</dt> </dl>                          | La acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tarea \_ de \_ \_ Controlador com de acción**</dt> <dt>5</dt> </dl>    | La acción activa un controlador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tarea \_ de ACCIÓN de \_ envío de \_ correo electrónico**</dt> <dt>6</dt> </dl>       | Esta acción envía un mensaje de correo electrónico.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tarea \_ de ACCIÓN \_ Mostrar \_ mensaje**</dt> <dt>7</dt> </dl> | Esta acción muestra un cuadro de mensaje.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto de [**acción**](action.md) que representa la nueva acción.

## <a name="remarks"></a>Observaciones

No se pueden agregar más de 32 acciones a la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de acción de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> <dt>

[**Acción**](action.md)
</dt> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





