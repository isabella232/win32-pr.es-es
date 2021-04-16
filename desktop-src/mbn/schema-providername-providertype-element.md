---
description: Contiene el nombre de la red de telefonía móvil.
ms.assetid: 4169babb-7616-468a-93f0-de25cce0c88b
title: ProviderName (providerType) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderName
api_type:
- Schema
ms.openlocfilehash: 47929d508ad6d3a6567c1b52e720360f4e7cfbda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648211"
---
# <a name="providername-providertype-element"></a>ProviderName (providerType) (elemento)

El elemento **providerName (providerType)** contiene el nombre de la red de telefonía móvil.

El elemento es una cadena con un máximo de 20 caracteres.

Este elemento es opcional.

``` syntax
<xs:element name="ProviderName"
    type="providerNameType"
 />
```

El elemento **providerName** se define mediante el tipo complejo de [**providerType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Proveedor (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




