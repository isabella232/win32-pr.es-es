---
description: Indica el modo de funcionamiento de la red.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Elemento connectionType (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 01eec035fdd42504e3c3da0baec537b096d42c63deb7c336d8446bc7a0d95572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799905"
---
# <a name="connectiontype-wlanprofile-element"></a>Elemento connectionType (WLANProfile)

El elemento connectionType (WLANProfile) indica el modo de funcionamiento de la red.

Un valor de **ESS** indica una red de infraestructura, mientras **que IBSS** indica una red ad hoc.

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento connectionType** se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento connectionType,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




