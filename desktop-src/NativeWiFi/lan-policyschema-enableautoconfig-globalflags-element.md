---
description: Especifica si las máquinas usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (globalFlags) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071590"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

El **elemento enableAutoConfig** (globalFlags) especifica si las máquinas usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1X).

Cuando **enableAutoConfig tiene** el valor FALSE, las máquinas no deben usar el servicio de configuración automática integrado para administrar las conexiones que requieren autenticación de nivel 2. En su lugar, la red especificada en el [**elemento profileList**](lan-policyschema-profilelist-lanpolicy-element.md) es la única red disponible para la conexión. El servicio de configuración automática solo responderá a las solicitudes para habilitar el servicio.

Cuando **enableAutoConfig tiene** el valor TRUE, las máquinas pueden usar el servicio de configuración automática integrado para conectarse a redes cableadas que requieren autenticación de nivel 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

El **elemento enableAutoConfig** se define mediante el [**elemento globalFlags.**](lan-policyschema-globalflags-lanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




