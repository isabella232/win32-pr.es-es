---
description: Contiene la configuración de conectividad relacionada con IHV. No está implementado actualmente.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: elemento connectivity (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 393a07df451c0a9e79f74f369a84bed5310d5efc6eae2186fe8da4844d3bb806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797915"
---
# <a name="connectivity-ihv-element"></a>elemento connectivity (IHV)

El elemento connectivity (IHV) contiene la configuración de conectividad relacionada con IHV. No está implementado actualmente.

**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento se define mediante el [**elemento IHV.**](wlan-profileschema-ihv-wlanprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




