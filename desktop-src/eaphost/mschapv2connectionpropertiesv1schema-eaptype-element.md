---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: Es un tipo derivado del elemento EapType del esquema baseeapconnectionpropertiesv1. Este es el elemento superior que aparece dentro del elemento Config del esquema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 18d3296dfab4a28ba818199d0b9329888c692f55831bced2af5abedfd1f205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984065"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Elemento EapType (mschapv2connectionpropertiesv1schema)

El **elemento EapType** es un tipo derivado del elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) del [esquema baseeapconnectionpropertiesv1.](baseeapconnectionpropertiesv1schema-schema.md) Este es el elemento superior que aparece dentro del elemento Config del [esquema EapHostConfig.](eaphostconfigschema-elements.md)

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
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



| Elemento                                                                                                       | Tipo    | Descripción                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | Controla el uso de las credenciales de winlogin. Si es TRUE, eap MS-CHAPv2 obtener las credenciales de winlogon. Si es FALSE, eap MS-CHAPv2 obtener las credenciales del usuario. <br/> El [**elemento UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) es opcional.<br/> |



## <a name="remarks"></a>Comentarios

El **elemento processContents** permite futuras mejoras en el esquema. El **elemento processContents** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





