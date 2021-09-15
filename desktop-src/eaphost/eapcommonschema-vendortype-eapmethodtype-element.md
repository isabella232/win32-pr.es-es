---
title: Elemento VendorType (EapMethodType)
description: Obtenga información sobre el elemento VendorType (EapMethodType). Este elemento es el tipo definido por el proveedor para el método .
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorType EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568788"
---
# <a name="vendortype-eapmethodtype-element"></a>Elemento VendorType (EapMethodType)

El **elemento VendorType (EapMethodType)** es el tipo definido por el proveedor para el método .

El **elemento VendorType** es opcional. Si se usa, **VendorType es** un número único emitido por internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

El tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) define el elemento **VendorType.**

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





