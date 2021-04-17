---
description: Especifica si el acceso a todas las redes ad hoc está bloqueado.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677341"
---
# <a name="denyallibss-networkfilter-element"></a>Elemento denyAllIBSS (networkFilter)

El elemento denyAllIBSS (networkFilter) especifica si se bloquea el acceso a todas las redes ad hoc. Cuando **denyAllIBSS** tiene un valor true, las máquinas no se pueden conectar a una red ad hoc; de lo contrario, es posible que los equipos se conecten a redes ad hoc.

El valor predeterminado de este elemento es FALSE. Si **denyAllIBSS** no se especifica en un perfil, los equipos pueden conectarse a las redes ad hoc de forma predeterminada.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

El elemento **denyAllIBSS** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

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

 

 




