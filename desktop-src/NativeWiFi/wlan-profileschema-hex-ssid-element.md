---
description: Contiene el SSID de una LAN inalámbrica en formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento Hex (SSID)
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
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686917"
---
# <a name="hex-ssid-element"></a>Elemento Hex (SSID)

El elemento Hex (SSID) contiene el SSID de una LAN inalámbrica en formato hexadecimal.

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

El elemento se define mediante el elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Observaciones

Aunque los elementos **Hex** y [**Name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Cuando la información de perfil se convierte en un SSID, el elemento **Hex** se convierte en el SSID (si existe) y se omite el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) . Si el elemento **Hex** no está presente, el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión de Unicode a ASCII.

Cuando se almacena un SSID en un perfil, siempre se genera el elemento **Hex** . El elemento [**Name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas. Es posible que se pierda parte de la información del SSID original cuando se convierte en un [**nombre**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el elemento **Hex** , vea [ejemplo de Perfil de FIPS](fips-profile-sample.md).

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




