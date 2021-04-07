---
description: La versión 2 del proveedor WMI de Hyper-V es la nueva para Windows 8 y Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Novedades en el proveedor de WMI de Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce222fd18955e88b9e33e1b706cf81ef5a806917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910998"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Novedades del proveedor WMI de Hyper-V

La versión 2 del proveedor WMI de Hyper-V es la nueva para Windows 8 y Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

Nuevas clases:

-   [**\_Batería MSVM**](msvm-battery.md)
-   [**MSVM \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**MSVM \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Propiedades nuevas:

-   [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md): **ExportedGuestStateFilePaths**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode** y **DefaultQueueVrssMinQueuePairs**
-   [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading**, **VrssExcludePrimaryProcessor**, **VrssQueueSchedulingModes** y **VrssMinQueuePairs**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **aligne**, **PmemAddressAbstractionType** y **IsPmemCompatible**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **DisableDifferentialOfIgnoredStorage** y **ExcludedVirtualHardDisks**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **HypervisorRootSchedulerEnabled**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **CPUCappingMagnitude** y **CancelIfBlackoutThresholdExceeded**
-   [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md): **ExportedGuestStateFilePath**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **Architecture**, **AutomaticSnapshotsEnabled**, **IsAutomaticSnapshot**, **GuestStateFile** y **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10, versión 1703

Nuevas clases:

-   [**MSVM \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**MSVM \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**MSVM \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**MSVM \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**MSVM \_ GpuPartition**](msvm-gpupartition.md)
-   [**MSVM \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**MSVM \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**MSVM \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**MSVM \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**MSVM \_ PciExpress**](msvm-pciexpress.md)
-   [**MSVM \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**MSVM ( \_ SecurityElement)**](msvm-securityelement.md)
-   [**MSVM \_ SecurityService**](msvm-securityservice.md)
-   [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**MSVM \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**MSVM \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Clases quitadas:

-   [**MSVM \_ TPMSettingData**](msvm-tpmsettingdata.md)

Nuevos métodos:

-   [**MSVM \_ Clase CollectionSnapshotService**](msvm-collectionsnapshotservice.md) : [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**MSVM \_ Clase VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) : [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)y [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**MSVM \_ Clase VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) : [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Propiedades nuevas:

-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVmmqQueuePairs**, **DefaultQueueVmmqEnabled** y **DefaultQueueVrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VmmqQueuePairs**, **VmmqEnabled** y **VrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **VmmqQueuePairs**, **VmmqEnabled** y **VrssEnabled**
-   [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md): **LastResourceMoveTime**
-   [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md): **DisableHostKVPItems**
-   [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md): **SgxSize** y **SgxEnabled**
-   [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md): **CompatibleForVirtualization** y **DriverModelVersion**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **HwThreadsPerCoreCpuGroupId**, **HideHypervisorPresent** y **ExposeVirtualizationExtensions**
-   [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md): **SupportStatement**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **WriteHardeningMethod**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **blindado**
-   [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md): **AllowPacketDirect**
-   [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md): **LastApplyConsistencyLevel**, **LastApplyVirtualMachineIds**, **LastApplyTime**, **FailedOverReplicationType**, **ReplicationMode** y **ReplicationState**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **ExportForLiveMigration**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **AvoidRemovingVHDs** y **AllowOverwriteExistingFile**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **HighMmioGapSize**
-   [**MSVM \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md): **GuestBackupType**

Propiedades quitadas:

-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **ParentPackage**

## <a name="windows-10"></a>Windows 10

Nuevas clases:

-   [**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
-   [**\_Colección CIM**](cim-collection.md)
-   [**CollectionOfMSEs de CIM \_**](cim-collectionofmses.md)
-   [**\_ELEMENTVIEW CIM**](cim-elementview.md)
-   [**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
-   [**TPM de CIM \_**](cim-tpm.md)
-   [**\_Vista CIM**](cim-view.md)
-   [**MSVM \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**MSVM \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**MSVM \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**MSVM \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**MSVM \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**MSVM \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**MSVM \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**MSVM \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**MSVM \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**MSVM \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**MSVM \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**MSVM \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**MSVM \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**MSVM \_ ManagementCollection**](msvm-managementcollection.md)
-   [**MSVM \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md)
-   [**MSVM \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**MSVM \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**MSVM \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**MSVM \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**MSVM \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md)
-   [**MSVM \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**MSVM \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**MSVM \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**MSVM \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**\_TPM MSVM**](msvm-tpm.md)
-   [**MSVM \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**MSVM \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**MSVM \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**MSVM \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**MSVM \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**MSVM \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**MSVM \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**MSVM \_ VssService**](msvm-vssservice.md)

Clase quitada:

-   [**MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**MSVM \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Propiedades nuevas:

-   [**MSVM \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md): **LastKnownSwitchName** y **CompartmentGuid**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **PacketDirectInUse**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**MSVM \_ EthernetSwitchPortSecuritySettingData**](msvm-ethernetswitchportsecuritysettingdata.md): **EnableFixSpeed10G** y **Reserved**
-   [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md): **DefaultEnabledStatePolicy**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **EnableHostResourceProtection**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **StorageQoSPolicyID**, **CachingMode** y **SnapshotId**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **InstanceID**, **version**, **ThumbnailImageHeight**, **ThumbnailImageWidth** y **HostComputerSystemName**
-   [**MSVM \_ Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md): **VRAMSizeBytes**
-   [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md): **TeamingEnabled** y **PacketDirectEnabled**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **ParentTimestamp** y **ParentIdentifier**
-   [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md): **marca** de tiempo
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **BackupIntent** y **DifferentialBackupBase**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **DefaultVirtualHardDiskCachingMode**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **RemoveSourceUnmanagedVhds** y **UnmanagedVhds**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **UserSnapshotType**, **GuestControlledCacheTypes**, **LockOnDisconnect**, **ParentPackage**, **AutomaticCriticalErrorActionTimeout**, **AutomaticCriticalErrorAction**, **ConsoleMode** y **SecureBootTemplateId**

Nuevos métodos:

-   [**MSVM \_ Clase ImageManagementService**](msvm-imagemanagementservice.md) : [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)y [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**MSVM \_ Clase ShutdownComponent**](msvm-shutdowncomponent.md) : [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md): [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)y [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**MSVM \_ Clase VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) : [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 y Windows Server 2012 R2:

Windows 8.1 y Windows Server 2012 R2 incluyen nuevas funciones para la versión 2 del proveedor WMI de Hyper-V.

-   Las propiedades **IOPSAllocationUnits**, **IOPSLimit**, **IOPSReservation** y **PersistentReservationsSupported** se han agregado a la clase [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .
-   La propiedad **VirtualDiskId** se ha agregado a la [**clase \_ VirtualHardDiskSettingData de MSVM**](msvm-virtualharddisksettingdata.md) .
-   Se ha agregado información sobre QoS de almacenamiento a la propiedad **OperationalStatus** de las clases [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) y [**MSVM \_ ResourcePool**](msvm-resourcepool.md) .
-   [**MSVM \_ Clase StorageAlert**](msvm-storagealert.md)
-   La propiedad **ClusterMonitored** se ha agregado a las clases [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) y [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) .
-   Las propiedades **EnableCompression** y **EnableSmbTransport** se han agregado a la [**clase \_ VirtualSystemMigrationServiceSettingData de MSVM**](msvm-virtualsystemmigrationservicesettingdata.md) .
-   La propiedad **EnableCompression** se ha agregado a la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) . La propiedad **TransportType** incluye información sobre la migración en vivo.
-   [**MSVM \_ Clase CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
-   [**MSVM \_ Clase CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)
-   [**MSVM \_ Clase GuestFileService**](msvm-guestfileservice.md)
-   [**MSVM \_ Clase GuestService**](msvm-guestservice.md)
-   [**MSVM \_ Clase GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
-   [**MSVM \_ Clase GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**MSVM \_ Clase RegisteredGuestService**](msvm-registeredguestservice.md)
-   La propiedad **EnhancedSessionModeEnabled** se ha agregado a la [**clase \_ VirtualSystemManagementServiceSettingData de MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) .
-   La propiedad **EnhancedModeState** y el método [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) se han agregado a la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .
-   Se han agregado las propiedades **BootSourceOrder**, **LowMmioGapSize**, **NetworkBootPreferredProtocol**, **PauseAfterBootFailure** , **SecureBootEnabled** y **VirtualSystemSubType** a la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .
-   [**MSVM \_ Clase BootSourceSettingData**](msvm-bootsourcesettingdata.md)
-   [**MSVM \_ Clase BootSourceComponent**](msvm-bootsourcecomponent.md)
-   [**MSVM \_ Clase LogicalIdentity**](msvm-logicalidentity.md)
-   [**MSVM \_ Clase CompatibilityVector**](msvm-compatibilityvector.md)
-   El método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) se ha agregado a la [**clase \_ VirtualSystemMigrationService de MSVM**](msvm-virtualsystemmigrationservice.md) .
-   Se han agregado las propiedades **ReplicationStateEx**, **ReplicationHealthEx**, **EnhancedSessionModeState**, **VirtualSwitchNames** y **VirtualSystemSubType** a la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Las propiedades **ReplicationState** y **ReplicationHealth** están en desuso y se reemplazan por las propiedades **ReplicationStateEx** y **ReplicationHealthEx** .
-   La propiedad **PnpDevicePath** se ha agregado a la [**clase \_ MountedStorageImage de MSVM**](msvm-mountedstorageimage.md) .
-   Se han agregado las propiedades **AllowedHashAlgorithms** y **TrustedIssuerCertificateHashes** a la clase [**MSVM \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) .

Windows 8.1 y Windows Server 2012 R2 incluyen nuevas funcionalidades para la replicación de máquinas virtuales y la recuperación de la conmutación por error.

-   [**MSVM \_ Clase ReplicationProvider**](msvm-replicationprovider.md)
-   [**MSVM \_ Clase ReplicationRelationship**](msvm-replicationrelationship.md)
-   Los métodos [**ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**InitiateFailback**](initiatefailback-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)y [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) se han agregado a la clase [**MSVM \_ ReplicationService**](msvm-replicationservice.md) . Los métodos **GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** y **ResetReplicationStatisticsEx** reemplazan a los métodos [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)y [**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md) .
-   La clase [**MSVM \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md) muestra una asociación entre una máquina virtual y muchas relaciones de replicación.
-   Se han agregado las propiedades **AdditionalSettings** y **ReplicationProvider** a la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) .
-   Se ha agregado información sobre el proveedor de host a host a los métodos [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) y [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) de la clase [**MSVM \_ ReplicationService**](msvm-replicationservice.md) .
-   El método [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) se ha agregado a la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) y reemplaza el método [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) . La propiedad **InstanceID** ahora puede indicar la replicación extendida. Para obtener más información acerca de la replicación extendida, consulte [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   [**MSVM \_**](msvm-replicationsettingdata.md) Las instancias [**de \_ ReplicationRelationship**](msvm-replicationrelationship.md) de ReplicationSettingData y Msvm tienen una relación 1:1 que se puede representar con una asociación [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

    | [**MSVM \_**](msvm-settingsdefinestate.md) Nombre de la propiedad SettingsDefineState | Value                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | Representa el [**objeto \_ ReplicationRelationship de MSVM**](msvm-replicationrelationship.md)          |
    | **SettingData**                                                             | Representa el objeto [**\_ ReplicationSettingData de MSVM**](msvm-replicationsettingdata.md) asociado |

    

     

-   [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) puede diferenciar entre las instancias de configuración de la relación de replicación basadas en la propiedad **InstanceID** o **ReplicationRelationship** . Por lo tanto, estos métodos que se ocupan de una relación única no cambiaron su firma:

    -   [**MSVM \_ ReplicationService:: CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: Resync**](resynchronize-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: StartReplication**](startreplication-msvm-replicationservice.md)

-   Aunque puede usar [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)y [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) siempre para la relación principal, se recomienda que use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)y [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) , ya que pueden procesar la relación de replicación principal y la extendida. Para obtener más información acerca de la replicación extendida, consulte [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   Aunque estas propiedades de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) continúan indicando el estado de la relación de replicación principal, en su lugar, use estas propiedades de un objeto [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para determinar el estado actual de la relación de replicación principal y extendida.

    | Nombre de propiedad                                | Tipo        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO) |
    | **ReplicationHealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | DateTime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | DateTime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 



