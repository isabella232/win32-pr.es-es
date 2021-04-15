---
title: Tipo complejo de timeTriggerType
description: Define el tipo base para el elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- tipo complejo de timeTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676622"
---
# <a name="timetriggertype-complex-type"></a>Tipo complejo de timeTriggerType

Define el tipo base para el elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                        | Tipo     | Descripción                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Especifica el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos). <br/> |



## <a name="remarks"></a>Observaciones

Tenga en cuenta que este elemento no agrega ningún elemento secundario a los definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





