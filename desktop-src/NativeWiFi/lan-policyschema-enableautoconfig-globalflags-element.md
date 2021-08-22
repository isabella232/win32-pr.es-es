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
ms.openlocfilehash: 2842da69b07136df80d15ea84553aecdf2c62d417c73f7ec85d9c315b819a397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780205"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

El **elemento enableAutoConfig** (globalFlags) especifica si las máquinas usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (como 802.1X).

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

 

 




