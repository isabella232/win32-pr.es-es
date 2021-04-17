---
title: Connection (conexiones) (elemento)
description: Define cada valor de configuración y lo asocia a un nombre. El elemento de conexión es opcional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento de conexión EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714599"
---
# <a name="connection-connections-element"></a>Connection (conexiones) (elemento)

El elemento de **conexión (conexiones)** define cada opción de configuración y la asocia a un nombre. El elemento de **conexión** es opcional.

``` syntax
<xs:element name="Connection">
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
```

El elemento de **conexión** se define mediante [**el elemento**](eapconnectionpropertiesv1schema-connections-element.md) Connections.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo   | Descripción                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Participante**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifica el elemento de configuración de EAP.<br/>                                                                    |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Captura el nombre de la conexión que se está definiendo y ayuda en la identificación de varias conexiones. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Conexiones**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Conexiones**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





