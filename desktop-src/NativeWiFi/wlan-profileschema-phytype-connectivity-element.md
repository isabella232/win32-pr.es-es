---
description: Especifica el estándar de LAN inalámbrica 802,11 usado en una LAN inalámbrica.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (Connectivity)
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
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686694"
---
# <a name="phytype-connectivity-element"></a>Elemento phyType (Connectivity)

El elemento phyType (conectividad) especifica el estándar de LAN inalámbrica 802,11 usado en una LAN inalámbrica.

Puede especificar varios **phyType** s. Si no se especifica **phyType** , el perfil se puede usar para conectarse a cualquier **phyType**. El valor "n" solo se admite en Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

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

El elemento se define mediante el elemento de [**Conectividad**](wlan-profileschema-connectivity-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Conectividad**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Conectividad (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




