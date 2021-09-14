---
title: Elemento AuthorId (EapMethodType)
description: Obtenga información sobre el elemento AuthorId (EapMethodType). El elemento AuthorID (EapMethodType) hace referencia al autor del método.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento EAPHost de AuthorId
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168441"
---
# <a name="authorid-eapmethodtype-element"></a>Elemento AuthorId (EapMethodType)

El **elemento AuthorId (EapMethodType)** hace referencia al autor del método.

AuthorId es un número único emitido por internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

El tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) define el elemento **AuthorId.**

## <a name="remarks"></a>Observaciones

Los **elementos AuthorId** y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) no necesitan ser iguales para un método determinado.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima del sistema operativo admitida |
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

 

 





