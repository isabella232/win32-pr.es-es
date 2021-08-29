---
description: Indica el período de tiempo, en minutos, que se conservará una caché de PMK.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Elemento PMKCacheTTL (seguridad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0c4f43acfd64c3e6e575b1a41103c65feb2373f205354567aa8e1a023805ca72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799875"
---
# <a name="pmkcachettl-security-element"></a>Elemento PMKCacheTTL (seguridad)

El elemento PMKCacheTTL (seguridad) indica el tiempo, en minutos, que se conservará una caché de PMK. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled".

El almacenamiento en caché de PMK se describe en la [especificación 802.11i.](https://standards.ieee.org/findstds/standard/802.11i-2004.html)

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**elemento de**](wlan-profileschema-security-msm-element.md) seguridad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




