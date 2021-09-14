---
title: Tipo complejo comHandlerType
description: Define los elementos secundarios y la información de secuenciación para el elemento ComHandler.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- Tipo complejo comHandlerType Programador de tareas
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071050"
---
# <a name="comhandlertype-complex-type"></a>Tipo complejo comHandlerType

Define los elementos secundarios y la información de secuenciación para el [**elemento ComHandler.**](taskschedulerschema-comhandler-actiongroup-element.md)

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                         | Descripción                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**Classid**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Especifica el identificador de la clase de controlador.<br/>          |
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datatype**](taskschedulerschema-datatype-complextype.md) | Especifica datos adicionales asociados al controlador. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





