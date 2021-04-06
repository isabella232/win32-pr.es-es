---
description: Especifica el origen de la configuración de seguridad de 802.1 X usada por un componente de seguridad IHV.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002188"
---
# <a name="usemsonex-ihv-element"></a>Elemento useMSOneX (IHV)

El elemento **useMSOneX** (IHV) especifica el origen de la configuración de seguridad de 802.1 x usada por un componente de seguridad IHV.

Cuando **useMSOneX** es true, los componentes de seguridad de IHV usan la configuración de 802.1 x definida por Microsoft. Cuando **useMSOneX** es false, los componentes de seguridad de IHV usan la configuración de 802.1 x suministrada por el proveedor.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

El elemento está definido por el elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




