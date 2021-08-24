---
title: Objeto ComHandlerAction
description: Objeto de scripting que representa una acción que activará un controlador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Acción del controlador COM Programador de tareas , objeto
- Objeto ComHandlerAction Programador de tareas
- Objeto ComHandlerAction Programador de tareas , descrito
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659685"
---
# <a name="comhandleraction-object"></a>Objeto ComHandlerAction

Objeto de scripting que representa una acción que activará un controlador.

## <a name="members"></a>Miembros

El **objeto ComHandlerAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ComHandlerAction** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso           | Descripción                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Classid**](comhandleraction-classid.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el identificador de la clase de controlador.<br/>                                              |
| [**data**](comhandleraction-data.md)<br/>       | Lectura/escritura<br/> | Obtiene o establece datos adicionales asociados al controlador.<br/>                              |
| [**Id**](action-id.md)<br/>                     | Lectura/escritura<br/> | Se hereda del [**objeto Action.**](action.md) Obtiene o establece el identificador de la acción.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Solo lectura<br/>  | Se hereda del [**objeto Action.**](action.md) Obtiene el tipo de la acción.<br/>               |



 

## <a name="remarks"></a>Comentarios

Los controladores COM deben implementar la [**interfaz ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para que el Programador de tareas inicie y detenga el controlador. A su vez, el controlador COM usa los métodos del [**objeto TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar el estado al Programador de tareas.

Al leer o escribir XML, se especifica una acción de controlador COM en el [**elemento ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





