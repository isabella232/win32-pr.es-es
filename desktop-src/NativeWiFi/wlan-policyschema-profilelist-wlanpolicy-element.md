---
description: 'Elemento profileList (WLANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: elemento profileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161169"
---
# <a name="profilelist-wlanpolicy-element"></a>elemento profileList (WLANPolicy)

El elemento profileList (WLANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo. Este elemento es opcional. Si este elemento está presente, debe contener al menos un perfil.

Los perfiles deben basarse en el esquema [ \_ de perfil WLAN](wlan-profileschema-schema.md), con un elemento raíz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El **elemento profileList** se define mediante el [**elemento WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)

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

 

 




