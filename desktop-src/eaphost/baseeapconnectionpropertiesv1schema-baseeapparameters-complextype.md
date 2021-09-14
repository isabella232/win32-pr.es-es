---
title: 'Tipo complejo BaseEapParameters: propiedades de conexión'
description: Define el elemento de marcador de posición para el tipo de método y la configuración específica del método.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Tipo complejo BaseEapParameters EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241323"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Tipo complejo BaseEapParameters: propiedades de conexión

El **tipo complejo BaseEapParameters** define el elemento de marcador de posición para el tipo de método y la configuración específica del método.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo    | Descripción                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Tipo**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | integer | Aquí se permite cualquier instancia de esquema.<br/> |



## <a name="remarks"></a>Observaciones

En **BaseEapParameters,** el método puede definir los elementos constituyentes. El método también realiza la validación del esquema en los elementos de **BaseEapParameters**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





