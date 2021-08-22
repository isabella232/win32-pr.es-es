---
description: Indica si se usará el almacenamiento en caché de PMK.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (seguridad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 23e32d7a658e41f80eb2a4d8d743afc2c96f7a5a1b4135e646374b98e6acac26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619261"
---
# <a name="pmkcachemode-security-element"></a>Elemento PMKCacheMode (seguridad)

El elemento PMKCacheMode (seguridad) indica si se usará el almacenamiento en caché de PMK. Este elemento solo es válido para redes definidas por WPA2. El almacenamiento en caché de PMK se describe en la [especificación 802.11i.](https://standards.ieee.org/findstds/standard/802.11i-2004.html)

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento de seguridad define [**el**](wlan-profileschema-security-msm-element.md) elemento .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




