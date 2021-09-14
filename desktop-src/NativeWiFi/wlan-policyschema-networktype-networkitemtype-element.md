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
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161171"
---
# <a name="networktype-networkitemtype-element"></a>elemento networkType (networkItemType)

El elemento networkType (networkItemType) especifica un tipo de red. Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

El **elemento networkType** se define mediante el [**tipo complejo networkItemType.**](wlan-policyschema-networkitemtype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

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

 

 




