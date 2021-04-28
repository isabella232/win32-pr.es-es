---
description: 'Elemento profileList (WLANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento profileList (WLANPolicy)
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
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109203"
---
# <a name="profilelist-wlanpolicy-element"></a>Elemento profileList (WLANPolicy)

El elemento profileList (WLANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo. Este elemento es opcional. Si este elemento está presente, debe contener al menos un perfil.

Los perfiles deben basarse en el esquema [de \_ perfil WLAN](wlan-profileschema-schema.md), con un elemento raíz [**de WLANProfile**](wlan-profileschema-wlanprofile-element.md).

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 




