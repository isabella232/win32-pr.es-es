---
title: 'Tipo complejo BaseEapParameters: propiedades de conexión'
description: Define el elemento de marcador de posición para el tipo de método y la configuración específica del método.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- EapHost de tipo complejo BaseEapParameters
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
ms.openlocfilehash: 4ae3abf23b19badb123f8eb49097c6b3e9d7ac6d26fc0132f34b84de5ac24c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086959"
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



## <a name="remarks"></a>Comentarios

En **BaseEapParameters,** el método puede definir los elementos constituyentes. El método también realiza la validación del esquema en los elementos de **BaseEapParameters**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





