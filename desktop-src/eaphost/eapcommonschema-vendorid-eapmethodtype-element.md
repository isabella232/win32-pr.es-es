---
title: VendorId (EapMethodType), elemento
description: Hace referencia al proveedor que definió el método si el elemento Type (EapMethodType) es 254 (un método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VendorId EAPHost
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534276"
---
# <a name="vendorid-eapmethodtype-element"></a>VendorId (EapMethodType), elemento

El elemento **VendorId (EapMethodType)** hace referencia al proveedor que definió el método si el elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido).

**VendorId** es opcional. Si se usa, el **VendorId** es un número único emitido por Internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

El elemento **VendorId** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Observaciones

No es necesario que los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y **VendorId** sean los mismos para un método determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 





