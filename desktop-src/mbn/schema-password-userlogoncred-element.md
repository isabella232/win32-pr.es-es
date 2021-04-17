---
description: Especifica la contraseña que se usa para autenticar a un usuario.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (UserLogonCred), elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666491"
---
# <a name="password-userlogoncred-element"></a>Password (UserLogonCred), elemento

El elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) especifica la contraseña que se usa para autenticar a un usuario.

El elemento es una cadena de hasta 255 caracteres.

Este elemento es opcional.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

El elemento de **contraseña** se define mediante el elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 




