---
title: headerFieldsType (tipo complejo)
description: Define los elementos que especifican los campos de un encabezado de correo electrónico.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- headerFieldsType de tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c05b0e739a7aa75fb8e628de45cd929dd8c0b1e696ecef751c0fc8f08d926f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356367"
---
# <a name="headerfieldstype-complex-type"></a>headerFieldsType (tipo complejo)

Define los elementos que especifican los campos de un encabezado de correo electrónico.

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                                       | Descripción                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Especifica un campo en un encabezado de correo electrónico. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





