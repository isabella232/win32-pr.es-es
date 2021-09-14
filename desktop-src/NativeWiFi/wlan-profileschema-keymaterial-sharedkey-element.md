---
description: Contiene una clave de red o frase de contraseña.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento keyMaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245462"
---
# <a name="keymaterial-sharedkey-element"></a>Elemento keyMaterial (sharedKey)

El elemento keyMaterial (sharedKey) contiene una clave de red o frase de contraseña. Si el [**elemento**](wlan-profileschema-protected-sharedkey-element.md) protegido tiene el valor TRUE, se cifra este material de clave; De lo contrario, el material de clave no está cifrado. El material de clave cifrado se expresa en formato hexadecimal.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

El elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) define el elemento .

## <a name="remarks"></a>Observaciones

El intervalo de valores válidos para el elemento keyMaterial varía según el tipo de autenticación y cifrado usados, según lo especificado por los elementos [**de**](wlan-profileschema-authentication-authencryption-element.md) autenticación [**y cifrado.**](wlan-profileschema-encryption-authencryption-element.md) También varía según [**keyType.**](wlan-profileschema-keytype-sharedkey-element.md)

En la tabla siguiente se muestran los **valores válidos de keyMaterial** para algunos pares de autenticación y cifrado.



| [**valor de autenticación**](wlan-profileschema-authentication-authencryption-element.md) | [**valor de**](wlan-profileschema-encryption-authencryption-element.md) cifrado | [**valor keyType**](wlan-profileschema-keytype-sharedkey-element.md) | Valores **válidos de keyMaterial**                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abrir o compartir                                                                           | WEP                                                                              | networkKey                                                            | Este elemento contiene una clave WEP de 5 o 13 caracteres ANSI, o de 10 o 26 caracteres hexadecimales.                                                                                             |
| WPAPSK o WPA2PSK                                                                        | TKIP o AES                                                                      | passPhrase                                                            | Este elemento contiene una frase de contraseña de 8 a 63 caracteres ASCII, es decir, de 8 a 63 caracteres ANSI en el intervalo de 32 a 126. Los valores de clave deben cumplir los requisitos especificados por 802.11i. |
| WPAPSK o WPA2PSK                                                                        | TKIP o AES                                                                      | networkKey                                                            | Este elemento contiene una clave de 64 caracteres hexadecimales.                                                                                                                                      |



 

Se pueden especificar caracteres Unicode donde se especifican caracteres ANSI o ASCII anteriormente. Sin embargo, si los caracteres Unicode proporcionados no se pueden asignar a caracteres ANSI o ASCII, se rechaza el material de clave proporcionado.

El material de clave devuelto [**por WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) siempre se cifra. Además, si se pasa material de clave sin cifrar a [**WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)el material de clave se cifra automáticamente antes de almacenarse en el almacén de perfiles.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** El material de clave nunca se cifra.

Si el proceso se ejecuta en el contexto de la cuenta LocalSystem, puede descifrar el material de clave mediante una llamada [**a CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo que usan el elemento **keyMaterial,** vea [Ejemplo](non-broadcast-profile-sample.md)de perfil no de difusión, Ejemplo de perfil [wpa-personal](wpa-personal-profile-sample.md)y [Ejemplo de perfil wpa2-personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
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

 

 
