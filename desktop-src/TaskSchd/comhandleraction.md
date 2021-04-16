---
title: Objeto ComHandlerAction
description: Objeto de scripting que representa una acción que activa un controlador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Acción del controlador COM Programador de tareas, objeto
- Objeto ComHandlerAction Programador de tareas
- Programador de tareas de objeto ComHandlerAction, descrito
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
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488938"
---
# <a name="comhandleraction-object"></a>Objeto ComHandlerAction

Objeto de scripting que representa una acción que activa un controlador.

## <a name="members"></a>Miembros

El objeto **ComHandlerAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ComHandlerAction** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso           | Descripción                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassId**](comhandleraction-classid.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el identificador de la clase de controlador.<br/>                                              |
| [**Data**](comhandleraction-data.md)<br/>       | Lectura/escritura<br/> | Obtiene o establece datos adicionales que están asociados al controlador.<br/>                              |
| [**Sesión**](action-id.md)<br/>                     | Lectura/escritura<br/> | Heredado del objeto de [**acción**](action.md) . Obtiene o establece el identificador de la acción.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Solo lectura<br/>  | Heredado del objeto de [**acción**](action.md) . Obtiene el tipo de la acción.<br/>               |



 

## <a name="remarks"></a>Observaciones

Los controladores COM deben implementar la interfaz [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para que el programador de tareas inicie y detenga el controlador. A su vez, el controlador COM usa los métodos del objeto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar el estado de vuelta al programador de tareas.

Al leer o escribir XML, se especifica una acción de controlador COM en el elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Objetos Programador de tareas](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





