---
title: Tipo simple de logonType
description: Define los valores posibles del elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Programador de tareas de tipo simple logonType
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150797"
---
# <a name="logontype-simple-type"></a>Tipo simple de logonType

Define los valores posibles del elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .

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

El tipo simple **logonType** define los siguientes valores.



| Value                      | Descripción                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.<br/>                                                                                                                                                          |
| Contraseña                   | El usuario debe iniciar sesión con una contraseña.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | El usuario ya debe haber iniciado sesión. La tarea se ejecutará solo en una sesión interactiva existente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Ya no se utiliza; es idéntico a password.<br/> **Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista y Windows server 2008:** La tarea se ejecutará en una sesión interactiva existente o el usuario debe iniciar sesión con una contraseña.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos simples de esquema de Programador de tareas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





