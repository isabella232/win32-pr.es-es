---
title: Elemento Password (EapType)
description: Obtenga información sobre el elemento Password (EapType). Este elemento identifica la contraseña del usuario o la máquina que se está autenticando.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbcb7b0acd372bbe71ee6d22f44a736948b145378f62f40820e3de53d77b875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273204"
---
# <a name="password-eaptype-element"></a>Elemento Password (EapType)

El **elemento Password (EapType)** identifica la contraseña del usuario o la máquina que se autentica.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

El **elemento Password** se define mediante el elemento [**EapType.**](mschapv2userpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Comentarios

Si el **elemento Password (EapType)** no está presente, el hash de contraseña se obtiene de winlogon. Este elemento es opcional.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Server<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1 Schema](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





