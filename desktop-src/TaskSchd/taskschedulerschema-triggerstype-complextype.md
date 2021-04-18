---
title: Tipo complejo de triggersType
description: Define el grupo (triggerGroup) para todos los elementos del desencadenador.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- tipo complejo de triggersType Programador de tareas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686221"
---
# <a name="triggerstype-complex-type"></a>Tipo complejo de triggersType

Define el grupo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) para todos los elementos del desencadenador. El grupo [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene la lista de desencadenadores que se pueden usar en una tarea.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





