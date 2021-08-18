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
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984095"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

El **elemento DifferentUsername (EapType)** determina qué nombre de usuario va a usar EAP-TLS.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

El elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) define el elemento **DifferentUsername.**

## <a name="remarks"></a>Comentarios

Si el **elemento DifferentUserName** es TRUE, EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado. Si el **elemento DifferentUserName** es FALSE, EAP-TLS usa el nombre de usuario que aparece en el certificado.

El **elemento DifferentUserName** es opcional.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

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

 

 





