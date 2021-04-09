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
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154192"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento Provider (DataRoamingPartners)

El elemento **Provider (DataRoamingPartners)** identifica el nombre y el identificador de proveedor de una red de telefonía móvil.

Este elemento tiene los siguientes elementos secundarios.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Este elemento se puede definir varias veces dentro del elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) . Debe definirse al menos una vez.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

El elemento de **proveedor** se define mediante el elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 




