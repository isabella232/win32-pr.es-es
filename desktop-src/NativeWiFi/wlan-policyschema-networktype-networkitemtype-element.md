---
description: Especifica un tipo de red.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678308"
---
# <a name="networktype-networkitemtype-element"></a>Elemento networkType (networkItemType)

El elemento networkType (networkItemType) especifica un tipo de red. Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

El elemento **NetworkType** se define mediante el tipo complejo de [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Posibles elementos primarios inmediatos en la instancia de esquema**
</dt> <dt>

[**red (permitidos)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**red (bloqueo de listas)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




