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
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619870"
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

 

 




