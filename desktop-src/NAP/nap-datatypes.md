---
title: Tipos de NapTypes. h de NAP
description: 'Nota: la plataforma de protección de acceso a redes no está disponible a partir de Windows 10. los tipos de la API de protección de acceso a redes (NAP) son los siguientes.'
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
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996890"
---
# <a name="nap-datatypes"></a>Tipos de texto de NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los tipos de la API de protección de acceso a redes (NAP) son los siguientes.


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

Una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene una hora relacionada con el período de prueba de un equipo cliente.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Valor que especifica el intervalo de valores posibles para el tamaño máximo, en bytes, de un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) tal y como lo define el intervalo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Identificador único de 4 bytes que usan Sha, SHV y clientes de cumplimiento para identificarse. Los tres primeros bytes son el código SMI asignado por IETF del proveedor y el último byte identifica el propio componente.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Valor de **NapComponentId** que se usa para identificar pares Sha/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Valor de **NapComponentId** que se usa para identificar los clientes de cumplimiento.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Valor que especifica el número de Sha registrados en el sistema NAP en el intervalo de 0 (cero) a [**maxSystemHealthEntityCount**](nap-type-constants.md).

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Valor que especifica el número de clientes de cumplimiento en el sistema NAP en el intervalo de 0 (cero) a [**maxEnforcerCount**](nap-type-constants.md).

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

La versión [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de una estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usada para emparejar [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) con **SoHResponses**.

</dd> <dt>

**ConnectionId**
</dt> <dd>

Un identificador único global (GUID) único que se usa para identificar las conexiones NAP mantenidas por los clientes de cumplimiento.

</dd> <dt>

**Porcentaje**
</dt> <dd>

Un valor que contiene el porcentaje comprendido entre 0 (cero) y 100 de corrección completada

</dd> <dt>

**MessageId**
</dt> <dd>

Un valor único que se usa para identificar los mensajes del sistema NAP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



 

