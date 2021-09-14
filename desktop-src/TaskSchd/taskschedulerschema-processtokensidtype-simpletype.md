---
title: Tipo simple processTokenSidType
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
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968700"
---
# <a name="processtokensidtype-simple-type"></a>Tipo simple processTokenSidType

Define los valores posibles para [**el elemento ProcessTokenSidType (principalType).**](taskschedulerschema-processtokensidtype-principaltype-element.md)

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
| Sin restricciones | Un SID de tarea se derivará de la ruta de acceso de tarea completa y se agregará a la lista de grupos de tokens de proceso.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





