---
description: Determina el comportamiento de itinerancia de una red conectada automáticamente cuando hay una red más preferida en el intervalo.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Elemento autoSwitch (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a656667a8c32d4b21793cfc605654f1c80c31ce1d69fd274a7be81078f6cc2c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799935"
---
# <a name="autoswitch-wlanprofile-element"></a>Elemento autoSwitch (WLANProfile)

El elemento autoSwitch (WLANProfile) determina el comportamiento de itinerancia de una red conectada automáticamente cuando hay una red preferida en el intervalo. . Este elemento es opcional.

Si autoSwitch es "true" y [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", se debe intentar una conexión a una red más preferida siempre que una red más preferida entre en el intervalo. Una red preferida es aquella que se ordena más arriba en la lista de redes inalámbricas preferidas. Este intento de conexión se produce cuando se conecta a otra red.

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", este valor puede ser "true" o "false".

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "manual", este valor debe establecerse en "false". Este elemento no tiene ningún efecto en una red conectada manualmente.

Un valor de autoSwitch establecido en "true" da como resultado una mayor frecuencia de examen periódico de nuevas redes. Esto puede provocar una mayor frecuencia de radiofrecuencia de estos exámenes periódicos y un mayor consumo de energía que usa el adaptador de red inalámbrica.

**Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas. Estos cambios están diseñados para reducir la frecuencia de radiofrecuencia, el consumo de energía y la interrupción del tráfico en tiempo real a través de redes inalámbricas. La configuración predeterminada de **autoSwitch** cuando este elemento no está establecido en un perfil de LAN inalámbrica ha cambiado. La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio laN inalámbrica instalado. El valor predeterminado era "true" en Windows Server 2008 y Windows Vista. Se recomienda establecer el valor del elemento **autoSwitch** usado por una aplicación en un perfil de LAN inalámbrica en "false" para reducir la frecuencia de examen periódico de nuevas redes, a menos que sea absolutamente necesario que una aplicación establezca este valor en "true".

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

El **elemento autoSwitch** se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento autoSwitch,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




