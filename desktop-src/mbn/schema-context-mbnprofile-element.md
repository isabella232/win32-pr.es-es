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
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241203"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
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

 

 




