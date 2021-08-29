---
description: Especifica la contraseña usada para autenticar a un usuario.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Elemento Password (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: 63ee5386c4bd9eb168e4b4ac663e857590509ebf5ab0183165fdb5e7ab59a7e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035793"
---
# <a name="password-userlogoncred-element"></a>Elemento Password (UserLogonCred)

El [**elemento Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) especifica la contraseña usada para autenticar a un usuario.

El elemento es una cadena de hasta 255 caracteres.

Este elemento es opcional.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

El **elemento Password** se define mediante el elemento [**UserLogonCred.**](schema-userlogoncred-contexttype-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**UserLogonCred (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




