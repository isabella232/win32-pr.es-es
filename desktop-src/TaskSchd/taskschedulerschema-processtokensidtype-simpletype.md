---
title: Tipo simple de processTokenSidType
description: Define los valores posibles para el elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Programador de tareas de tipo simple processTokenSidType
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422161"
---
# <a name="processtokensidtype-simple-type"></a>Tipo simple de processTokenSidType

Define los valores posibles para el elemento [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .

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

El tipo simple **processTokenSidType** define los siguientes valores.



| Value        | Descripción                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| None         | Las tareas se ejecutan en un proceso que no contiene un SID de token de proceso (no se realizarán cambios en la lista de grupos de tokens de proceso).<br/> |
| Sin restricciones | Un SID de tarea se derivará de la ruta de acceso completa de la tarea y se agregará a la lista de grupos de tokens de proceso.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





