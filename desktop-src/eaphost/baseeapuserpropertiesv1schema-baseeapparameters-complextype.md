---
title: 'Tipo complejo BaseEapParameters: propiedades de usuario'
description: Define el elemento que especificó el método heredado seleccionado y las credenciales específicas del método.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 80ae1dc749d1c31ee11809b530fe1b04a59ce3e4e4dc76e84323b7dc078ec44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978295"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Tipo complejo BaseEapParameters: propiedades de usuario

El **tipo complejo BaseEapParameters** define el elemento que especificó el método heredado seleccionado y las credenciales específicas del método.

El método puede definir los elementos constituyentes dentro **de BaseEapParameters**; El método también realiza la validación del esquema en los elementos de **BaseEapParameters**.

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



| Elemento                                                                      | Tipo    | Descripción                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**Tipo**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | integer | Define el elemento de marcador de posición para el tipo de método seleccionado y las credenciales específicas del método. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1 Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





