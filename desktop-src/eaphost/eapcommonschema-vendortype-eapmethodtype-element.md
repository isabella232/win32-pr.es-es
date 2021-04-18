---
title: VendorType (EapMethodType), elemento
description: Obtenga información sobre el elemento VendorType (EapMethodType). Este elemento es el tipo definido por el proveedor para el método.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorType de VendorType
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
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488271"
---
# <a name="vendortype-eapmethodtype-element"></a>VendorType (EapMethodType), elemento

El elemento **VendorType (EapMethodType)** es el tipo definido por el proveedor para el método.

El elemento **VendorType** es opcional. Si se utiliza, **VendorType** es un número único emitido por Internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

El elemento **VendorType** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 





