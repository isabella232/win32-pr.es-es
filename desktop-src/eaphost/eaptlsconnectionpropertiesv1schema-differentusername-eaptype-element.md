---
title: Elemento DifferentUsername (EapType)
description: Obtenga información sobre el elemento DifferentUsername (EapType). Este elemento determina qué nombre de usuario debe usar EAP-TLS.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360139"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

El **elemento DifferentUsername (EapType)** determina qué nombre de usuario va a usar EAP-TLS.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

El elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) define el elemento **DifferentUsername.**

## <a name="remarks"></a>Observaciones

Si el **elemento DifferentUserName** es TRUE, EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado. Si el **elemento DifferentUserName** es FALSE, EAP-TLS usa el nombre de usuario que aparece en el certificado.

El **elemento DifferentUserName** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Remoto<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Eaptlsconnectionpropertiesv1 Schema Elements](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





