---
description: Representa la configuración específica de la replicación para una máquina virtual.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 90e16e70f7b5bd0a075ffdef54cf0c591719d4993031f3abee19dd8186ec5996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148258"
---
# <a name="msvm_replicationsettingdata-class"></a>Clase Msvm \_ ReplicationSettingData

Representa la configuración específica de la replicación para una máquina virtual. El cliente pasa una instancia de esta clase a [**Msvm \_ ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) para crear una relación de replicación. El cliente no puede cambiar directamente los valores de ninguna de las propiedades de esta clase; debe llamar al método [**Msvm \_ ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) para cambiar los valores. Cada relación de replicación tiene una única instancia de configuración.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a>Miembros

La **clase \_ ReplicationSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ReplicationSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**AdditionalSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración de replicación adicional que puede usar el proveedor de puntos de conexión.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**ApplicationConsistentSnapshotInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo entre instantáneas coherentes con la aplicación, especificadas en horas. Los valores válidos van de 1 hora a 12 horas.

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Defina el modo de autenticación utilizado para conectarse al servidor de recuperación.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticación Kerberos** (1)


</dt> <dd>

Autenticación Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)


</dt> <dd>

Autenticación basada en certificados.

</dd> </dl>

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tiempo de retraso antes de que la máquina virtual se inicie automáticamente. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutoResynchronizeEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si las operaciones de resincronización se desencadenan automáticamente cuando se produce un error de replicación debido a errores de alimentación y hardware. Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd.**

El valor predeterminado es **False**.

</dd> <dt>

**AutoResynchronizeIntervalEnd**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora de finalización de las operaciones de resincronización automáticas que se van a desencadenar. Este valor está en hora local. El valor predeterminado es 06:00 (6:00 a. m.).

Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd.**

También se pueden programar operaciones de resincronización para que se desencadene durante el siguiente intervalo.

</dd> <dt>

**AutoResynchronizeIntervalStart**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora de inicio de las operaciones de resincronización automáticas que se van a desencadenar. Este valor está en hora local. El valor predeterminado es 18:30 (6:30 p. m.).

Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd.**

También se pueden programar operaciones de resincronización para que se desencadene durante el siguiente intervalo.

</dd> <dt>

**BypassProxyServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se debe omitir el servidor proxy al conectarse a un servidor de recuperación.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Replication Configuración".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Huella digital del certificado que se va a usar **cuando la propiedad AuthenticationType** sea la autenticación basada en certificados.

</dd> <dt>

**CompressionEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si los datos de replicación se comprimirán mientras se envían al servidor de recuperación.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa y nombre de archivo de un archivo donde se almacena información sobre la configuración de la máquina virtual. Esta ruta de acceso es relativa a la **propiedad ConfigurationDataRoot.** Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual. Si este objeto representa la configuración actual de la máquina virtual, este valor sería la hora a la que se creó el sistema. Si este objeto representa la configuración de instantáneas de la máquina virtual, este valor sería la hora a la que se tomó la instantánea. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Virtual Machine Replication Configuración Data".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))y se establece en el nombre para mostrar de la máquina virtual.

</dd> <dt>

**EnableWriteOrderPreservationAcrossDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor")
</dt> </dl>

Especifica si todos los discos duros virtuales de replicación de la máquina virtual se replican en el mismo momento dado. Esto garantiza que la replicación respeta el orden de escritura de las aplicaciones en la máquina virtual.

**Windows 8.1:** A partir Windows 8.1 y Windows Server 2012 R2, esta propiedad está en desuso y siempre se establece en **TRUE.**

</dd> <dt>

**IncludedDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Lista de discos duros virtuales (VHD) conectados al sistema que replicará el motor de replicación. Se trata de una matriz de cadenas, cada una de las que contiene el **InstanceID** de [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) que representa el VHD.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)). Por Windows 8, siempre se establece en "Microsoft:*VIRTUAL Machine GUID* \\ HVR". Por Windows 8.1, se establece en "Microsoft:*Virtual Machine GUID* \\ HVR<\\ 0/1>". En el Windows 8.1, 0 indica principal y 1 indica replicación extendida. Para obtener más información sobre la replicación extendida, vea [**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena la información de registro de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa y no se puede establecer.

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**PrimaryConnectionPoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre del punto de conexión principal. En el caso de un clúster principal, este es el nombre CAP del agente. En el caso de un servidor principal independiente, este es el nombre del sistema host.

</dd> <dt>

**PrimaryHostSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de dominio completo del sistema host principal que hospeda la máquina virtual.

</dd> <dt>

**RecoveryConnectionPoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre del punto de conexión de recuperación. En el caso de un clúster de recuperación, este es el nombre CAP del agente. En el caso de un servidor de recuperación independiente, este es el nombre del sistema host.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa de un archivo donde se almacena la información relacionada con la recuperación de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**RecoveryHistory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de instantáneas de recuperación que se almacenarán en el servidor de recuperación. Los valores válidos van de 0 a 24.

</dd> <dt>

**RecoveryHostSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de dominio completo del sistema host de recuperación que hospeda la máquina virtual.

</dd> <dt>

**RecoveryServerPortNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de puerto del servidor de recuperación que se usará al realizar una conexión segura para la replicación.

</dd> <dt>

**ReplicateHostKvpItems**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se debe replicar [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s solo de host desde la máquina virtual principal a la máquina virtual de recuperación.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de replicación de una relación de replicación en segundos. Los valores válidos son:

30

300

900

El valor predeterminado es 300 segundos.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**ReplicationProvider**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso a la instancia de la clase [**\_ ReplicationProvider de Msvm**](msvm-replicationprovider.md) que identifica el punto de conexión del proveedor de replicación.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**RootCertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Huella digital del certificado raíz del certificado en uso cuando **AuthenticationType** es 2 (autorización basada en certificado).

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre las instantáneas de máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre la máquina virtual relacionada con la suspensión. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del objeto [**\_ ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen los datos de esta configuración. Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de máquina virtual que representan los datos de configuración. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))y siempre se establece en "Microsoft:Hyper-V:Replica".

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

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

