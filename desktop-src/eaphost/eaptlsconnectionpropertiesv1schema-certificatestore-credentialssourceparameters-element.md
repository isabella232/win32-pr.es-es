---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica que EAP-TLS debe leer el certificado de Mi almacén del usuario o de la máquina que se autentica.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento EAPHost de CertificateStore
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fb3d2b5c9d50ea8b63c513e4fd9e7297afe236c5ccd16711d9bf4371e76a8d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274297"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>Elemento CertificateStore (CredentialsSourceParameters)

El **elemento CertificateStore (CredentialsSourceParameters)** indica que EAP-TLS debe leer el certificado de My Store del usuario o de la máquina que se está autenticando.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

El tipo complejo [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) define el elemento **CertificateStore.**

## <a name="remarks"></a>Comentarios

Los **elementos CertificateStore** [**y SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) no se pueden usar simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





