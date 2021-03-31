---
description: Contiene el SSID de una LAN inalámbrica.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: nombre (SSID) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911897"
---
# <a name="name-ssid-element"></a>nombre (SSID) (elemento)

El elemento Name (SSID) contiene el SSID de una LAN inalámbrica.

``` syntax
<xs:element name="name">
    <xs:simpleType>
        <xs:restriction
            base="string"
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

Los nombres distinguen mayúsculas de minúsculas.

Aunque los elementos [**Hex**](wlan-profileschema-hex-ssid-element.md) y **Name** son opcionales, al menos un elemento **Hex** o **Name** debe aparecer como elemento secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Cuando la información de perfil se convierte en un SSID, el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) se convierte en el SSID (si existe) y se omite el elemento de **nombre** . Si el elemento **Hex** no está presente, el elemento de **nombre** se convierte en un SSID mediante la conversión de Unicode a ASCII.

Cuando se almacena un SSID en un perfil, siempre se genera el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) . El elemento **Name** solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas. Es posible que se pierda parte de la información del SSID original cuando se convierte en un **nombre**.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** No se muestran los caracteres de escape XML, como &. Evite usar caracteres de escape XML en nombres SSID para perfiles implementados en Windows XP con SP3 y API LAN inalámbrica para Windows XP con SP2.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **Name** , vea [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

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

 

 




