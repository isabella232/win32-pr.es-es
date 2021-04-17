---
description: Indica si la clave compartida será una clave de red o una frase de contraseña.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento keyType (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677961"
---
# <a name="keytype-sharedkey-element"></a>Elemento keyType (sharedKey)

El elemento keyType (sharedKey) indica si la clave compartida será una clave de red o una frase de contraseña.

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Observaciones

Cuando el elemento de [**cifrado**](wlan-profileschema-encryption-authencryption-element.md) tiene un valor de WEP, **KeyType** debe establecerse en **networkKey**.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **KeyType** , vea ejemplo [de perfil sin difusión](non-broadcast-profile-sample.md), ejemplo de perfil [de WPA-Personal](wpa-personal-profile-sample.md)y [ejemplo de Perfil de WPA2-Personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




