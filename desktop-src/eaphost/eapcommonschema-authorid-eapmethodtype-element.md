---
title: AuthorId (EapMethodType), elemento
description: Obtenga información sobre el elemento AuthorId (EapMethodType). El elemento AuthorID (EapMethodType) hace referencia al autor del método.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento AuthorId EAPHost
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
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995638"
---
# <a name="authorid-eapmethodtype-element"></a>AuthorId (EapMethodType), elemento

El elemento **AuthorId (EapMethodType)** hace referencia al autor del método.

AuthorId es un número único emitido por Internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

El elemento **AuthorId** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Observaciones

No es necesario que los elementos **AuthorId** y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) sean los mismos para un método determinado.

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

 

 





