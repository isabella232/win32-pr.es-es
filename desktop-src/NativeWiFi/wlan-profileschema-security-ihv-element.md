---
description: Contiene varias configuraciones de seguridad utilizadas por proveedores de hardware independientes.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: security (IHV) (Elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e4baeadc5e53dc53d0a526b62c4905da1a778a1015f58321ae8b96e4aa52dfcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912755"
---
# <a name="security-ihv-element"></a>security (IHV) (Elemento)

El elemento de seguridad (IHV) contiene varias configuraciones de seguridad utilizadas por proveedores de hardware independientes.

La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes. Si ambos conjuntos de configuración de seguridad están presentes en el mismo perfil, el perfil no es válido.

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="security">
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

El **elemento** de seguridad se define mediante el [**elemento IHV.**](wlan-profileschema-ihv-wlanprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




