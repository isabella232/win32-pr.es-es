---
description: Especifica el estándar laN inalámbrica 802.11 que se usa en una LAN inalámbrica.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684025"
---
# <a name="phytype-connectivity-element"></a>Elemento phyType (connectivity)

El elemento phyType (connectivity) especifica el estándar laN inalámbrica 802.11 que se usa en una LAN inalámbrica.

Puede especificar varios **phyType** s. Si no **se especifica ningún phyType,** el perfil se puede usar para conectarse a cualquier **phyType**. El valor "n" solo se admite en Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**elemento de**](wlan-profileschema-connectivity-msm-element.md) conectividad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Conectividad**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**conectividad (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




