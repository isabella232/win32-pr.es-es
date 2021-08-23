---
description: Especifica el número de intentos previos a la autenticación para probar en los AP vecinos.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: preAuthThrottle (security) (Elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8bc310d19126a0e4bc9a7e6abf2a6ae1d0eb917cb5f425796d10bee66ea6ebed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064605"
---
# <a name="preauththrottle-security-element"></a>preAuthThrottle (security) (Elemento)

El elemento preAuthThrottle (seguridad) especifica el número de intentos de autenticación previa para probar en los AP vecinos. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled". Si **PMKCacheMode** está habilitado y este elemento no está presente, el número de intentos tiene como valor predeterminado 3.

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento de seguridad define [**el**](wlan-profileschema-security-msm-element.md) elemento .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




