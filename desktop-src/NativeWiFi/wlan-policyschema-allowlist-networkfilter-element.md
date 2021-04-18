---
description: Especifica la lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Elemento permitidos (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686492"
---
# <a name="allowlist-networkfilter-element"></a>Elemento permitidos (networkFilter)

El elemento permitidos (networkFilter) especifica la lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **permitidos** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                     | Descripción                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**Storage**](wlan-policyschema-network-allowlist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | La red a la que se puede conectar la máquina.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




