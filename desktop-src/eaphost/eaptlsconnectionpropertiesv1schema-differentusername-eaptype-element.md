---
title: Elemento DifferentUsername (EapType)
description: Obtenga información sobre el elemento DifferentUsername (EapType). Este elemento determina el nombre de usuario EAP-TLS que se va a usar.
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
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705025"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

El elemento **DifferentUsername (EapType)** determina el nombre de usuario EAP-TLS que se va a usar.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

El elemento **DifferentUsername** se define mediante el elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si el elemento **DifferentUserName** es true, EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado. Si el elemento **DifferentUserName** es false, EAP-TLS usa el nombre de usuario que aparece en el certificado.

El elemento **DifferentUserName** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





