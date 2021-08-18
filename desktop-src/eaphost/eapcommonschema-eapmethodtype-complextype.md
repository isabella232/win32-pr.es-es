---
title: Tipo complejo EapMethodType
description: Define los elementos que identifican de forma única un único tipo de método EAP, VendorId, VendorType y AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType de tipo complejo EAPHost
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
ms.openlocfilehash: 059ea8162241c61d88fc93f565fa0aa4ba8aee223212e6fab254ed9d5dec4eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739175"
---
# <a name="eapmethodtype-complex-type"></a>Tipo complejo EapMethodType

El **tipo complejo EapMethodType** define los elementos que identifican de forma única un único método EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) son elementos obligatorios, mientras que [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) solo son necesarios cuando el **elemento Type** es 254 (un método EAP expandido).

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
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Hace referencia al proveedor que definió el método , si el [**elemento Type**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido). [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) es opcional. <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Es el tipo definido por el proveedor para el método . [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) es opcional. <br/>                                                                                                           |



## <a name="remarks"></a>Comentarios

Los [**elementos AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) no necesitan ser iguales para un método determinado.

Los [**elementos AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) y [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) son cada uno un número único emitido por internet Assigned Numbers Authority (IANA).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





