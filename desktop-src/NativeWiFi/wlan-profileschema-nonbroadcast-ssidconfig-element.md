---
description: Indica si se debe conectar a una red oculta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: nonBroadcast (SSIDConfig) (Elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272244"
---
# <a name="nonbroadcast-ssidconfig-element"></a>nonBroadcast (SSIDConfig) (Elemento)

El elemento nonBroadcast (SSIDConfig) indica si se debe conectar a una red oculta. Si una red no difunde su SSID, se conoce como una red oculta. Si se establecen varios SSID dentro del perfil, todos deben tener el mismo valor nonBroadcast.

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **ESS,** este valor puede ser "true" o "false". Si este elemento no está presente, el valor predeterminado es "false".

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **IBSS,** este valor debe ser "false". Si este elemento no está presente, el valor predeterminado es "false".

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

El elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) define el elemento .

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el **elemento nonBroadcast,** vea [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




