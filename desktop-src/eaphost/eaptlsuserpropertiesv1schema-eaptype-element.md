---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187758"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Elemento EapType (eaptlsuserpropertiesv1schema)

El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo      | Descripción                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta. Si falta el elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) , EAP-TLS usa el nombre del certificado al que se hace referencia en el elemento [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Observaciones

El elemento **processContents** permite futuras mejoras en el esquema. El elemento **processContents** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





