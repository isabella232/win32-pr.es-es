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
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571868"
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

## <a name="remarks"></a>Observaciones

Los [**elementos AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y **VendorId** no necesitan ser iguales para un método determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





