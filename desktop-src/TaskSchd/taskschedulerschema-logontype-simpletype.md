---
title: Tipo simple logonType
description: Define los valores posibles del elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Tipo simple logonType Programador de tareas
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259175"
---
# <a name="logontype-simple-type"></a>Tipo simple logonType

Define los valores posibles del [**elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple logonType** define los valores siguientes.



| Value                      | Descripción                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | El usuario debe iniciar sesión con un servicio para el inicio de sesión del usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.<br/>                                                                                                                                                          |
| Contraseña                   | El usuario debe iniciar sesión con una contraseña.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | El usuario ya debe haber iniciado sesión. La tarea solo se ejecutará en una sesión interactiva existente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Ya no está en uso; actualmente es idéntica a La contraseña.<br/> **Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista y Windows Server 2008:** La tarea se ejecutará en una sesión interactiva existente o el usuario debe iniciar sesión con una contraseña.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos simples de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





