---
title: Elemento ServerNames (ServerValidationParameters) (TLS)
description: Obtenga información sobre el elemento ServerNames (ServerValidationParameters). Este elemento representa una lista de nombres de servidor delimitados por punto y coma. | Elemento ServerNames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Elemento ServerNames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698156"
---
# <a name="servernames-servervalidationparameters-element-tls"></a>Elemento ServerNames (ServerValidationParameters) (TLS)

El elemento **servernames (ServerValidationParameters)** representa una lista de nombres de servidor delimitados por punto y coma.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

El elemento **servernames** se define mediante el tipo complejo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Observaciones

Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares. El elemento **servernames** es opcional.

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

 

 





