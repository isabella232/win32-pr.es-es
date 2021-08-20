---
description: Representa la configuración de migración para migrar un sistema virtual y el almacenamiento asociado a un sistema virtual.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ad7fd5cea4518d08810acce702ea1e29b7b70d13c5440f17610566a6348d3e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994158"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>Clase Msvm \_ VirtualSystemMigrationSettingData

Representa la configuración de migración para migrar un sistema virtual y el almacenamiento asociado a un sistema virtual.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualSystemMigrationSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemMigrationSettingData** tiene estas propiedades.

<dl> <dt>

**AllowOverwriteExistingFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Permita que la operación de migración de almacenamiento sobrescriba los archivos .vhdx existentes.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703.

 

</dd> <dt>

**AvoidRemovingVHDs**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No quite ningún VHD durante la migración, es decir, vhds en el origen en correctoy VHD en el destino en caso de error.

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

**Ancho de banda**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el ancho de banda asignado o solicitado para una operación de migración del sistema virtual. La propiedad **BandwidthUnit** especifica las unidades de ancho de banda. Dentro de una migración, un valor de 0 indica el ancho de banda predeterminado. De lo contrario, un valor de 0 indica que no se admiten anchos de banda.

**El ancho** **de banda y la** prioridad se pueden usar juntos. Los procesos de migración que tienen el valor de prioridad más alta comparten el ancho de banda disponible en función del ancho de banda solicitado. Si este conjunto de procesos consume no todo el ancho de banda, los procesos de migración con la siguiente prioridad igual inferior comparten el ancho de banda restante. Si aún queda más ancho de banda, se tienen en cuenta los procesos de migración con la siguiente prioridad igual menor, etc.

Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las unidades usadas por la **propiedad Bandwidth.** El valor de esta propiedad debe ser un valor legal del calificador Unidades de programación tal como se define en el Apéndice C.1 de DSP0004 V2.4 o posterior.

Si el valor de esta propiedad es "percent", el valor de la propiedad **Bandwidth** debe estar entre 0 y 100, con valores más altos que indican un ancho de banda mayor. Un valor de 100 indica el ancho de banda total disponible para realizar operaciones de migración del sistema virtual. Los valores entre 1 y 100 deben correlacionarse linealmente con el intervalo de ancho de banda disponible. Por ejemplo, un valor de 50 debe solicitar la mitad del ancho de banda disponible.

Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**CancelIfBlackoutThresholdExceeded**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cancela la migración si se supera el tiempo de umbral de bloqueo.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CPUCappingMagnitude**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")
</dt> </dl>

Grado de límite de CPU durante la migración.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Normal** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Bajo** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Alto** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DestinationIPAddressList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Será NULL **para la migración** de almacenamiento. Para la migración del sistema virtual, puede contener una lista de direcciones IP del host de destino.

</dd> <dt>

**DestinationPlannedVirtualSystemId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si existe una máquina virtual planeada en el destino de la migración, esta propiedad se establecerá en el GUID de la máquina virtual planeada de destino a la que la máquina virtual debe migrarse. Esto es útil para los casos en los que un usuario ha creado una máquina virtual planeada en el destino, junto con la configuración de recursos, y quiere que una máquina virtual del origen se migre a esta máquina virtual planeada.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se debe comprimir el tráfico de migración en vivo. **True** indica que se debe comprimir; en caso **contrario, False**.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")
</dt> </dl>

Especifica el tipo de operación de migración que se va a realizar. Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)


</dt> <dd>

Migra el sistema virtual al host de destino.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)


</dt> <dd>

Migra solo los recursos de almacenamiento del sistema virtual.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)


</dt> <dd>

Con la configuración del sistema virtual, crea un sistema virtual planeado en el host de destino.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)


</dt> <dd>

Migra el sistema virtual y su almacenamiento al host de destino.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)


</dt> <dd>

Realiza una comprobación de la capacidad de migración de recursos de almacenamiento del sistema virtual en el host de destino.

</dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de transporte que se va a aplicar si el valor de **TransportType** es 1 (Other). Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica una importancia de migración relativa, que el sistema de migración puede usar para ordenar o dar preferencia entre varias solicitudes de migración pendientes. Cuanto menor sea el valor, mayor será la prioridad. Dentro de una migración, un valor de 0 indica la prioridad predeterminada. De lo contrario, un valor de 0 indica que no se admiten prioridades.

Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**RemoveSourceUnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Quite los discos duros virtuales no administrados de origen.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

**RetainVhdCopiesOnSource**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Para una migración de almacenamiento, especifica si los VHD de solo lectura del host de origen deben quitarse una vez completada la migración.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")
</dt> </dl>

Especifica el tipo de transporte que se va a aplicar para una operación de migración del sistema virtual. Esta propiedad se hereda de **CIM \_ VirtualSystemMigrationSettingData**.

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

**Reservado por** el proveedor (32768.).


</dt> <dd></dd> </dl>

Para la migración en vivo, esta propiedad especifica el tipo de transporte que se usará para transferir el estado del sistema virtual al host de destino. Los valores admitidos son:

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Indica el tipo de transporte TCP.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Indica que el tipo de transporte para transferir el estado de la máquina virtual es SMB.

</dd> </dl>

</dd> <dt>

**UnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm \_ MoveUnmanagedVhd")
</dt> </dl>

Matriz de instancias [**insertadas de Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) que contienen información de discos duros virtuales no administrados.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

