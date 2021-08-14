---
title: registrationInfoType Complex Type
description: Define los elementos secundarios y la información de secuenciación para el elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- tipo complejo registrationInfoType Programador de tareas
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 704fcb3205f032654ef6a666dd119dec34f88992018f16b1715ba4982847149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131665"
---
# <a name="registrationinfotype-complex-type"></a>registrationInfoType Complex Type

Define los elementos secundarios y la información de secuenciación para el [**elemento RegistrationInfo.**](taskschedulerschema-registrationinfo-tasktype-element.md)

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
| [**Fecha**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Especifica la fecha y hora en que se registra la tarea.<br/>                                                |
| [**Descripción**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Especifica la descripción de la tarea.<br/>                                                                  |
| [**Documentación**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Especifica cualquier documentación adicional para la tarea.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Especifica el descriptor de seguridad de la tarea.<br/>                                                          |
| [**Fuente**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Especifica de dónde se originó la tarea. Por ejemplo, desde un componente, servicio, aplicación o usuario.<br/> |
| [**Identificador URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Especifica el URI de la tarea.<br/>                                                                          |
| [**Versión**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Especifica el número de versión de la tarea.<br/>                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





