---
title: weeksType Complex Type
description: Define el elemento secundario y la información de secuenciación para el elemento Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- Tipo complejo weeksType Programador de tareas
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876d798acdf1f8684fc4f2cecac8e77bceb73dddd0036f2117d4bb55a77a71ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757992"
---
# <a name="weekstype-complex-type"></a>weeksType Complex Type

Define el elemento secundario y la información de secuenciación para el [**elemento Week.**](taskschedulerschema-week-weekstype-element.md)

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                    | Tipo                                                        | Descripción                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Semana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Especifica la semana en la que se ejecuta la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





