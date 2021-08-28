---
description: Contiene varias configuraciones de conectividad.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: elemento connectivity (MSM)
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
ms.openlocfilehash: 8745671004799f96aecfe68b531c122c76122b5865678258fd241e9d8a07260a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799915"
---
# <a name="connectivity-msm-element"></a>elemento connectivity (MSM)

El elemento connectivity (MSM) contiene varias configuraciones de conectividad.

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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

El elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) define el elemento .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                            | Tipo |
|--------------------------------------------------------------------|------|
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento de conectividad,** vea [Ejemplos de perfil inalámbrico](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Msm**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




