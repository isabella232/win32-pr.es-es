---
description: Define la lista de redes permitidas y denegadas para las máquinas.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161175"
---
# <a name="networkfilter-wlanpolicy-element"></a>Elemento networkFilter (WLANPolicy)

El elemento networkFilter (WLANPolicy) define la lista de redes permitidas y denegadas para las máquinas.

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

El **elemento networkFilter** se define mediante el [**elemento WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                    | Tipo                                                                     | Descripción                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | Lista de redes LAN inalámbricas a las que se debe permitir la conexión de cualquier máquina. <br/> |
| [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | Lista de redes LAN inalámbricas a las que una máquina no debe conectarse.<br/>              |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)   | boolean                                                                  | Especifica si se bloquea el acceso a todas las redes de infraestructura. <br/>                     |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md) | boolean                                                                  | Especifica si se bloquea el acceso a todas las redes ad hoc. <br/>                             |
| [**Red**](wlan-policyschema-network-allowlist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Una red permitida. <br/>                                                                |
| [**Red**](wlan-policyschema-network-blocklist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Una red bloqueada. <br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




