---
title: Elemento Connection (Connections)
description: Define cada valor de configuración y lo asocia a un nombre. El elemento Connection es opcional.
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
ms.openlocfilehash: 6948675f7910c46cb2b5db4285ce0df795fa057f275ce29b7f4c664b14c4ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498375"
---
# <a name="connection-connections-element"></a>Elemento Connection (Connections)

El **elemento Connection (Connections)** define cada valor de configuración y lo asocia a un nombre. El **elemento Connection** es opcional.

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

El **elemento Connection** se define mediante el elemento [**Connections.**](eapconnectionpropertiesv1schema-connections-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo   | Descripción                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifica el elemento de configuración de EAP.<br/>                                                                    |
| [**Nombre**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Captura el nombre de la conexión que se está definiendo, lo que ayuda a identificar varias conexiones. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

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

[esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





