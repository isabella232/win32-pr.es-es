---
description: Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (Indicadores_globales) (LAN_policy)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815422"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (Indicadores_globales) (LAN_policy)

El elemento **enableAutoConfig** (indicadores_globales) especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (como 802.1 x).

Cuando **enableAutoConfig** tiene un valor de false, los equipos no deben usar el servicio de configuración automática integrado para administrar las conexiones que requieren la autenticación de nivel 2. En su lugar, la red especificada en el elemento [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) es la única red disponible para la conexión. El servicio de configuración automática solo responderá a las solicitudes para habilitar el servicio.

Cuando **enableAutoConfig** tiene un valor true, los equipos pueden usar el servicio de configuración automática integrado para conectarse a redes cableadas que requieran autenticación de nivel 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

El elemento **enableAutoConfig** se define mediante el elemento [**indicadores_globales**](lan-policyschema-globalflags-lanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Indicadores**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Indicadores_globales (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




