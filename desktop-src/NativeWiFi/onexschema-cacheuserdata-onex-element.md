---
description: Especifica si las credenciales de usuario se almacenan en caché para las conexiones posteriores.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169454"
---
# <a name="cacheuserdata-onex-element"></a>Elemento cacheUserData (OneX)

El elemento cacheUserData (OneX) especifica si las credenciales de usuario se almacenan en caché para las conexiones posteriores. Cuando cacheUserData es TRUE, las credenciales se almacenan en caché. Cuando cacheUserData es FALSE, las credenciales no se almacenan en caché y es posible que se le pidan credenciales al usuario en los intentos de conexión posteriores.

Este elemento es opcional. Cuando no se especifica cacheUserData en un perfil, las credenciales de usuario se almacenan en caché.

**Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

El **elemento cacheUserData** se define mediante [**el elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




