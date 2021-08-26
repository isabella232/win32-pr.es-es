---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- EapType, elemento EAPHost
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
ms.openlocfilehash: fbc58ab640b7993d274abdb134de4648d51c495c07f70a4468460de1d920bd76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021635"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Elemento EapType (eaptlsuserpropertiesv1schema)

El **elemento EapType** es un tipo derivado del [**elemento EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del [esquema baseeapuserpropertiesv1.](baseeapuserpropertiesv1schema-schema.md)

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
| [**Nombre de usuario**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Captura el nombre de usuario que se va a enviar en EAP-Identity respuesta. Si el [**elemento Username**](eaptlsuserpropertiesv1schema-username-element.md) no está presente, EAP-TLS usa el nombre en el certificado al que se hace referencia en el [**elemento UserCert.**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md)<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Comentarios

El **elemento processContents** permite futuras mejoras en el esquema. El **elemento processContents** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





