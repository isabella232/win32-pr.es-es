---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187838"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Elemento EapType (mspeapuserpropertiesv1schema)

El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

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
| [**Participante**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | El elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica el método interno y las credenciales que se van a utilizar con ese método. Cuando la configuración de PEAP está configurada para el acceso de invitado de PEAP, este elemento no está presente.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | El elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) permite futuras mejoras en el esquema. <br/> El elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) es opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





