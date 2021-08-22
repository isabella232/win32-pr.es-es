---
title: Elemento DisableUserPromptForServerValidation (PEAP)
description: Obtenga información sobre el elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica si se debe solicitar al usuario la validación del servidor. | Elemento DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- Elemento EAPHost DisableUserPromptForServerValidation
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c032c4c0dcb67f60f64fe2b447fd1af7061df51ed19586f4ee15b43d6a6f870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561765"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)

El **elemento DisableUserPromptForServerValidation (ServerValidationParameters)** indica si se debe solicitar al usuario la validación del servidor.

Si **DisableUserPromptForServerValidation** es TRUE, EAP-TLS realiza la validación del servidor sin la entrada del usuario; Si se produce un error en la validación, EAP-TLS produce un error en la autenticación. Si **DisableUserPromptForServerValidation** es FALSE, se solicita al usuario un nombre o certificado de servidor validado o una entidad de certificación (CA) raíz.

El **elemento DisableUserPromptForServerValidation** es opcional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

El tipo complejo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) define el elemento **DisableUserPromptForServerValidation.**

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Posibles elementos primarios inmediatos en la instancia de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





