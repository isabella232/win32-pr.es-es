---
description: Identifica el nombre y el identificador de proveedor de una red de telefonía móvil.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347165"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento Provider (DataRoamingPartners)

El **elemento Provider (DataRoamingPartners)** identifica el nombre y el identificador del proveedor de una red de telefonía móvil.

Este elemento tiene los siguientes elementos secundarios.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Este elemento se puede definir varias veces dentro del [**elemento DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md) Debe definirse al menos una vez.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

El **elemento Provider** se define mediante el elemento [**DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




