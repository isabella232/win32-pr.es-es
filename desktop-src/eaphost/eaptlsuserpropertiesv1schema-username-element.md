---
title: Elemento Username (TLS)
description: Obtenga información sobre el elemento Username. Este elemento captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Elemento EAPHost del nombre de usuario
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6748ac8c352540d2288cf3bf3c790004d832ba47961fbc7b9e8211fa712ccb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720124"
---
# <a name="username-element-tls"></a>Elemento Username (TLS)

El **elemento Username** captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.

Si el **elemento Username** no está presente, EAP-TLS usa el nombre del certificado al que se hace referencia en el [**elemento UserCert.**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md)

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Requisitos



| Rol | Versiones mínimas del sistema operativo admitidas |
|------|-------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





