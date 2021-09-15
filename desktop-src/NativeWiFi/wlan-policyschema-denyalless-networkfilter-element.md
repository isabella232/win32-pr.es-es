---
description: Especifica si se bloquea el acceso a todas las redes de infraestructura.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473704"
---
# <a name="denyalless-networkfilter-element"></a>elemento denyAllESS (networkFilter)

El elemento denyAllESS (networkFilter) especifica si se bloquea el acceso a todas las redes de infraestructura. Cuando **denyAllESS tiene** el valor TRUE, las máquinas no se pueden conectar a una red de infraestructura; De lo contrario, las máquinas pueden conectarse a redes de infraestructura.

El valor predeterminado de este elemento es FALSE. Si **denyAllESS** no se especifica en un perfil, las máquinas pueden conectarse de forma predeterminada a redes de infraestructura.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

El **elemento denyAllESS** se define mediante el [**elemento networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




