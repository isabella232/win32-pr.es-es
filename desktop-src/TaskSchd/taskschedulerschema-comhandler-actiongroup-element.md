---
title: Elemento ComHandler (actionGroup)
description: Especifica una acción que llama a un controlador.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento ComHandler Programador de tareas
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aba73244c3dc5217bcfe7350462200cd3226f0607c6d68ce5c6bcb8f5574b7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943242"
---
# <a name="comhandler-actiongroup-element"></a>Elemento ComHandler (actionGroup)

Especifica una acción que llama a un controlador.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

El **elemento ComHandler** se define mediante [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                         | Derivado de                                                       | Descripción                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                         | Descripción                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Classid**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Especifica el identificador de la clase de controlador.<br/>         |
| [**data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datatype**](taskschedulerschema-datatype-complextype.md) | Especifica datos adicionales asociados al controlador.<br/> |



## <a name="remarks"></a>Comentarios

Las aplicaciones definen una acción de controlador COM mediante [**la interfaz IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

### <a name="attributes"></a>Atributos

El siguiente atributo se define mediante el [**tipo complejo actionBaseType.**](taskschedulerschema-actionbasetype-complextype.md)

-   Id.: identificador de la acción realizada por la tarea.

## <a name="examples"></a>Ejemplos

El código XML siguiente define una acción de controlador COM.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





