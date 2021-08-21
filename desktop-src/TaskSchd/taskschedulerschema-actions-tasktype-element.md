---
title: Elemento Actions (taskType)
description: Contiene las acciones realizadas por la tarea.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Elemento Actions (taskType) Programador de tareas
- actions Programador de tareas , XML
- Elemento Actions Programador de tareas
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79fb5fe36b6fcff3622e0d12f0571e7f06c5f00d1ae930abc2bca805315f7dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357111"
---
# <a name="actions-tasktype-element"></a>Elemento Actions (taskType)

Contiene las acciones realizadas por la tarea.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

El **elemento Actions** se define mediante el tipo complejo [**taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Describe la tarea que realiza el servicio Programador de tareas trabajo.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                    | Tipo                                                                       | Descripción                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Especifica una acción que llama a un controlador.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Especifica una acción que envía un mensaje de correo electrónico.<br/>            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Especifica una acción que muestra un cuadro de mensaje.<br/>               |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo | Descripción                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Context |      | Identificador principal del usuario que es el contexto de seguridad para las acciones de la tarea.<br/> |



## <a name="remarks"></a>Comentarios

El grupo [**actionGroup**](taskschedulerschema-actiongroup-group.md) define los elementos secundarios enumerados anteriormente (máximo 32). Estos elementos se pueden agregar en cualquier orden.

Para el desarrollo de C++, las acciones de una tarea se definen en la [**interfaz IActionCollection.**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)

Para el desarrollo de scripts, las acciones de una tarea se definen en el [**objeto ActionCollection.**](actioncollection.md)

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo completo del XML para una tarea que contiene una sola acción de ejecución, vea Ejemplo de desencadenador de tiempo [(XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





