---
title: Tipo complejo de sendEmailType
description: Define el tipo de acción que se usa para especificar que se enviará un correo electrónico cuando se ejecute una tarea. Este tipo define todos los elementos que se usan para modelar el mensaje de correo electrónico.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- tipo complejo de sendEmailType Programador de tareas
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676994"
---
# <a name="sendemailtype-complex-type"></a>Tipo complejo de sendEmailType

Define el tipo de acción que se usa para especificar que se enviará un correo electrónico cuando se ejecute una tarea. Este tipo define todos los elementos que se usan para modelar el mensaje de correo electrónico.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                        | Tipo                                                                         | Descripción                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Datos adjuntos**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Especifica una lista de datos adjuntos en el mensaje de correo electrónico.<br/>                                 |
| [**CCO**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Especifica las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.<br/>               |
| [**Cuerpo**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Especifica el texto en el cuerpo del mensaje de correo electrónico.<br/>                                  |
| [**Correos**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Especifica las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.<br/>                |
| [**From**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Especifica la dirección de correo electrónico del remitente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Especifica las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Especifica el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico. <br/>                           |
| [**Asunto**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Especifica el asunto del mensaje de correo electrónico.<br/>                                           |
| [**En**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Especifica las direcciones de correo electrónico a las que se enviará el correo electrónico.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





