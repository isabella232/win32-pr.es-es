---
description: Especifica la lista de redes LAN inalámbricas a las que se debe permitir la conexión de cualquier máquina.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: elemento allowList (networkFilter)
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
ms.openlocfilehash: 39eb56800b43bce0696bdfd8fe7dea2f6bbcb3c0b82fcffa39e3144af3c93620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800324"
---
# <a name="allowlist-networkfilter-element"></a>elemento allowList (networkFilter)

El elemento allowList (networkFilter) especifica la lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier máquina.

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

El **elemento allowList** se define mediante el [**elemento networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                     | Descripción                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**Red**](wlan-policyschema-network-allowlist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Red a la que se puede conectar la máquina.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 




