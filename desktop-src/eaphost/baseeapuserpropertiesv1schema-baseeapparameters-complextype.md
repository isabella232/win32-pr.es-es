---
title: 'Tipo complejo de BaseEapParameters: propiedades de usuario'
description: Define el elemento que especificó las credenciales seleccionadas del método heredado y específicas del método.
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718577"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Tipo complejo de BaseEapParameters: propiedades de usuario

El tipo complejo **BaseEapParameters** define el elemento que especificó las credenciales seleccionadas del método heredado y específicas del método.

El método puede definir los elementos constituyentes dentro de **BaseEapParameters**; el método también realiza la validación de esquemas en los elementos de **BaseEapParameters**.

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
| [**Automáticamente**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | integer | Define el elemento de marcador de posición para el tipo de método seleccionado y las credenciales específicas del método. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





