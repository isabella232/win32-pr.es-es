---
description: Proporciona información adicional que se va a usar con el método ExportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686598"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>MSVM \_ VirtualSystemExportSettingData (clase)

Proporciona información adicional que se va a usar con el método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) .

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemExportSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualSystemExportSettingData** tiene estas propiedades.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica el intento de uso de los conjuntos de copia de seguridad exportados.

> [!Note]  
> Esta propiedad se agregó en Windows 10 y Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)


</dt> <dd>

Todos los conjuntos de copia de seguridad completos y diferenciales exportados se conservarán tal como están.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)


</dt> <dd>

Los conjuntos de copia de seguridad completos y diferenciales exportados se combinarán para sintetizar los conjuntos de copia de seguridad completos.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica qué estado capturar si el destino de la exportación es una máquina virtual en ejecución.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)


</dt> <dd>

No se exportarán archivos de estado guardados para la máquina virtual en ejecución y se colocarán en un estado coherente con el bloqueo.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)


</dt> <dd>

Los archivos de estado guardados de la máquina virtual en ejecución se exportarán junto con la configuración de la máquina virtual.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)


</dt> <dd>

Se exportará el estado coherente con la aplicación de la máquina virtual en ejecución.

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica qué instantáneas se van a exportar con la máquina virtual.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)


</dt> <dd>

Todas las instantáneas se exportarán con la máquina virtual.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)


</dt> <dd>

No se exportará ninguna instantánea con la máquina virtual.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)


</dt> <dd>

Las instantáneas identificadas por la propiedad **SnapshotVirtualSystem** se exportarán con la máquina virtual. Se omiten las propiedades **CopyVmStorage** y **CopyVmRuntimeInformation** , el almacenamiento y la información en tiempo de ejecución se exportan con la máquina virtual y los discos de diferenciación de VHD se combinarán en un nuevo VHD.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)


</dt> <dd>

La instantánea identificada por la propiedad **SnapshotVirtualSystem** se exportará con el fin de realizar una copia de seguridad de la máquina virtual. La configuración exportada usará el identificador de la máquina virtual.

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la información de tiempo de ejecución de la máquina virtual se copiará cuando se exporte la máquina virtual.



| Value                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Se copiará la información en tiempo de ejecución de la máquina virtual.<br/>     |
| <dl> <dt>**False**</dt> </dl> | No se copiará la información en tiempo de ejecución de la máquina virtual.<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el almacenamiento de la máquina virtual se copiará cuando se exporte la máquina virtual.



| Value                                                                                | Significado                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Se copiará el almacenamiento de la máquina virtual.<br/>     |
| <dl> <dt>**False**</dt> </dl> | No se copiará el almacenamiento de la máquina virtual.<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si se creará un subdirectorio con el nombre de la máquina virtual cuando se exporte la máquina virtual.



| Value                                                                                | Significado                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Se creará un subdirectorio.<br/>     |
| <dl> <dt>**False**</dt> </dl> | No se creará un subdirectorio.<br/> |



 

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Base para la exportación diferencial. Se trata de una ruta de acceso a una instancia de [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia o la ruta de acceso a una instancia de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea que se va a usar como base para la exportación diferencial. Si la propiedad **CopySnapshotConfiguration** no está establecida en 3 (**ExportOneSnapshotForBackup**), se omite esta propiedad.

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si se crearán discos de diferenciación o no para el almacenamiento omitido durante la exportación. De forma predeterminada, se establece en false, lo que significa que se crean discos de diferenciación para el almacenamiento que no se va a copiar en el destino de exportación.

> [!Note]  
> Agregado en Windows 10, versión 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de esta instancia. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de identificadores de instancia de [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) que representan los discos duros virtuales que se solicitan que se excluyan de la operación de exportación. Si al menos uno de los identificadores proporcionados no es un disco duro virtual conectado válido, se producirá un error en la operación.

Los discos duros virtuales a los que hace referencia esta propiedad pueden ser de la máquina virtual o de cualquiera de sus instantáneas. No se admite la exclusión de discos duros virtuales cuando la propiedad **CopySnapshotConfiguration** está establecida en 0 (ExportAllSnapshots).

Tenga en cuenta que el identificador de instancia de RASD para los discos duros virtuales representa la ubicación a la que están conectados y, al excluir este identificador, se excluyen todos los discos duros virtuales conectados en esa ubicación a lo largo del árbol de instantáneas de la máquina virtual, independientemente de que sean realmente una cadena de disco duro virtual válida.

> [!Note]  
> Agregado en Windows 10, versión 1709.

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la máquina virtual exportada está pensada para usarse en la migración en vivo.

> [!Note]  
> Agregado en Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Dentro del ámbito del espacio de nombres de la creación de instancias, identifica de forma opaca y única una instancia de esta clase. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Ruta de acceso a una instancia de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea que se va a exportar con la máquina virtual. Si la propiedad **CopySnapshotConfiguration** no está establecida en 2 (ExportOneSnapshot), se omite esta propiedad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ VirtualSystemExportSettingData** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> <dt>

[Clases de administración de sistema virtual](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

