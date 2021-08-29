---
description: Especifica cómo controlar las contraseñas al actualizar perfiles.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 683fafb763e3f8613afa1b8dca99020856d67a03fdb44e993adf032ce166ceab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975174"
---
# <a name="ignorepassword-userlogoncred-element"></a>Elemento IgnorePassword (UserLogonCred)

El **elemento IgnorePassword (UserLogonCred)** especifica cómo controlar las contraseñas al actualizar perfiles.

Si se establece en **TRUE** y existe un perfil con el mismo nombre en el momento de la operación de actualización, la contraseña de ese perfil se toma y se almacena en el nuevo perfil.

Este elemento es opcional.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

El **elemento IgnorePassword** se define mediante el [**elemento UserLogonCred.**](schema-userlogoncred-contexttype-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
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

 

 




