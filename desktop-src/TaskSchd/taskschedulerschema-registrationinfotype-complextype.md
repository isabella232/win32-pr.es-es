---
title: Tipo complejo de registrationInfoType
description: Define los elementos secundarios y la información de secuenciación para el elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- tipo complejo de registrationInfoType Programador de tareas
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996685"
---
# <a name="registrationinfotype-complex-type"></a>Tipo complejo de registrationInfoType

Define los elementos secundarios y la información de secuenciación para el elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                           | Tipo     | Descripción                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Autor**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Especifica el autor de la tarea.<br/>                                                                       |
| [**Posteriormente**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Especifica la fecha y hora en que se registra la tarea.<br/>                                                |
| [**Descripción**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Especifica la descripción de la tarea.<br/>                                                                  |
| [**Documentación**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Especifica cualquier documentación adicional para la tarea.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Especifica el descriptor de seguridad de la tarea.<br/>                                                          |
| [**Fuentes**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Especifica el origen desde el que se originó la tarea. Por ejemplo, de un componente, servicio, aplicación o usuario.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Especifica el URI de la tarea.<br/>                                                                          |
| [**Versión**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Especifica el número de versión de la tarea.<br/>                                                               |



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

 

 





