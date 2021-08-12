---
title: ProcessTokenSidType Simple Type
description: Define los valores posibles para el elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Tipo simple processTokenSidType Programador de tareas
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611907"
---
# <a name="processtokensidtype-simple-type"></a>ProcessTokenSidType Simple Type

Define los valores posibles [**para el elemento ProcessTokenSidType (principalType).**](taskschedulerschema-processtokensidtype-principaltype-element.md)

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple processTokenSidType** define los valores siguientes.



| Value        | Descripción                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| None         | Las tareas se ejecutan en un proceso que no contiene un SID de token de proceso (no se realizará ningún cambio en la lista de grupos de tokens de proceso).<br/> |
| Sin restricciones | Un SID de tarea se derivará de la ruta de acceso completa de la tarea y se agregará a la lista de grupos de tokens de proceso.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





