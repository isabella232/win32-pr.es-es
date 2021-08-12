---
title: triggersType Complex Type
description: Define el grupo (triggerGroup) para todos los elementos de desencadenador.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- triggersType tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610542"
---
# <a name="triggerstype-complex-type"></a>triggersType Complex Type

Define el grupo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) para todos los elementos de desencadenador. El [**grupo triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene la lista de desencadenadores que se pueden usar en una tarea.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





