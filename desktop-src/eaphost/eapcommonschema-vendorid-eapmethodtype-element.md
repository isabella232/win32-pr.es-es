---
title: Elemento VendorId (EapMethodType)
description: Hace referencia al proveedor que definió el método si el elemento Type (EapMethodType) es 254 (un método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VENDORId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29508121a9724a52df19038b82d97576a924c3c8bab49ac6801c1de51ec71919
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067305"
---
# <a name="vendorid-eapmethodtype-element"></a>Elemento VendorId (EapMethodType)

El **elemento VendorId (EapMethodType)** hace referencia al proveedor que definió el método si el elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido).

**VendorId** es opcional. Si se usa, **vendorId** es un número único emitido por internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

El tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) define el elemento **VendorId.**

## <a name="remarks"></a>Comentarios

Los [**elementos AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y **VendorId** no necesitan ser iguales para un método determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 





