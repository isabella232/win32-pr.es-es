---
description: Especifica la lista de redes LAN inalámbricas a las que una máquina no debe conectarse.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Elemento blockList (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c5bd795ee9f5fc21dc205c24306820b4dec7f074638aa0e4f11ba3acde68cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684425"
---
# <a name="blocklist-networkfilter-element"></a>Elemento blockList (networkFilter)

El elemento blockList (networkFilter) especifica la lista de redes LAN inalámbricas a las que una máquina no debe conectarse.

``` syntax
<xs:element name="blockList">
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

El **elemento blockList** se define mediante el [**elemento networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                     | Descripción                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**Red**](wlan-policyschema-network-blocklist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Red bloqueada. <br/> |



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

 

 




