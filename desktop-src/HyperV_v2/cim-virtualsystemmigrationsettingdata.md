---
description: Define la configuración de la migración del sistema virtual administrada por una instancia de la clase \_ CIM VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData clase
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
ms.openlocfilehash: 24a48877a4195d17398457912314186d0220ace8016a4c9cc3edd3e06c378ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950680"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>Cim \_ VirtualSystemMigrationSettingData (clase)

Define la configuración de la migración del sistema virtual administrada por una instancia de la clase [**\_ CIM VirtualSystemMigrationService.**](cim-virtualsystemmigrationservice.md)

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

La **clase CIM \_ VirtualSystemMigrationSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM VirtualSystemMigrationSettingData** tiene estas propiedades.

<dl> <dt>

**Ancho de banda**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

Ancho de banda asignado o solicitado para una operación de migración del sistema virtual. "0" es el ancho de banda predeterminado para las solicitudes de migración.

Las **propiedades Ancho de** banda **y** Prioridad se pueden usar juntos. Los procesos de migración que tienen los valores de **prioridad iguales más** altos comparten el ancho de banda disponible en función del ancho de banda solicitado. Si este conjunto de procesos no consume todo el ancho de banda, los procesos de migración con los siguientes valores de **prioridad** igual inferior comparten el ancho de banda restante. Si queda más ancho de banda, se tienen en cuenta los procesos de migración con los siguientes valores **de prioridad** iguales inferiores.

El valor  de la propiedad BandwidthUnit especifica la unidad usada en **la propiedad BandwidthUnit.**

Si el valor de la **propiedad BandwidthUnit** es "percent", se aplican las reglas siguientes:

-   El valor de la **propiedad Bandwidth** debe estar entre "0" y "100", con valores más altos que indican un ancho de banda mayor.
-   El valor "100" indica todo el ancho de banda disponible para realizar operaciones de migración del sistema virtual.
-   Los valores entre "1" y "100" se correlacionan linealmente con el intervalo de ancho de banda disponible. Por ejemplo, un valor de 50 solicitudes la mitad del ancho de banda disponible.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Ancho de** banda "), **IsPUnit**
</dt> </dl>

Unidad utilizada por la propiedad **Bandwidth.** El valor de esta propiedad debe ser un valor legal del calificador Unidades de programación definido en el Apéndice C.1 de DSP0004 V2.4 o posterior.

> [!Note]  
> Los perfiles como DMTF DSP1081 definen cómo los clientes pueden detectar el conjunto de unidades compatibles con una implementación, así como intervalos e incrementos para los valores de la propiedad **Bandwidth.**

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de operación de migración que se realizará.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La importancia relativa de la migración que la implementación de migración del sistema virtual puede usar para ordenar o asignar preferencias entre varias solicitudes de migración pendientes. Cuanto menor sea el valor, mayor será la prioridad. "0" es el ancho de banda predeterminado para las solicitudes de migración.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

Tipo de transporte que se aplicará a una operación de migración del sistema virtual.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


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

**Vendor Reserved** (32768.).


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

