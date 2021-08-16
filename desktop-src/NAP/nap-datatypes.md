---
title: Tipos de datos NAP (NapTypes.h)
description: Nota La plataforma de protección de acceso a redes no está disponible a partir de Windows 10 Los tipos de datos de la API de protección de acceso a redes (NAP) son los siguientes.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Porcentaje
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550baa14779ccefaec14605938edb6076e7cc332aa9d1a2390ab430f7568e844
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802625"
---
# <a name="nap-datatypes"></a>Tipos de datos NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los tipos de datos de la API de Protección de acceso a redes (NAP) son los siguientes.


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**ProbationTime**
</dt> <dd>

Estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene una hora relacionada con la sondeación de un equipo cliente.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Valor que especifica el intervalo de valores posibles para el tamaño máximo, en bytes, de un [**paquete SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) definido por range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Identificador único de 4 bytes usado por SHA, SHV y clientes de cumplimiento para identificarse. Los tres primeros bytes son el código SMI asignado por IETF del proveedor y el último byte identifica el propio componente.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Valor **napComponentId** que se usa para identificar los pares SHA/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Valor **napComponentId que** se usa para identificar los clientes de cumplimiento.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Valor que especifica el número de SHA registrados en el sistema NAP en el intervalo de 0 (cero) a [**maxSystemHealthEntityCount**](nap-type-constants.md).

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Valor que especifica el número de clientes de cumplimiento en el sistema NAP en el intervalo de 0 (cero) a [**maxEnforcerCount**](nap-type-constants.md).

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

La [**versión CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de una [**estructura CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que se usa para [**emparejar SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) con **SoHResponses.**

</dd> <dt>

**ConnectionId**
</dt> <dd>

Identificador único global único (GUID) que se usa para identificar las conexiones NAP mantenidas por los clientes de cumplimiento.

</dd> <dt>

**Porcentaje**
</dt> <dd>

Valor que contiene el porcentaje entre 0 (cero) y 100 de corrección que se ha completado

</dd> <dt>

**MessageId**
</dt> <dd>

Valor único que se usa para identificar los mensajes del sistema NAP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



 

