---
title: Elemento comhandler (actionGroup)
description: Especifica una acción que activa un controlador.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento comhandler Programador de tareas
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996847"
---
# <a name="comhandler-actiongroup-element"></a>Elemento comhandler (actionGroup)

Especifica una acción que activa un controlador.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

[**ActionGroup**](taskschedulerschema-actiongroup-group.md) define el elemento **comhandler** .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                         | Derivado de                                                       | Descripción                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                         | Descripción                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Especifica el identificador de la clase de controlador.<br/>         |
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Tipo**](taskschedulerschema-datatype-complextype.md) | Especifica datos adicionales asociados al controlador.<br/> |



## <a name="remarks"></a>Observaciones

Las aplicaciones definen una acción del controlador COM mediante la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

### <a name="attributes"></a>Atributos

El atributo siguiente se define mediante el tipo complejo [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .

-   ID: identificador de la acción realizada por la tarea.

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define una acción de controlador COM.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





