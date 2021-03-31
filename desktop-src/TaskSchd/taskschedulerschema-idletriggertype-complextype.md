---
title: Tipo complejo de idleTriggerType
description: Define el tipo base para el elemento IdleTrigger.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- tipo complejo de idleTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97868d5b13f224bc55661b681246be29f3a4a20b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801484"
---
# <a name="idletriggertype-complex-type"></a>Tipo complejo de idleTriggerType

Define el tipo base para el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos complejos de esquema Programador de tareas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





