---
description: Especifica los parámetros necesarios para configurar una conexión de datos.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Elemento Context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: 6d5e5d6db0a2d2c2e207a61a7d20d9a084416954b54c98f6429e3916b526e663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066149"
---
# <a name="context-mbnprofile-element"></a>Elemento Context (MBNProfile)

El **elemento Context (MBNProfile)** especifica los parámetros necesarios para configurar una conexión de datos.

El elemento puede tener los siguientes elementos secundarios.

-   [**AccessString**](schema-accessstring-contexttype-element.md)
-   [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
-   [**Compresión**](schema-compression-contexttype-element.md)
-   [**AuthProtocol**](schema-authprotocol-contexttype-element.md)

Este elemento puede tener un máximo de una repetición.

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

El **elemento Context** se define mediante el elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




