---
description: Especifica el origen de la configuración de seguridad 802.1X que usa un componente de seguridad de IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Elemento useMSOneX (IHV)
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
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074177"
---
# <a name="usemsonex-ihv-element"></a>Elemento useMSOneX (IHV)

El **elemento useMSOneX** (IHV) especifica el origen de la configuración de seguridad 802.1X que usa un componente de seguridad de IHV.

Cuando **useMSOneX es** true, los componentes de seguridad de IHV usan la configuración 802.1X definida por Microsoft. Cuando **useMSOneX es** false, los componentes de seguridad de IHV usan la configuración 802.1X proporcionada por el proveedor.

Windows XP con SP3 y la API de LAN inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

El elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) define el elemento .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




