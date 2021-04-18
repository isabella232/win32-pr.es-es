---
description: Especifica cómo administrar las contraseñas al actualizar perfiles.
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
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715255"
---
# <a name="ignorepassword-userlogoncred-element"></a>Elemento IgnorePassword (UserLogonCred)

El elemento **IgnorePassword (UserLogonCred)** especifica cómo administrar las contraseñas al actualizar perfiles.

Si se establece en **true** y existe un perfil con el mismo nombre en el momento de la operación de actualización, se tomará la contraseña de ese perfil y se almacenará en el perfil nuevo.

Este elemento es opcional.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

El elemento **IgnorePassword** se define mediante el elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

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

 

 




