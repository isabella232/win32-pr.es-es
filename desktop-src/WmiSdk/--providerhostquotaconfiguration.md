---
description: Permite establecer límites en el uso del proceso de host de los recursos del sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277129"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_Clase ProviderHostQuotaConfiguration

La clase del sistema **\_ \_ ProviderHostQuotaConfiguration** es una clase de configuración para los procesos del proveedor de host. Esta clase reside en el espacio de nombres raíz y permite establecer límites en el uso del proceso de host de los recursos del sistema.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ProviderHostQuotaConfiguration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ProviderHostQuotaConfiguration** tiene estas propiedades.

<dl> <dt>

**HandlesPerHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número de identificadores de objetos de kernel que puede tener cada host.

</dd> <dt>

**MemoryAllHosts**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Cantidad combinada de memoria privada en bytes que pueden tener todos los hosts.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MemoryPerHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Cantidad de memoria privada que se puede almacenar en cada host.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ProcessLimitAllHosts**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número total de procesos de host que se pueden ejecutar simultáneamente.

</dd> <dt>

**ThreadsPerHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número de subprocesos que pertenecen a un host.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se pueden cambiar las propiedades que representan los límites pero, dado que la clase es un singleton, todos los hosts del proveedor comparten los mismos límites.

Los parámetros siguientes se utilizan al configurar los límites de objetos de trabajo para el objeto de trabajo de host:

-   **MemoryAllHosts**
-   **MemoryPerHost**
-   **ProcessLimitAllHosts**
-   **ThreadsPerHost**

Los sondeos del proceso de host controlan el uso y salen del proceso si se infringe la cuota **HandlesPerHost** . Los cambios en estos valores surten efecto después de reiniciar el equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

