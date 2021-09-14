---
description: Indica si el modo de estándar federal de procesamiento de información (FIPS) está habilitado.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245517"
---
# <a name="fipsmode-authencryption-element"></a>Elemento FIPSMode (authEncryption)

El **elemento FIPSMode** (authEncryption) indica si el modo fips (Estándar federal de procesamiento de información) está habilitado. Cuando una conexión inalámbrica funciona en modo FIPS, el nivel de seguridad de la conexión cumple con el estándar FIPS 140-2. Para obtener más información sobre FIPS, vea la [página principal de FIPS](https://www.itl.nist.gov/fipspubs/).

Este elemento es opcional. Si este elemento no se especifica en un perfil, el modo FIPS no está habilitado.

**FIPSMode solo** se puede establecer en TRUE cuando se cumplen las condiciones siguientes:

-   El [**elemento connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) tiene un valor `ESS` de (es decir, la conexión es una conexión de infraestructura).
-   El [**elemento**](wlan-profileschema-authentication-authencryption-element.md) de autenticación tiene un valor `WPA2` de o `WPA2PSK` .
-   El [**elemento**](wlan-profileschema-encryption-authencryption-element.md) de cifrado tiene un valor de `AES` .

A diferencia de la mayoría de los elementos del esquema \_ de perfil WLAN, este elemento está en el espacio de `https://www.microsoft.com/networking/WLAN/profile/v2` nombres .

El valor del elemento **FIPSMode** se omite si el controlador de minipuerto para la interfaz inalámbrica no admite el modo FIPS.

**Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento. Si **FIPSMode** está presente en un perfil, se omite el elemento .

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

El elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) define el elemento .

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el **comando netsh wlan set profileparameter.** Para obtener más información, [vea Netsh Commands for Wireless Local Area Network (wlan) (Comandos de Netsh para redes inalámbricas de área local [wlan]).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el **elemento FIPSMode,** vea [Ejemplo de perfil de FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**authEncryption (seguridad)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
