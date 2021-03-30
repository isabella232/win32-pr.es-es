---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: Obtenga información sobre el elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica si se debe solicitar la validación del servidor al usuario. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Elemento DisableUserPromptForServerValidation EAPHost
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
ms.openlocfilehash: 368b2593b3c55ef571e3f1892634318e54447643
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280014"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (TLS)

El elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica si se debe pedir al usuario la validación del servidor.

Si **DisableUserPromptForServerValidation** es true, EAP-TLS realiza la validación del servidor sin intervención del usuario; Si se produce un error en la validación, EAP-TLS produce un error en la autenticación. Si **DisableUserPromptForServerValidation** es false, se solicita al usuario un certificado o un nombre de servidor validados, o una entidad de certificación raíz (CA).

El elemento **DisableUserPromptForServerValidation** es opcional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

El elemento **DisableUserPromptForServerValidation** se define mediante el tipo complejo de [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Posibles elementos primarios inmediatos en la instancia de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





