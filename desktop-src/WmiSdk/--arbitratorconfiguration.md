---
description: Limita los recursos internos que usan las operaciones iniciadas por clientes WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: __ArbitratorConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 4344eb368a96d2d47207748cba622d07d11ef78e0a046c6ea169305d9c587957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321125"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_Clase Desconfiguración

La **\_ \_ claseConfigurationConfiguration** es una clase de configuración que limita los recursos internos que usan las operaciones iniciadas por clientes WMI. Se trata de una clase singleton que reside en el espacio \\ de nombres raíz. La clase se genera internamente, por lo que no hay ningún archivo MOF para ella.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a>Miembros

La **\_ \_ claseConfigurationConfiguration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ claseConfigurationConfiguration** tiene estas propiedades.

<dl> <dt>

**OutstandingTasksPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número de tareas pendientes iniciadas por el usuario en cualquier momento.

</dd> <dt>

**OutstandingTasksTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número total de tareas pendientes en cualquier momento.

</dd> <dt>

**PermanentSubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de suscripciones permanentes permitidas para un usuario determinado en cualquier momento.

</dd> <dt>

**PermanentSubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de suscripciones permanentes permitidas para todos los usuarios en cualquier momento.

</dd> <dt>

**PollingInstructionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de consultas de eventos de sondeo permitidas para un usuario determinado en cualquier momento.

</dd> <dt>

**PollingInstructionsTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de instrucciones de sondeo permitidas para todos los usuarios en cualquier momento.

</dd> <dt>

**PollingMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de consultas de eventos de sondeo de memoria, emitidas por un usuario determinado, puede consumir en cualquier momento.

</dd> <dt>

**PollingMemoryTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad total de memoria que las consultas de eventos de sondeo, para todos los usuarios combinados, pueden consumidor en cualquier momento.

</dd> <dt>

**QuotaRetryCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número de infracciones de cuota permitidas antes de cancelar una tarea.

</dd> <dt>

**QuotaRetryWaitInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Retraso introducido en la ejecución de la tarea en cada infracción de cuota.

</dd> <dt>

**TaskThreadsPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número máximo de subprocesos de tareas asociados a un usuario determinado una vez.

</dd> <dt>

**TaskThreadsTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número máximo de subprocesos de tareas.

</dd> <dt>

**TemporarySubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de suscripciones temporales permitidas para un usuario determinado en cualquier momento.

</dd> <dt>

**TemporarySubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de suscripciones temporales permitidas para todos los usuarios en cualquier momento.

</dd> <dt>

**TotalCacheDisk**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Caché de disco total asociada a todos los usuarios en cualquier momento.

</dd> <dt>

**TotalCacheDiskPerTask**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Caché de disco total asociada a una tarea determinada en cualquier momento.

</dd> <dt>

**TotalCacheDiskPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Caché de disco total asociada a un usuario determinado en cualquier momento.

</dd> <dt>

**TotalCacheMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Memoria caché total asociada a todos los usuarios en cualquier momento.

</dd> <dt>

**TotalCacheMemoryPerTask**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Memoria caché total asociada a una tarea determinada en cualquier momento.

</dd> <dt>

**TotalCacheMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Memoria caché total asociada a un usuario determinado en cualquier momento.

</dd> <dt>

**TotalUsers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sin usar. Número máximo de usuarios conectados.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**\_ \_ ConfigurationConfiguration** se hereda de [**\_ \_ SystemClass.**](--systemclass.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Root<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

