---
title: 'Elemento TrustedRootCA (ServerValidationParameters): Connection'
description: Captura la huella digital de las entidades de certificación raíz (CA) de confianza para el cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8f5b129f2db80bc46b24d1a935eea9294d423b205268ec0885869613d44a8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904477"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Elemento TrustedRootCA (ServerValidationParameters) para las propiedades de conexión

El **elemento TrustedRootCA (ServerValidationParameters)** captura la huella digital de las entidades de certificación (CA) raíz de confianza para el cliente.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

El **elemento TrustedRootCA** se define mediante el tipo complejo [**ServerValidationParameters.**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)

## <a name="remarks"></a>Comentarios

La huella digital es una cadena hexadecimal que contiene el hash SHA-1 del certificado. El **elemento TrustedRootCA** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

[Eaptlsconnectionpropertiesv1 Schema Elements](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





