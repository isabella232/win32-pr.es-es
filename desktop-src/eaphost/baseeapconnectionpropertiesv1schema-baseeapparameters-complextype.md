---
title: 'Tipo complejo de BaseEapParameters: propiedades de conexión'
description: Define el elemento de marcador de posición para la configuración específica del método y el tipo de método.
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
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105698464"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Tipo complejo de BaseEapParameters: propiedades de conexión

El tipo complejo **BaseEapParameters** define el elemento de marcador de posición para la configuración específica del método y el tipo de método.

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
| [**Automáticamente**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | integer | Aquí se permite cualquier instancia del esquema.<br/> |



## <a name="remarks"></a>Observaciones

En **BaseEapParameters** , el método puede definir los elementos constituyentes. El método también realiza la validación de esquemas en los elementos de **BaseEapParameters**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





