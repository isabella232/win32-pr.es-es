---
description: Indica si se va a conectar a una red oculta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonbroadcast (SSIDConfig)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677535"
---
# <a name="nonbroadcast-ssidconfig-element"></a>Elemento nonbroadcast (SSIDConfig)

El elemento nonbroadcast (SSIDConfig) indica si se va a conectar a una red oculta. Si una red no emite su SSID, se denomina red oculta. Si se establecen varios SSID en el perfil, todos deben tener el mismo valor de no difusión.

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **ESS**, este valor puede ser "true" o "false". Si este elemento no está presente, el valor predeterminado es "false".

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **IBSS**, este valor debe ser "false". Si este elemento no está presente, el valor predeterminado es "false".

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

El elemento se define mediante el elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="examples"></a>Ejemplos

Para ver un perfil de ejemplo que usa el elemento de no **difusión** , vea [ejemplo de perfil sin difusión](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




