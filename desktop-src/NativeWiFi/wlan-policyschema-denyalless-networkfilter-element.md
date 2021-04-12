---
description: Especifica si el acceso a todas las redes de infraestructura está bloqueado.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275325"
---
# <a name="denyalless-networkfilter-element"></a>Elemento denyAllESS (networkFilter)

El elemento denyAllESS (networkFilter) especifica si el acceso a todas las redes de infraestructura está bloqueado. Cuando **denyAllESS** tiene un valor true, las máquinas no se pueden conectar a una red de infraestructura; de lo contrario, las máquinas pueden conectarse a redes de infraestructura.

El valor predeterminado de este elemento es FALSE. Si **denyAllESS** no se especifica en un perfil, los equipos pueden conectarse a las redes de infraestructura de forma predeterminada.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

El elemento **denyAllESS** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 




