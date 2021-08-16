---
title: Elemento Connections
description: Obtenga información sobre el elemento Connections. Este elemento recopila y contiene cero o más elementos Connection.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento CONNECTIONS EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62635d09030875a4f17deefa1aec05432df5662369eb483894f1a8cef4bbaf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498223"
---
# <a name="connections-element"></a>Elemento Connections

El **elemento Connections** recopila y contiene cero o más elementos [**Connection.**](eapconnectionpropertiesv1schema-connection-connections-element.md)

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Name"
                            type="string"
                         />
                        <xs:element
                            maxOccurs="unbounded"
                            ref="Eap"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                              | Tipo   | Descripción                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifica el elemento de configuración de EAP.<br/>                                                                                                                                       |
| [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Define cada valor de configuración y lo asocia a un nombre. El [**elemento Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) es opcional.<br/> |
| [**Nombre**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Captura el nombre de la conexión que se está definiendo, lo que ayuda a identificar varias conexiones.<br/>                                                                     |



## <a name="remarks"></a>Comentarios

El **elemento Connections** no se usa con métodos heredados a través de las API de EAPHost.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





