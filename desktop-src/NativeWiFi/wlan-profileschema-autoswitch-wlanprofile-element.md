---
description: Determina el comportamiento de itinerancia de una red conectada automáticamente cuando una red más preferida está dentro del alcance.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: AutoSwitch (WLANProfile) (elemento)
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
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908339"
---
# <a name="autoswitch-wlanprofile-element"></a>AutoSwitch (WLANProfile) (elemento)

El elemento AutoSwitch (WLANProfile) determina el comportamiento de itinerancia de una red conectada automáticamente cuando una red más preferida está dentro del alcance. . Este elemento es opcional.

Si AutoSwitch es "true" y [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", se debe intentar una conexión a una red preferida cada vez que una red más favorita entra en el intervalo. Una red más preferida es la que se ordena más arriba en la lista de redes inalámbricas preferidas. Este intento de conexión se produce cuando se conecta a otra red.

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", este valor puede ser "true" o "false".

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "manual", este valor debe establecerse en "false". Este elemento no tiene ningún efecto en una red conectada manualmente.

Un valor de AutoSwitch establecido en "true" da como resultado una mayor frecuencia de detección periódica de nuevas redes. Esto puede producir una mayor contaminación de la frecuencia de radio de estos exámenes periódicos y el mayor consumo de energía que usa el adaptador de red inalámbrica.

**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas. Estos cambios están diseñados para reducir la contaminación de la radiofrecuencia, el consumo de energía y la interrupción del tráfico en tiempo real a través de redes inalámbricas. La configuración predeterminada de **AutoSwitch** cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado. La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado. La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista. Se recomienda que el valor del elemento **AutoSwitch** que usa una aplicación en un perfil de LAN inalámbrica se establezca en "false" para reducir la frecuencia de detección periódica de nuevas redes, a menos que sea absolutamente necesario que una aplicación establezca este valor en "true".

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

El elemento **AutoSwitch** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **AutoSwitch** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 




