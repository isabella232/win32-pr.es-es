---
description: Define la configuración para la migración del sistema virtual administrada por una instancia de la \_ clase VirtualSystemMigrationService de CIM.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813387"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>\_Clase VirtualSystemMigrationSettingData de CIM

Define la configuración para la migración del sistema virtual administrada por una instancia de la clase [**\_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) .

## <a name="syntax"></a>Sintaxis

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ VirtualSystemMigrationSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ VirtualSystemMigrationSettingData** tiene estas propiedades.

<dl> <dt>

**Ancho de banda**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

Ancho de banda asignado a o solicitado para una operación de migración del sistema virtual. "0" es el ancho de banda predeterminado para las solicitudes de migración.

Las propiedades de **ancho de banda** y **prioridad** se pueden usar conjuntamente. Los procesos de migración que tienen los valores de **prioridad** más altos comparten el ancho de banda disponible según el ancho de banda solicitado. Si este conjunto de procesos no consume todo el ancho de banda, los procesos de migración con los valores de **prioridad** inferior siguientes comparten el ancho de banda restante. Si se mantiene más ancho de banda, se tienen en cuenta los procesos de migración con los siguientes valores de **prioridad** inferiores.

La unidad usada en la propiedad **ancho de banda** se especifica mediante el valor de la propiedad **BandwidthUnit** .

Si el valor de la propiedad **BandwidthUnit** es "Percent", se aplican las siguientes reglas:

-   El valor de la propiedad de **ancho de banda** debe estar entre "0" y "100", con valores más altos que indiquen un ancho de banda mayor.
-   Un valor de "100" indica todo el ancho de banda disponible para realizar operaciones de migración del sistema virtual.
-   Los valores entre "1" y "100" se correlacionan linealmente con el intervalo de ancho de banda disponible. Por ejemplo, un valor de 50 solicita la mitad del ancho de banda disponible.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Ancho de banda**"), **IsPUnit**
</dt> </dl>

Unidad usada por la propiedad de **ancho de banda** . El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación definido en el Apéndice C. 1 de DSP0004 V 2.4 o posterior.

> [!Note]  
> Los perfiles como DMTF DSP1081 definen cómo los clientes pueden detectar el conjunto de unidades admitidas por una implementación, y intervalos e incrementos para los valores de la propiedad de **ancho de banda** .

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de operación de migración que se va a realizar.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Live** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**Reanudar** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Reiniciar** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")
</dt> </dl>

Tipo de transporte que se va a aplicar si el valor de **TransportType** es "1" (otro).

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Importancia de la migración relativa que la implementación de la migración del sistema virtual puede usar para ordenar o asignar preferencias entre varias solicitudes de migración pendientes. Cuanto menor sea el valor, mayor será la prioridad. "0" es el ancho de banda predeterminado para las solicitudes de migración.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

El tipo de transporte que se va a aplicar a una operación de migración del sistema virtual.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**Ssh** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS STRICT** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32768...)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> </dl>

 

