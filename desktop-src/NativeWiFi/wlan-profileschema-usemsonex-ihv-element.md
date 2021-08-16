---
description: Especifica el origen de la configuración de seguridad 802.1X utilizada por un componente de seguridad de IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: elemento useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4a62f2f25ef2a4a52fae82e2ce8ddb097a4b434d7c2f8f35a2783703a617ad8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912645"
---
# <a name="usemsonex-ihv-element"></a>elemento useMSOneX (IHV)

El **elemento useMSOneX** (IHV) especifica el origen de la configuración de seguridad 802.1X utilizada por un componente de seguridad de IHV.

Cuando **useMSOneX es** true, los componentes de seguridad de IHV usan la configuración 802.1X definida por Microsoft. Cuando **useMSOneX es** false, los componentes de seguridad de IHV usan la configuración 802.1X proporcionada por el proveedor.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

El elemento se define mediante el [**elemento IHV.**](wlan-profileschema-ihv-wlanprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




