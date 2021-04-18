---
description: Especifica el número de entradas en la caché de PMK en el cliente.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Elemento PMKCacheSize (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677334"
---
# <a name="pmkcachesize-security-element"></a>Elemento PMKCacheSize (Security)

El elemento PMKCacheSize (Security) especifica el número de entradas en la caché de PMK en el cliente. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado". Si **PMKCacheMode** está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.

El almacenamiento en caché PMK se describe en la especificación [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**bursátil**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




