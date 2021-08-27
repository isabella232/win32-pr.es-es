---
title: Método ActionCollection.Create
description: Para el scripting, crea y agrega una nueva acción a la colección.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Creación de un método Programador de tareas
- Crear método Programador de tareas , objeto ActionCollection
- ActionCollection object Programador de tareas , Create method
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
ms.openlocfilehash: 7cce517ae33681fcb106e83720fc5ddd7685f26f673c466e24162ce95e9ca442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072705"
---
# <a name="actioncollectioncreate-method"></a>Método ActionCollection.Create

Para el scripting, crea y agrega una nueva acción a la colección.

## <a name="syntax"></a>Sintaxis


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Este parámetro se establece en una de las siguientes constantes de [**enumeración TASK \_ ACTION \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**TASK \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | La acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**TASK \_ CONTROLADOR \_ COM \_ DE ACCIÓN**</dt> <dt>5</dt> </dl>    | La acción desaprende un controlador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**TASK \_ ACCIÓN \_ ENVIAR \_ CORREO ELECTRÓNICO**</dt> <dt>6</dt> </dl>       | Esta acción envía un mensaje de correo electrónico.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**TASK \_ ACCIÓN \_ MOSTRAR \_ MENSAJE**</dt> <dt>7</dt> </dl> | Esta acción muestra un cuadro de mensaje.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Action**](action.md) que representa la nueva acción.

## <a name="remarks"></a>Comentarios

No se pueden agregar más de 32 acciones a la colección.

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

 

 





