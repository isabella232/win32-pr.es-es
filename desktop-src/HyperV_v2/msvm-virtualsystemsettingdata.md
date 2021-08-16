---
description: Representa la configuración específica de la virtualización para una máquina virtual.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fb57c7b96a6e2cd1839f4d830074bb69d742aef688325a37d61b67589d026436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147898"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>Clase Msvm \_ VirtualSystemSettingData

Representa la configuración específica de la virtualización para una máquina virtual.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualSystemSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemSettingData** tiene estas propiedades.

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cualquier información adicional proporcionada a la acción de recuperación. La acción de **AutomaticRecoveryAction** define el significado de esta propiedad. Si **AutomaticRecoveryAction** es 0 ("None") o 1 ("Restart"), este valor es **Null.** Si **AutomaticRecoveryAction** es 2 ("Revertir a instantánea"), esta es la ruta de acceso del objeto a una instantánea que se debe aplicar en caso de error del proceso de trabajo de la máquina virtual.

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**True** si los comandos SCSI del sistema operativo invitado se pasan a discos de paso a través; de lo contrario, **False**. Si **es True,** los comandos SCSI emitidos por el sistema operativo invitado para los discos de paso a través no se filtran. Se recomienda que el filtrado SCSI permanezca habilitado para las implementaciones de producción.

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si se permite la migración en vivo de una máquina virtual configurada con un adaptador de Canal de fibra virtual a un equipo de destino que no tenga rutas de acceso a los dispositivos Canal de fibra destino o que no tengan ninguna ruta de acceso reducida. Esta propiedad debe borrarse después de una migración en vivo.



| Value                                                                            | Significado                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | La máquina virtual no se puede migrar en vivo a un equipo de destino que no tenga rutas de acceso o reducidas a los dispositivos de destino Canal de fibra destino.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | La máquina virtual se puede migrar en vivo a un equipo de destino que puede no tener rutas de acceso o rutas de acceso reducidas al destino Canal de fibra dispositivos. El sistema operativo invitado puede perder la conectividad con el almacenamiento y puede comportarse de forma impredecible.<br/> |



 

</dd> <dt>

**Arquitectura**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La arquitectura de este sistema.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identifica la acción que se debe realizar en la máquina virtual cuando se produce un error crítico, como la desconexión del almacenamiento.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)


</dt> <dd>

No se realizará ninguna acción específica para condiciones de error críticas.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pausar reanudación** (1)


</dt> <dd>

Hace que la máquina virtual se pause y se reanude automáticamente cuando se resuelve la condición de error crítica.

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")
</dt> </dl>

Identifica la duración máxima durante la que **se realizará AutomaticCriticalErrorAction** para resolver el error crítico. Esto solo es aplicable cuando el valor de la **propiedad AutomaticCriticalErrorAction** no es 0 (None). Una vez que expire el tiempo de espera, la máquina virtual se apagará. El valor se redondeará al minuto más cercano. Un valor de 0 implica que la máquina virtual debe apagarse inmediatamente cuando encuentra una condición de error crítica.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual. Los errores en este caso significan un error que la plataforma host puede detectar, como una condición de estado de espera no ininterrumpida. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Puede ser uno de los siguientes valores.



| Value                                                                               | Significado                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Ninguno.<br/>               |
| <dl> <dt>3</dt> </dl>        | Restart. (Reiniciar)<br/>            |
| <dl> <dt>4</dt> </dl>        | Revertir a la instantánea.<br/> |
| <dl> <dt>5..32768</dt> </dl> | Reservado.<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se apaga el host. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Puede ser uno de los siguientes valores.



| Value                                                                               | Significado                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Apaga.<br/>   |
| <dl> <dt>3</dt> </dl>        | Guardar estado.<br/> |
| <dl> <dt>4</dt> </dl>        | Apagar.<br/>   |
| <dl> <dt>5..32768</dt> </dl> | Reservado.<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si esta máquina virtual debe tener habilitadas las instantáneas automáticas.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se inicia el host. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Puede ser uno de los siguientes valores.



| Value                                                                               | Significado                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Ninguno.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Reinicie si previamente está activo.<br/> |
| <dl> <dt>4</dt> </dl>        | Inicie siempre.<br/>                 |
| <dl> <dt>5..32768</dt> </dl> | Reservado.<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tiempo de retraso antes de que la máquina virtual se inicie automáticamente. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host. Un número inferior indica la activación anterior. Si una o varias configuraciones muestran el mismo valor, la secuencia depende de la implementación. Un valor de 0 indica que la secuencia depende de la implementación. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número de serie de la placa base de la máquina virtual.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador único global para el BIOS de la máquina virtual.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**True** si el BIOS establece la tecla de bloqueo num en on; **False** si el BIOS establece la tecla de bloqueo num en desactivada.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número de serie del BIOS de la máquina virtual.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Orden de arranque establecido en el BIOS de la máquina virtual. Esta propiedad es una matriz de valores, **BootOrder** 0 a \[ \] **BootOrder** \[ 3, ambos incluidos, donde cada valor indica un dispositivo desde el que \] arrancar. Cada uno de los 4 valores de la matriz debe establecerse y no debe ser igual que otro valor de la matriz. La máquina virtual intentará arrancar primero desde el dispositivo indicado por el primer valor dentro de la matriz. Si ese dispositivo no contiene un sector de arranque, la máquina virtual intentará arrancar desde el siguiente dispositivo especificado por la propiedad **BootOrder,** y así sucesivamente. Si ningún dispositivo especificado dentro de **BootOrder** contiene un sector de arranque, la máquina virtual no podrá arrancar. El valor predeterminado de una máquina virtual \[ es 0, 1, 2, 3 \] .

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquete** (0)


</dt> <dd>

La máquina virtual intentará arrancar desde el disquete dentro de la unidad de disquete.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

La máquina virtual intentará arrancar desde el primer disco de CD o DVD que se encuentra con un sector de arranque.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Unidad de disco duro ide** (2)


</dt> <dd>

La máquina virtual intentará arrancar desde la primera unidad de disco duro que se encuentra con un sector de arranque.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Arranque PXE** (3)


</dt> <dd>

La máquina virtual intentará arrancar PXE desde la red.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Unidad de disco duro SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (5..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El orden de origen de arranque de la máquina virtual.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

La etiqueta de recurso del chasis para la máquina virtual.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número de serie del chasis de la máquina virtual.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre la configuración de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa y nombre de archivo de un archivo donde se almacena información sobre la configuración de la máquina virtual. Esta ruta de acceso es relativa a la **propiedad ConfigurationDataRoot.** Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identifica el modo de consola de la máquina virtual.

> [!Note]  
> Esta propiedad se agregó en Windows 10 y Windows Server 2016.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valor** predeterminado (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual. Si este objeto representa la configuración actual de la máquina virtual, este valor sería la hora a la que se creó el sistema. Si este objeto representa la configuración de instantáneas de la máquina virtual, este valor sería la hora a la que se tomó la instantánea. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador de canal utilizado para depurar la máquina virtual mediante el depurador unificado.

</dd> <dt>

**DebugPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Puerto TCP/IP que se usa para depurar la máquina virtual mediante la depuración sintética.

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si la máquina virtual usa la depuración sintética. Puede ser uno de los siguientes valores.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Desactivado** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)


</dt> <dd>

Asignado automáticamente

</dd> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en uno de los siguientes valores.



| Value                                                                                                                  | Significado                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Configuración activa de la máquina virtual"</dt> </dl>   | Esta instancia hace referencia a una máquina virtual.<br/> |
| <dl> <dt>"Configuración de instantáneas para la máquina virtual"</dt> </dl> | Esta instancia hace referencia a una instantánea.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))y siempre se establece en el nombre para mostrar de la máquina. Este nombre no puede superar los 100 caracteres de longitud.

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica el tipo de transporte que se usará al conectarse a una sesión mejorada.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1803.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**Canalización de VMBus** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Socket de Hyper-V** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el invitado puede controlar los tipos de caché.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de archivo de un directorio donde se almacena información sobre el estado de tiempo de ejecución del invitado.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de archivo de un archivo donde se almacena información sobre el estado de tiempo de ejecución del invitado. Una ruta de acceso relativa se anexa al valor de la **propiedad GuestStateDataRoot.**

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El tamaño de la brecha de E/S alta (por encima de 4 GB) Memory-Mapped de E/S en MB

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703.

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si vsS Writer de Hyper-V admite la toma de copias de seguridad incrementales de esta máquina virtual.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se trata de una instantánea creada automáticamente para el usuario.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si la configuración tiene una referencia a un archivo de estado guardado; de lo contrario, **False**. Esto no indica la presencia de este tipo de archivo, solo que la configuración especifica uno.

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Bloquee la consola al desconectarse de vmconnect.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena la información de registro de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Configura el tamaño, en megabytes, de la primera brecha mmio para una máquina virtual (VM).

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

Intervalo: 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Determina si el protocolo preferido para el arranque PXE es IPv4 o IPv6.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notas proporcionadas por el usuario relacionadas con la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si esta instancia no representa un sistema basado en una instantánea de una máquina virtual, esta propiedad es **Null.** De lo contrario, la propiedad contiene la ruta de acceso del objeto **Msvm \_ VirtualSystemSettingData** en el que se basa esta instancia. Al crear una jerarquía de árbol de instantáneas para la máquina virtual, esta propiedad hace referencia al objeto del que se deriva la instancia actual (la instancia actual es el nodo secundario y el objeto al que se hace referencia en esta propiedad es el nodo primario).

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si este sistema es un contenedor, la ruta de acceso al containerPackage de Msvm \_ desde el que se basa este sistema.

> [!Note]  
> Se ha agregado en Windows 10; se quitó Windows 10, versión 1703.

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el BIOS se detiene después de cada error de entrada de arranque a la espera de que el usuario presione una tecla. **True** si el BIOS se detiene; de lo contrario, **False**.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa de un archivo donde se almacena la información relacionada con la recuperación de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el arranque seguro está habilitado para la máquina virtual (VM). **True** si está habilitado; de lo contrario, **False**.

> [!Note]  
> El arranque seguro solo se puede habilitar para máquinas virtuales de generación 2.

 

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador único global de la plantilla de valores intiales de variables relacionadas con el arranque seguro de UEFI.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre las instantáneas de máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre la máquina virtual relacionada con la suspensión. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**UserSnapshotType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica el tipo de instantánea definido por el usuario.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (2)


</dt> <dd>

Deshabilite la creación de cualquier instantánea.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)


</dt> <dd>

Instantánea coherente con los datos para su uso en el entorno de producción. Realiza una instantánea con el estado de la aplicación cuando la capacidad de crear una instantánea coherente con los datos no está disponible.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)


</dt> <dd>

Instantánea coherente con los datos para su uso en el entorno de producción. No crea una instantánea con el estado de la aplicación si no es posible crear una instantánea coherente con los datos.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (5)


</dt> <dd>

Instantánea que contiene información de memoria y dispositivo con fines de prueba y desarrollo.

</dd> </dl>

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de la máquina virtual en un formato de "major.minor", por ejemplo, "2.0".

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")
</dt> </dl>

**True** si los nodos de acceso a memoria no uniforme (NUMA) virtuales se proyectan en la máquina virtual; **False** si la máquina virtual tendrá un único nodo. Si **es True,** el número de nodos NUMA virtuales proyectados en la máquina virtual se determina a partir de los valores de las propiedades [**\_ Msvm ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) y [**Msvm \_ MemorySettingData.MaxMemoryBlocksPerNumaNode.**](msvm-memorysettingdata.md)

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Nombre del objeto [**\_ ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen los datos de esta configuración. Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los valores válidos para esta propiedad son Microsoft:Hyper-V:SubType:1 y Microsoft:Hyper-V:SubType:2. Una máquina virtual de generación 1 es el subtipo 1. Una máquina virtual de generación 2 es el subtipo 2.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de máquina virtual que representan los datos de configuración. Esta propiedad se hereda de la [**clase \_ CIM VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85)) Este será uno de los siguientes valores.



| Value                                                                                                                                 | Significado                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft:Hyper-V:System:Realized"</dt> </dl>                        | Una máquina virtual realizada.<br/>               |
| <dl> <dt>"Microsoft:Hyper-V:System:Planned"</dt> </dl>                         | Una máquina virtual planeada.<br/>                |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt> </dl>                      | Instantánea de una máquina virtual realizada.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt> </dl>                      | Instantánea de una máquina virtual de recuperación.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt> </dl>                       | Instantánea de una máquina virtual planeada.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt> </dl>                       | Una instantánea que falta.<br/>                       |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt> </dl>              | Una instantánea de punto de replicación basada en tiempo.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt> </dl> | Una instantánea de punto de replicación de VSS.<br/>         |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt> </dl>       | Una instantánea de replicación planeada.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm VirtualSystemSettingData** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

