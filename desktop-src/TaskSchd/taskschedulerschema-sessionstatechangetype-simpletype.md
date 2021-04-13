---
title: Tipo simple de sessionStateChangeType
description: Define los valores para el tipo de Terminal Server cambio de estado de sesión que puede usar para desencadenar la inicio de una tarea.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Programador de tareas de tipo simple sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492269"
---
# <a name="sessionstatechangetype-simple-type"></a>Tipo simple de sessionStateChangeType

Define los valores para el tipo de Terminal Server cambio de estado de sesión que puede usar para desencadenar la inicio de una tarea.

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El tipo simple **sessionStateChangeType** define los siguientes valores.



| Value             | Descripción                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Terminal Server cambio del estado de conexión de la consola. Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                            |
| ConsoleDisconnect | Terminal Server cambio de estado de desconexión de la consola. Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                      |
| RemoteConnect     | Terminal Server cambio de estado de la conexión remota. Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa de Conexión a Escritorio remoto desde un equipo remoto. <br/>            |
| RemoteDisconnect  | Terminal Server cambio de estado de desconexión remota. Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa el programa Conexión a Escritorio remoto desde un equipo remoto. <br/> |
| SessionLock       | Terminal Server cambio de estado de la sesión bloqueada. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado. <br/>                                                       |
| SessionUnlock     | Terminal Server cambio de estado desbloqueado de la sesión. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando se desbloquea el equipo.<br/>                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





