---
title: tipo complejo showMessageType
description: Define los elementos que representan una acción que muestra un cuadro de mensaje.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Tipo complejo showMessageType Programador de tareas
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968664"
---
# <a name="showmessagetype-complex-type"></a>tipo complejo showMessageType

Define los elementos que representan una acción que muestra un cuadro de mensaje.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                            | Tipo           | Descripción                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Cuerpo**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Especifica el texto que se mostrará en el cuerpo del cuadro de mensaje. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Especifica el título del cuadro de mensaje. <br/>                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





