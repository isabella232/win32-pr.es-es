---
title: ActionCollection, objeto
description: Objeto de scripting que contiene las acciones realizadas por la tarea.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- acciones Programador de tareas , objeto de colección
- Objeto ActionCollection Programador de tareas
- Objeto ActionCollection Programador de tareas , descrito
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5356757d232570a31f5c8d05e01b695f130a33e34c1c0e98689b1c74feba40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011725"
---
# <a name="actioncollection-object"></a>ActionCollection, objeto

Objeto de scripting que contiene las acciones realizadas por la tarea.

## <a name="members"></a>Miembros

El **objeto ActionCollection** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto ActionCollection** tiene estos métodos.



| Método                                    | Descripción                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Borrar**](actioncollection-clear.md)   | Borra todas las acciones de la colección.<br/>      |
| [**Crear**](actioncollection-create.md) | Crea y agrega una nueva acción a la colección.<br/> |
| [**Quitar**](actioncollection-remove.md) | Quita una acción especificada de la colección.<br/>  |



 

### <a name="properties"></a>Propiedades

El **objeto ActionCollection** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso           | Descripción                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el identificador de la entidad de seguridad de la tarea.<br/> |
| [**Count**](actioncollection-count.md)<br/>     | Solo lectura<br/>  | Obtiene el número de acciones de la colección.<br/>              |
| [**Elemento**](actioncollection-item.md)<br/>       | Solo lectura<br/>  | Obtiene una acción especificada de la colección.<br/>               |
| [**Xmltext**](actioncollection-xmltext.md)<br/> | Lectura/escritura<br/> | Obtiene o establece una versión con formato XML de la colección.<br/>   |



 

## <a name="remarks"></a>Comentarios

Al leer o escribir XML, las acciones de una tarea se especifican en el [**elemento Actions**](taskschedulerschema-actions-tasktype-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting),](time-trigger-example--scripting-.md)Ejemplo de desencadenador de eventos [(scripting),](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))Ejemplo de desencadenador diario [(scripting),](daily-trigger-example--scripting-.md)Ejemplo de desencadenador de registro [(scripting),](registration-trigger-example--scripting-.md)Ejemplo de desencadenador semanal [(scripting),](weekly-trigger-example--scripting-.md)Ejemplo de desencadenador de inicio [(scripting)](logon-trigger-example--scripting-.md)o Ejemplo de desencadenador de arranque [(scripting).](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





