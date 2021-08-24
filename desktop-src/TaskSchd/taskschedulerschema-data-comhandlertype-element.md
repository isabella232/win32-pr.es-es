---
title: Elemento Data (comHandlerType)
description: Especifica datos adicionales asociados al controlador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Elemento data Programador de tareas
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 649cadf0fc10919902e65ce82df1b410708d74a9db8dd3638c6fb22753aa557a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334595"
---
# <a name="data-comhandlertype-element"></a>Elemento Data (comHandlerType)

Especifica datos adicionales asociados al controlador.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

El **tipo** complejo [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) define el elemento Data.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                             | Descripción                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica una acción que llama a un controlador.<br/> |



## <a name="remarks"></a>Comentarios

Las aplicaciones definen los datos del controlador mediante [**la propiedad Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de la interfaz [**IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





