---
title: Elemento Data (comHandlerType)
description: Especifica datos adicionales asociados al controlador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Datos de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071041"
---
# <a name="data-comhandlertype-element"></a>Elemento Data (comHandlerType)

Especifica datos adicionales asociados al controlador.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

El **elemento Data** se define mediante el tipo complejo [**comHandlerType.**](taskschedulerschema-comhandlertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                             | Descripción                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica una acción que llama a un controlador.<br/> |



## <a name="remarks"></a>Observaciones

Las aplicaciones definen los datos del controlador mediante [**la propiedad Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de la interfaz [**IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





