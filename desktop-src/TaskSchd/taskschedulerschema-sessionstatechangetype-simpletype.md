---
title: Tipo simple sessionStateChangeType
description: Define los valores para el tipo de cambio de estado de sesión de Terminal Server que puede usar para desencadenar una tarea que se va a iniciar.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Tipo simple sessionStateChangeType Programador de tareas
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a67334b2e8d51404a0e5e78a7d2b3e49908cd1c6ce74f499e66272d2db9be910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099815"
---
# <a name="sessionstatechangetype-simple-type"></a>Tipo simple sessionStateChangeType

Define los valores para el tipo de cambio de estado de sesión de Terminal Server que puede usar para desencadenar una tarea que se va a iniciar.

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

El **tipo simple sessionStateChangeType** define los valores siguientes.



| Value             | Descripción                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Cambio del estado de conexión de la consola de Terminal Server. Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                            |
| ConsoleDisconnect | Cambio de estado de desconexión de la consola de Terminal Server. Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                      |
| RemoteConnect     | Cambio de estado de conexión remota de Terminal Server. Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa Conexión a Escritorio remoto desde un equipo remoto. <br/>            |
| RemoteDisconnect  | Cambio de estado de desconexión remota de Terminal Server. Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa Conexión a Escritorio remoto programa desde un equipo remoto. <br/> |
| SessionLock       | Cambio de estado bloqueado de sesión de Terminal Server. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado. <br/>                                                       |
| SessionUnlock     | Cambio de estado desbloqueado de la sesión de Terminal Server. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está desbloqueado.<br/>                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





