---
description: Especifica el identificador de proveedor de la red de telefonía móvil.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Elemento ProviderID (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: b40ac5abab2abf850d927c21f0de66ad419987f594f28dffcd380ead7f982d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959795"
---
# <a name="providerid-providertype-element"></a>Elemento ProviderID (providerType)

El **elemento ProviderID (providerType)** especifica el identificador de proveedor de la red de telefonía móvil.

El elemento es una secuencia de dígitos con un máximo de 6 dígitos.

Este elemento es necesario dentro del [**elemento Provider.**](schema-provider-dataroamingpartners-element.md)

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

El tipo complejo [**providerType**](schema-providertype-complextype.md) define el elemento **ProviderID.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Provider (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




