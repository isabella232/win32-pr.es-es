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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245456"
---
# <a name="keytype-sharedkey-element"></a>Elemento keyType (sharedKey)

El elemento keyType (sharedKey) indica si la clave compartida será una clave de red o una frase de paso.

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

El elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) define el elemento .

## <a name="remarks"></a>Observaciones

Cuando el [**elemento de**](wlan-profileschema-encryption-authencryption-element.md) cifrado tiene un valor de WEP, **keyType** debe establecerse en **networkKey.**

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento keyType,** vea [Ejemplo](non-broadcast-profile-sample.md)de perfil que no es de difusión, Ejemplo de perfil [wpa-personal](wpa-personal-profile-sample.md)y Ejemplo de perfil [wpa2-personal](wpa2-personal-profile-sample.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




