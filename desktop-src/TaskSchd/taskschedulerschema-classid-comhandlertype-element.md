---
title: Elemento ClassId (comHandlerType)
description: Especifica el identificador de la clase de controlador.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- Elemento ClassId Programador de tareas
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2729226320758f93140e1d4073286fba02f446d34f9eb9c36caf931b7190e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402125"
---
# <a name="classid-comhandlertype-element"></a>Elemento ClassId (comHandlerType)

Especifica el identificador de la clase de controlador.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

El tipo complejo [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) define el elemento **ClassId.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                             | Descripción                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica una acción que llama a un controlador.<br/> |



## <a name="remarks"></a>Comentarios

Las aplicaciones definen el identificador de clase mediante la [**propiedad ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) de la [**interfaz IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





