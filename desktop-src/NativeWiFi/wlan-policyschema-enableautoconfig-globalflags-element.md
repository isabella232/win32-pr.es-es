---
description: Especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
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
ms.openlocfilehash: c03e4c2afa9e8e98c07e1bc0cdec4099d3260aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541038"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (Indicadores_globales) (LAN_policy)

El elemento **enableAutoConfig** (indicadores_globales) especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas. Cuando **enableAutoConfig** tiene un valor de false, los equipos no deben usar AutoConfig para administrar las conexiones inalámbricas y el servicio de configuración automática solo responde a las solicitudes para habilitar el servicio. Cuando **enableAutoConfig** tiene un valor de true, los equipos pueden usar el servicio de configuración automática.

Este elemento es obligatorio. Cuando el servicio de configuración automática crea un perfil, este elemento tendrá el valor predeterminado TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

El elemento **enableAutoConfig** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Indicadores**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Indicadores_globales (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




