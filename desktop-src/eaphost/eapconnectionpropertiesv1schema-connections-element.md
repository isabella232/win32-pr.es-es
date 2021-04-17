---
title: Elemento Connections
description: Obtenga información sobre el elemento Connections. Este elemento recopila y contiene cero o más elementos de conexión.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
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
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714450"
---
# <a name="connections-element"></a>Elemento Connections

El elemento **Connections** recopila y contiene cero o más elementos de [**conexión**](eapconnectionpropertiesv1schema-connection-connections-element.md) .

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
| [**Participante**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifica el elemento de configuración de EAP.<br/>                                                                                                                                       |
| [**Conectarse**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Define cada valor de configuración y lo asocia a un nombre. El elemento de [**conexión**](eapconnectionpropertiesv1schema-connection-connections-element.md) es opcional.<br/> |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Captura el nombre de la conexión que se está definiendo y ayuda en la identificación de varias conexiones.<br/>                                                                     |



## <a name="remarks"></a>Observaciones

El elemento **Connections** no se utiliza con métodos heredados a través de las API de EAPHost.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





