---
title: Propiedad Action.Type
description: Para el scripting, obtiene el tipo de la acción.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Tipo de propiedad Programador de tareas
- Propiedad type Programador de tareas , objeto Action
- Objeto action Programador de tareas , propiedad Type
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
ms.openlocfilehash: 499c7e42b5b2578928796e6f878219e0c53612e454948d390cdb631dcaccd64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739035"
---
# <a name="actiontype-property"></a>Propiedad Action.Type

Para el scripting, obtiene el tipo de la acción.

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad devuelve una de las siguientes constantes de [**enumeración TASK \_ ACTION \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**TASK \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**TASK \_ CONTROLADOR \_ COM \_ DE ACCIÓN**</dt> <dt>5</dt> </dl>    | Esta acción desaprende un controlador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**TASK \_ ACCIÓN \_ ENVIAR \_ CORREO ELECTRÓNICO**</dt> <dt>6</dt> </dl>       | Esta acción envía un mensaje de correo electrónico.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**TASK \_ ACCIÓN \_ MOSTRAR \_ MENSAJE**</dt> <dt>7</dt> </dl> | Esta acción muestra un cuadro de mensaje.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

El tipo de acción se define cuando se crea la acción y no se puede cambiar más adelante. Para obtener información sobre cómo crear una acción, [**vea ActionCollection.Create**](actioncollection-create.md).

Para obtener información sobre cómo funcionan conjuntamente las acciones y las tareas, vea [Acciones de tarea](task-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO \_ DE ACCIÓN \_ TASK**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Acción**](action.md)
</dt> </dl>

 

 





