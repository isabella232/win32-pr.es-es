---
description: Contiene el SSID de una LAN inalámbrica.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: elemento name (SSID)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161158"
---
# <a name="name-ssid-element"></a>elemento name (SSID)

El elemento name (SSID) contiene el SSID de una LAN inalámbrica.

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

El elemento se define mediante el [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

## <a name="remarks"></a>Observaciones

Los nombres distinguen mayúsculas de minúsculas.

Aunque los [**elementos hexadecimal**](wlan-profileschema-hex-ssid-element.md) y **name** son opcionales, al menos un **elemento hexadecimal** o **name** debe aparecer como elemento secundario del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

Cuando la información del perfil se convierte en un SSID, el elemento [**hexadecimal**](wlan-profileschema-hex-ssid-element.md)  se convierte al SSID (si está presente) y se omite el elemento name. Si el **elemento hexadecimal** no está presente, el **elemento name** se convierte en un SSID mediante la conversión unicode a ASCII.

Cuando se almacena un SSID en un perfil, siempre [**se genera**](wlan-profileschema-hex-ssid-element.md) el elemento hexadecimal. El **elemento name** solo se genera si la conversión ASCII a Unicode del SSID y la generación del perfil XML son correctas. Es posible que se pierda cierta información del SSID original cuando se convierte en un **nombre**.

**Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se muestran los caracteres de escape XML, como &, . Evite el uso de caracteres de escape XML en nombres SSID para perfiles implementados en Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento name,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




