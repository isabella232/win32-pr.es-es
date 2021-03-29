---
description: Especifica el identificador del conjunto de servicios (SSID) de una red inalámbrica.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Elemento networkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912526"
---
# <a name="networkname-networkitemtype-element"></a>Elemento networkName (networkItemType)

El elemento networkName (networkItemType) especifica el identificador del conjunto de servicios (SSID) de una red inalámbrica.

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

El elemento **networkName** se define mediante el tipo complejo de [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

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

 

 




