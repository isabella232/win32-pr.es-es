---
description: Contiene el SSID de una LAN inalámbrica en formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento hexadecimal (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 666562f7a476505dbb0ff23d5354e0f073505d9dd5195bcae17543294cc5f176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799895"
---
# <a name="hex-ssid-element"></a>Elemento hexadecimal (SSID)

El elemento hexadecimal (SSID) contiene el SSID de una LAN inalámbrica en formato hexadecimal.

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

## <a name="remarks"></a>Comentarios

Aunque los **elementos hexadecimal** y [**name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un **elemento hexadecimal** o [**name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

Cuando la información del perfil se convierte en un SSID, el elemento **hexadecimal** se convierte en el SSID (si está presente) y el elemento [**name**](wlan-profileschema-name-ssid-element.md) se omite. Si el **elemento hexadecimal** no está presente, el [**elemento name**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión unicode a ASCII.

Cuando se almacena un SSID en un perfil, siempre **se genera** el elemento hexadecimal. El [**elemento name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión ASCII a Unicode del SSID y la generación del perfil XML son correctas. Es posible que se pierda cierta información del SSID original cuando se convierte en un [**nombre**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el **elemento hexadecimal,** vea [Ejemplo de perfil de FIPS](fips-profile-sample.md).

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

[**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




