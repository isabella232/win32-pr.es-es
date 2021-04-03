---
description: Indica si está habilitado el modo estándar federal de procesamiento de información (FIPS).
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810376"
---
# <a name="fipsmode-authencryption-element"></a>Elemento FIPSMode (authEncryption)

El elemento **FIPSMode** (authEncryption) indica si está habilitado el modo estándar federal de procesamiento de información (FIPS). Cuando una conexión inalámbrica funciona en modo FIPS, el nivel de seguridad de la conexión cumple con el estándar FIPS 140-2. Para obtener más información acerca de FIPS, consulte la [Página principal de FIPS](https://www.itl.nist.gov/fipspubs/).

Este elemento es opcional. Si este elemento no se especifica en un perfil, no se habilita el modo FIPS.

**FIPSMode** solo se puede establecer en true cuando se cumplen las condiciones siguientes:

-   El elemento [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) tiene un valor de `ESS` (es decir, la conexión es una conexión de infraestructura).
-   El elemento [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) tiene un valor de `WPA2` o `WPA2PSK` .
-   El elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tiene un valor de `AES` .

A diferencia de la mayoría de los elementos del esquema de Perfil de WLAN \_ , este elemento se encuentra en el `https://www.microsoft.com/networking/WLAN/profile/v2` espacio de nombres.

El valor del elemento **FIPSMode** se omite si el controlador de minipuerto para la interfaz inalámbrica no es compatible con el modo FIPS.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite. Si **FIPSMode** está presente en un perfil, se omite el elemento.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter** Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el elemento **FIPSMode** , vea [ejemplo de Perfil de FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 
