---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067185"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Elemento EapType (mspeapuserpropertiesv1schema)

El **elemento EapType** es un tipo derivado del [**elemento EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del [esquema baseeapuserpropertiesv1.](baseeapuserpropertiesv1schema-schema.md)

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                               | Tipo                                                                                      | Descripción                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | El [**elemento Eap**](baseeapuserpropertiesv1schema-eap-element.md) identifica el método interno y las credenciales que se usarán con ese método. Cuando se configura la configuración de PEAP para el acceso de invitado PEAP, este elemento no está presente.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | El [**elemento PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) permite futuras mejoras en el esquema. <br/> El [**elemento PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) es opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Mspeapuserpropertiesv1 Schema](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





