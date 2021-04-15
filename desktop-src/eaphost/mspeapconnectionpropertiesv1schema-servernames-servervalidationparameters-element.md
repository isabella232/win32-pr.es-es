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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649345"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Elemento ServerNames (ServerValidationParameters) (PEAP)

El elemento **servernames (ServerValidationParameters)** representa una lista de nombres de servidor delimitados por punto y coma.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

El elemento **servernames** se define mediante el tipo complejo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

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

 

 





