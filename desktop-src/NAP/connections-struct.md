---
title: Estructura de conexiones (NapEnforcementClient. h)
description: Contiene información sobre la lista de conexiones mantenida por un aplicador.
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
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997157"
---
# <a name="connections-structure"></a>Estructura de conexiones

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La estructura de **conexiones** contiene información sobre la lista de conexiones mantenida por un aplicador.

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

El número de conexiones activas que mantiene actualmente un aplicador en el intervalo de 0 (cero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**connections**
</dt> <dd>

Puntero COM a una lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representan las conexiones de cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de NAP](nap-reference.md)
</dt> <dt>

[Estructuras de NAP](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





