---
description: Especifica un tipo de red.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684395"
---
# <a name="networktype-networkitemtype-element"></a>elemento networkType (networkItemType)

El elemento networkType (networkItemType) especifica un tipo de red. Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

El tipo complejo [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) define el elemento **networkType.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Posibles elementos primarios inmediatos en la instancia de esquema**
</dt> <dt>

[**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




