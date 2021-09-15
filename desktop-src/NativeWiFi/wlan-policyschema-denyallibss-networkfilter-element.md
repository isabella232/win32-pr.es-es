---
description: Especifica si se bloquea el acceso a todas las redes ad hoc.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473703"
---
# <a name="denyallibss-networkfilter-element"></a>elemento denyAllIBSS (networkFilter)

El elemento denyAllIBSS (networkFilter) especifica si se bloquea el acceso a todas las redes ad hoc. Cuando **denyAllIBSS tiene** el valor TRUE, las máquinas no se pueden conectar a una red ad hoc; De lo contrario, las máquinas pueden conectarse a redes ad hoc.

El valor predeterminado de este elemento es FALSE. Si **denyAllIBSS** no se especifica en un perfil, las máquinas pueden conectarse de forma predeterminada a redes ad hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

El **elemento denyAllIBSS** se define mediante el [**elemento networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

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

 

 




