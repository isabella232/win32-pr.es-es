---
description: Especifica si las máquinas usan el servicio de configuración automática (AutoConfig) integrado para administrar conexiones inalámbricas.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN
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
ms.openlocfilehash: 77b09bf046cdbadb58c888a3084d14ed14794064bf9f11c110ccecaff105fceb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684416"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN 

El **elemento enableAutoConfig** (globalFlags) especifica si las máquinas usan el servicio de configuración automática integrado (AutoConfig) para administrar las conexiones inalámbricas. Cuando **enableAutoConfig tiene** el valor FALSE, las máquinas no deben usar AutoConfig para administrar conexiones inalámbricas y el servicio AutoConfig solo responde a las solicitudes para habilitar el servicio. Cuando **enableAutoConfig** tiene el valor TRUE, las máquinas pueden usar el servicio AutoConfig.

Este elemento es obligatorio. Cuando el servicio AutoConfig crea un perfil, este elemento tendrá el valor predeterminado TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

El **elemento enableAutoConfig** se define mediante el [**elemento globalFlags.**](wlan-policyschema-globalflags-wlanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




