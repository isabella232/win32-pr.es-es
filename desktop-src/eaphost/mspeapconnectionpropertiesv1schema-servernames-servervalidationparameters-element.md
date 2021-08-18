---
title: Elemento ServerNames (ServerValidationParameters) (PEAP)
description: Obtenga información sobre el elemento ServerNames (ServerValidationParameters). Este elemento representa una lista de nombres de servidor delimitados por punto y coma. | Elemento ServerNames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: f3f9de6ee28077b5206a9783ef7722864a479e1e5f26b78e4402ac79c6e4be5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984015"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Elemento ServerNames (ServerValidationParameters) (PEAP)

El **elemento ServerNames (ServerValidationParameters)** representa una lista de nombres de servidor delimitados por punto y coma.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

El tipo complejo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) define el elemento **ServerNames.**

## <a name="remarks"></a>Comentarios

Cada nombre de servidor está delimitado por punto y coma y se puede representar mediante expresiones regulares. El **elemento ServerNames** es opcional.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
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

[Mspeapconnectionpropertiesv1 Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





