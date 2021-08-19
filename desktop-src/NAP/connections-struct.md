---
title: Estructura de conexiones (NapEnforcementClient.h)
description: Contiene información sobre la lista de conexiones mantenidas por un ejecutor.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Estructura de conexiones NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800152"
---
# <a name="connections-structure"></a>Estructura de conexiones

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **estructura Connections** contiene información sobre la lista de conexiones mantenidas por un ejecutor.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Miembros

<dl> <dt>

**count**
</dt> <dd>

Número de conexiones activas mantenidas actualmente por un ejecutor dentro del intervalo de 0 (cero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**connections**
</dt> <dd>

Puntero COM a una lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representan conexiones de cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de NAP](nap-reference.md)
</dt> <dt>

[Estructuras nap](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





