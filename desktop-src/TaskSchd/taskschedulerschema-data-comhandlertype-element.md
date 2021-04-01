---
title: Elemento Data (comHandlerType)
description: Especifica datos adicionales asociados al controlador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Programador de tareas de elementos de datos
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996846"
---
# <a name="data-comhandlertype-element"></a>Elemento Data (comHandlerType)

Especifica datos adicionales asociados al controlador.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

El elemento de **datos** se define mediante el tipo complejo de [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                             | Descripción                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Controlador**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica una acción que activa un controlador.<br/> |



## <a name="remarks"></a>Observaciones

Las aplicaciones definen los datos del controlador mediante la propiedad [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





