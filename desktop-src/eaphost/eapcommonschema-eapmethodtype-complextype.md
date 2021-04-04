---
title: Tipo complejo de EapMethodType
description: Define los elementos que identifican de forma única un solo tipo de método EAP, VendorId, VendorType y AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Tipo complejo EapMethodType EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802533"
---
# <a name="eapmethodtype-complex-type"></a>Tipo complejo de EapMethodType

El tipo complejo **EapMethodType** define los elementos que identifican de forma única un solo método EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) son elementos obligatorios, mientras que [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) solo son necesarios cuando el elemento **Type** es 254 (un método EAP ampliado).

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                | Tipo         | Descripción                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Hace referencia al autor del método. <br/>                                                                                                                                                                                                                 |
| [**Tipo**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Hace referencia al tipo de método EAP. <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Hace referencia al proveedor que definió el método, si el elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido). [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) es opcional. <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Es el tipo definido por el proveedor para el método. [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) es opcional. <br/>                                                                                                           |



## <a name="remarks"></a>Observaciones

No es necesario que los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) sean los mismos para un método determinado.

Los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) y [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) son un número único emitido por Internet Assigned Numbers Authority (IANA).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





