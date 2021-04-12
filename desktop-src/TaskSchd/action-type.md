---
title: Action. Type (propiedad)
description: En el caso de scripting, obtiene el tipo de la acción.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Propiedad Type Programador de tareas
- Propiedad Type Programador de tareas, objeto Action
- Objeto de acción Programador de tareas, propiedad de tipo
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491704"
---
# <a name="actiontype-property"></a>Action. Type (propiedad)

En el caso de scripting, obtiene el tipo de la acción.

## <a name="syntax"></a>Sintaxis


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad devuelve una de las siguientes constantes de enumeración de [**\_ \_ tipo de acción de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tarea \_ de ACCIÓN \_ exec**</dt> <dt>0</dt> </dl>                          | Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tarea \_ de \_ \_ Controlador com de acción**</dt> <dt>5</dt> </dl>    | Esta acción activa un controlador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tarea \_ de ACCIÓN de \_ envío de \_ correo electrónico**</dt> <dt>6</dt> </dl>       | Esta acción envía un mensaje de correo electrónico.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tarea \_ de ACCIÓN \_ Mostrar \_ mensaje**</dt> <dt>7</dt> </dl> | Esta acción muestra un cuadro de mensaje.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

El tipo de acción se define cuando se crea la acción y no se puede cambiar más adelante. Para obtener información sobre cómo crear una acción, vea [**ActionCollection. Create**](actioncollection-create.md).

Para obtener información sobre cómo funcionan conjuntamente las acciones y tareas, vea [acciones de tarea](task-actions.md).

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

[**Acción**](action.md)
</dt> </dl>

 

 





