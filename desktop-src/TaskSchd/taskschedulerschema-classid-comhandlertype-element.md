---
title: ClassId (comHandlerType), elemento
description: Especifica el identificador de la clase de controlador.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassId (Programador de tareas del elemento)
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493132"
---
# <a name="classid-comhandlertype-element"></a>ClassId (comHandlerType), elemento

Especifica el identificador de la clase de controlador.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

El elemento **ClassID** se define mediante el tipo complejo [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                             | Descripción                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Controlador**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica una acción que activa un controlador.<br/> |



## <a name="remarks"></a>Observaciones

Las aplicaciones definen el identificador de clase mediante la propiedad [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) de la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





