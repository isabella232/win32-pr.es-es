---
title: Username (elemento) (TLS)
description: Obtenga información sobre el elemento username. Este elemento captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Username (elemento) EAPHost
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
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705027"
---
# <a name="username-element-tls"></a>Username (elemento) (TLS)

El elemento **username** captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.

Si falta el elemento **username** , EAP-TLS usa el nombre del certificado al que se hace referencia en el elemento [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Requisitos



| Role | Versiones mínimas admitidas del sistema operativo |
|------|-------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





