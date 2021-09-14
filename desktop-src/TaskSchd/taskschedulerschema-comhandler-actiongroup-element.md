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
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071052"
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
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datatype**](taskschedulerschema-datatype-complextype.md) | Especifica datos adicionales asociados al controlador.<br/> |



## <a name="remarks"></a>Observaciones

Las aplicaciones definen una acción de controlador COM mediante [**la interfaz IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

### <a name="attributes"></a>Atributos

El siguiente atributo se define mediante el [**tipo complejo actionBaseType.**](taskschedulerschema-actionbasetype-complextype.md)

-   Id.: identificador de la acción realizada por la tarea.

## <a name="examples"></a>Ejemplos

El xml siguiente define una acción de controlador COM.


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

 

 





