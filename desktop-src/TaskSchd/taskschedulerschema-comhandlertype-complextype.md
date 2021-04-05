---
title: Tipo complejo de comHandlerType
description: Define los elementos secundarios y la información de secuenciación para el elemento comhandler.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- tipo complejo de comHandlerType Programador de tareas
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079160"
---
# <a name="comhandlertype-complex-type"></a>Tipo complejo de comHandlerType

Define los elementos secundarios y la información de secuenciación para el elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) .

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
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Especifica el identificador de la clase de controlador.<br/>          |
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Tipo**](taskschedulerschema-datatype-complextype.md) | Especifica datos adicionales asociados al controlador. <br/> |



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

 

 





