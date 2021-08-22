---
description: La versión 2 del proveedor WMI de Hyper-V es nueva para Windows 8 y Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Novedades del proveedor WMI de Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbaab65c08031c291eb11e8f865b77e256e5600deba060e0f8176ec8d13c3714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754935"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Novedades del proveedor WMI de Hyper-V

La versión 2 del proveedor WMI de Hyper-V es nueva para Windows 8 y Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

Nuevas clases:

-   [**Batería de \_ Msvm**](msvm-battery.md)
-   [**Msvm \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**Msvm \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Propiedades nuevas:

-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md): **ExportedGuestStateFilePaths**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor,** **DefaultQueueVrssQueueSchedulingMode** y **DefaultQueueVrssMinQueuePairs**
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData:**](msvm-ethernetswitchhardwareoffloadsettingdata.md) **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading,** **VrssExcludePrimaryProcessor,** **VrssQueueSchedulingModes** y **VrssMinQueuePairs**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **DataAlignment**, **PmemAddressAbstractionType** e **IsPmemCompatible**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **DisableDifferentialOfIgnoredStorage** y **ExcludedVirtualHardDisks**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **HypervisorRootSchedulerEnabled**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **CPUCappingMagnitude** y **CancelIfBlackoutThresholdExceeded**
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md): **ExportedGuestStateFilePath**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **Architecture**, **AutomaticSnapshotsEnabled**, **IsAutomaticSnapshot,** **GuestStateFile** y **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10, versión 1703

Nuevas clases:

-   [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**Colección de \_ MsvmReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**GpuPartition de Msvm \_**](msvm-gpupartition.md)
-   [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**Msvm \_ PciExpress**](msvm-pciexpress.md)
-   [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**SecurityElement de Msvm \_**](msvm-securityelement.md)
-   [**Msvm \_ SecurityService**](msvm-securityservice.md)
-   [**SecuritySettingData de Msvm \_**](msvm-securitysettingdata.md)
-   [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Clases quitadas:

-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)

Nuevos métodos:

-   [**Msvm \_ Clase CollectionSnapshotService:**](msvm-collectionsnapshotservice.md) [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**Msvm \_ Clase VirtualSystemManagementService:**](msvm-virtualsystemmanagementservice.md) [**AddSystemComponentSetting,**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md) [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)y [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**Msvm \_ Clase VirtualSystemReferencePointService:**](msvm-virtualsystemreferencepointservice.md) [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Propiedades nuevas:

-   [**Msvm \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVmmqQueuePairs**, **DefaultQueueVmmqEnabled** y **DefaultQueueVrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VmmqQueuePairs,** **VmmqEnabled** y **VrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **VmmqQueuePairs,** **VmmqEnabled** y **VrssEnabled**
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md): **LastResourceMoveTime**
-   [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md): **DisableHostKVPItems**
-   [**Msvm \_ MemorySettingData:**](msvm-memorysettingdata.md) **SgxSize** y **SgxEnabled**
-   [**Msvm \_ Physical3dGraphicsProcessor:**](msvm-physical3dgraphicsprocessor.md) **CompatibleForVirtualization** y **DriverModelVersion**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **HwThreadsPerCoreCpuGroupId,** **HideHypervisorPresent** y **ExposeVirtualizationExtensions**
-   [**Msvm \_ ConfiguraciónDefineCapabilities:**](msvm-settingsdefinecapabilities.md) **SupportStatement**
-   [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **WriteHardeningMethod**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **Shielded**
-   [**Msvm \_ SyntheticEthernetPortSettingData:**](msvm-syntheticethernetportsettingdata.md) **AllowPacketDirect**
-   [**Msvm \_ VirtualSystemCollection:**](msvm-virtualsystemcollection.md) **LastApplyConsistencyLevel**, **LastApplyVirtualMachineIds**, **LastApplyTime**, **FailedOverReplicationType,** **ReplicationMode** y **ReplicationState**
-   [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **ExportForLiveMigration**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **AvoidRemovingVHDs** y **AllowOverwriteExistingFile**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **HighMmioGapSize**
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md): **GuestBackupType**

Propiedades quitadas:

-   [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **ParentPackage**

## <a name="windows-10"></a>Windows 10

Nuevas clases:

-   [**CIM \_ CollectedMSEs**](cim-collectedmses.md)
-   [**Colección \_ CIM**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**CIM \_ ElementView**](cim-elementview.md)
-   [**CIM \_ MemberOfCollection**](cim-memberofcollection.md)
-   [**TPM \_ de CIM**](cim-tpm.md)
-   [**Vista \_ CIM**](cim-view.md)
-   [**Msvm \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**Msvm \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**Msvm \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**Msvm \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**CollectionManagementService de Msvm \_**](msvm-collectionmanagementservice.md)
-   [**Colección de \_ MsvmReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**Colección de \_ MsvmReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**Colección de \_ MsvmReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**Msvm \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**Colección de \_ MsvmSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**Colección de \_ MsvmSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**Msvm \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**Msvm \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**Msvm \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**Msvm \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**Msvm \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**Msvm \_ ManagementCollection**](msvm-managementcollection.md)
-   [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**ReferencePointCollection de Msvm \_**](msvm-referencepointcollection.md)
-   [**Msvm \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**Msvm \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**Msvm \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**Msvm \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**Msvm \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**SnapshotCollection de Msvm \_**](msvm-snapshotcollection.md)
-   [**\_SnapshotOfVirtualSystemCollection de Msvm**](msvm-snapshotofvirtualsystemcollection.md)
-   [**Msvm \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**Msvm \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**TPM de Msvm \_**](msvm-tpm.md)
-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**Msvm \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**VssService de Msvm \_**](msvm-vssservice.md)

Clase eliminada:

-   [**ResourcePoolComponent de Msvm \_**](msvm-resourcepoolcomponent.md)
-   [**Msvm \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**Virtualización de \_ MsvmComponent**](msvm-virtualizationcomponent.md)
-   [**Virtualización de \_ MsvmComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Propiedades nuevas:

-   [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**Msvm \_ EthernetPortAllocationSettingData:**](msvm-ethernetportallocationsettingdata.md) **LastKnownSwitchName** y **CompartmentGuid**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **PacketDirectInUse**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**Msvm \_ EthernetSwitchPortSecuritySettingData:**](msvm-ethernetswitchportsecuritysettingdata.md) **EnableFixSpeed10G** y **Reserved**
-   [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md): **DefaultEnabledStatePolicy**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **EnableHostResourceProtection**
-   [**Msvm \_ StorageAllocationSettingData:**](msvm-storageallocationsettingdata.md) **StorageQoSPolicyID,** **CachingMode** e **SnapshotId**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **InstanceID**, **Version**, **ThumbnailImageHeight,** **ThumbnailImageWidth** y **HostComputerSystemName**
-   [**Msvm \_ Synthetic3DDisplayControllerSettingData:**](msvm-synthetic3ddisplaycontrollersettingdata.md) **VRAMSizeBytes**
-   [**Msvm \_ VirtualEthernetSwitchSettingData:**](msvm-virtualethernetswitchsettingdata.md) **TeamingEnabled** y **PacketDirectEnabled**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **ParentTimestamp** y **ParentIdentifier**
-   [**Msvm \_ VirtualHardDiskState:**](msvm-virtualharddiskstate.md) **marca de tiempo**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **BackupIntent** y **DifferentialBackupBase**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData:**](msvm-virtualsystemmanagementservicesettingdata.md) **DefaultVirtualHardDiskCachingMode**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **RemoveSourceUnmanagedVhds** y **UnmanagedVhds**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **UserSnapshotType**, **GuestControlledCacheTypes**, **LockOnDisconnect**, **ParentPackage,** **AutomaticCriticalErrorActionTimeout,** **AutomaticCriticalErrorAction,** **ConsoleMode** y **SecureBootTemplateId**

Nuevos métodos:

-   [**Msvm \_ Clase ImageManagementService:**](msvm-imagemanagementservice.md) [**ConvertVirtualHardDiskToVHDSet,**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md) [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation,**](msvm-imagemanagementservice-getvhdsnapshotinformation.md) [**GetVirtualDiskChanges,**](msvm-imagemanagementservice-getvirtualdiskchanges.md) [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)y [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**Msvm \_ Clase ShutdownComponent:**](msvm-shutdowncomponent.md) [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**Msvm \_ VirtualSystemManagementService:**](msvm-virtualsystemmanagementservice.md) [**AddBootSourceSettings,**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md) [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings,**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md) [**RemoveBootSourceSettings,**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md) [**RemoveGuesServiceSettings,**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md) [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)y [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**Msvm \_ Clase VirtualSystemSnapshotService:**](msvm-virtualsystemsnapshotservice.md) [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 y Windows Server 2012 R2:

Windows 8.1 y Windows Server 2012 R2 incluyen nueva funcionalidad para la versión 2 del proveedor WMI de Hyper-V.

-   Las **propiedades IOPSAllocationUnits,** **IOPSLimit,** **IOPSReservation** y **PersistentReservationsSupported** se han agregado a la clase [**\_ StorageAllocationSettingData de Msvm.**](msvm-storageallocationsettingdata.md)
-   La **propiedad VirtualDiskId** se ha agregado a la clase [**Msvm \_ VirtualHardDiskSettingData.**](msvm-virtualharddisksettingdata.md)
-   Se ha agregado información sobre la QoS de almacenamiento a la **propiedad OperationalStatus** de las clases [**\_ Msvm LogicalDisk**](msvm-logicaldisk.md) y [**Msvm \_ ResourcePool.**](msvm-resourcepool.md)
-   [**Msvm \_ Clase StorageAlert**](msvm-storagealert.md)
-   La **propiedad ClusterMonitored** se ha agregado a las clases [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) y [**Msvm \_ SyntheticEthernetPortSettingData.**](msvm-syntheticethernetportsettingdata.md)
-   Las **propiedades EnableCompression** y **EnableSmbTransport** se han agregado a la clase [**Msvm \_ VirtualSystemMigrationServiceSettingData.**](msvm-virtualsystemmigrationservicesettingdata.md)
-   La **propiedad EnableCompression** se ha agregado a la clase [**Msvm \_ VirtualSystemMigrationSettingData.**](msvm-virtualsystemmigrationsettingdata.md) La **propiedad TransportType** incluye información sobre la migración en vivo.
-   [**Msvm \_ CopyFileToGuestJob (clase)**](msvm-copyfiletoguestjob.md)
-   [**Msvm \_ CopyFileToGuestSettingData (clase)**](msvm-copyfiletoguestsettingdata.md)
-   [**Msvm \_ Clase GuestFileService**](msvm-guestfileservice.md)
-   [**Msvm \_ Clase GuestService**](msvm-guestservice.md)
-   [**Msvm \_ Clase GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
-   [**Msvm \_ Clase GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**Msvm \_ RegisteredGuestService (clase)**](msvm-registeredguestservice.md)
-   La **propiedad EnhancedSessionModeEnabled** se ha agregado a la clase [**Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md)
-   La **propiedad EnhancedModeState** y [**el método InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) se han agregado a la clase ComputerSystem de [**Msvm. \_**](msvm-computersystem.md)
-   Las **propiedades BootSourceOrder**, **LowMmioGapSize**, **NetworkBootPreferredProtocol**, **PauseAfterBootFailure,** **SecureBootEnabled** y **VirtualSystemSubType** se han agregado a la clase [**Msvm \_ VirtualSystemSettingData.**](msvm-virtualsystemsettingdata.md)
-   [**Msvm \_ Clase BootSourceSettingData**](msvm-bootsourcesettingdata.md)
-   [**Msvm \_ Clase BootSourceComponent**](msvm-bootsourcecomponent.md)
-   [**Msvm \_ LogicalIdentity (clase)**](msvm-logicalidentity.md)
-   [**Msvm \_ Clase CompatibilityVector**](msvm-compatibilityvector.md)
-   El [**método GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) se ha agregado a la clase [**Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)
-   Las **propiedades ReplicationStateEx,** **ReplicationHealthEx,** **EnhancedSessionModeState,** **VirtualSwitchNames** y **VirtualSystemSubType** se han agregado a la clase [**Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Las **propiedades ReplicationState** y **ReplicationHealth** están en desuso y se reemplazan por las propiedades **ReplicationStateEx** y **ReplicationHealthEx.**
-   La **propiedad PnpDevicePath** se ha agregado a la [**clase Msvm \_ MountedStorageImage.**](msvm-mountedstorageimage.md)
-   Las **propiedades AllowedHashAlgorithms** y **TrustedIssuerCertificateHashes** se han agregado a la clase [**\_ TerminalServiceSettingData de Msvm.**](msvm-terminalservicesettingdata.md)

Windows 8.1 y Windows Server 2012 R2 incluyen una nueva funcionalidad para la replicación de máquinas virtuales y la recuperación de conmutación por error.

-   [**Msvm \_ ReplicationProvider (clase)**](msvm-replicationprovider.md)
-   [**Msvm \_ ReplicationRelationship (clase)**](msvm-replicationrelationship.md)
-   Los [**métodos ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**InitiateFailback**](initiatefailback-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)y [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) se han agregado a la clase [**\_ ReplicationService de Msvm.**](msvm-replicationservice.md) Los **métodos GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** y **ResetReplicationStatisticsEx** reemplazan a los [**métodos GetReplicationStatistics,**](getreplicationstatistics-msvm-replicationservice.md) [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)y [**ResetReplicationStatistics.**](resetreplicationstatistics-msvm-replicationservice.md)
-   La [**clase \_ SystemReplicationRelationship de Msvm**](msvm-systemreplicationrelationship.md) muestra una asociación entre una máquina virtual y muchas relaciones de replicación.
-   Las **propiedades AdditionalSettings** y **ReplicationProvider** se han agregado a la clase [**\_ ReplicationSettingData de Msvm.**](msvm-replicationsettingdata.md)
-   Se ha agregado información sobre el proveedor de host a host a los métodos [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) y [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) de la clase [**\_ ReplicationService de Msvm.**](msvm-replicationservice.md)
-   El [**método RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) se ha agregado a la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) y reemplaza al [**método RequestReplicationStateChange.**](msvm-computersystem-requestreplicationstatechange.md) La **propiedad InstanceID** ahora puede indicar la replicación extendida. Para obtener más información sobre la replicación extendida, vea Replicación de [**MsvmRelationship \_**](msvm-replicationrelationship.md).
-   [**Msvm \_ Las instancias replicationSettingData**](msvm-replicationsettingdata.md) y [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) tienen una relación 1:1 que puede representar con una asociación [**\_ SettingsDefineState de Msvm.**](msvm-settingsdefinestate.md)

    | [**Msvm \_ SettingsDefineState property**](msvm-settingsdefinestate.md) name | Valor                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | Representa el [**objeto \_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md)          |
    | **SettingData**                                                             | Representa el objeto [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) asociado |

    

     

-   [**Msvm \_ ReplicationSettingData puede diferenciar**](msvm-replicationsettingdata.md) entre establecer instancias para la relación de replicación en función de la **propiedad InstanceId** **o ReplicationRelationship.** Por lo tanto, estos métodos que tratan con una relación única no cambiaron su firma:

    -   [**Msvm \_ ReplicationService::CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**ReplicationService::Resync de Msvm \_**](resynchronize-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::StartReplication**](startreplication-msvm-replicationservice.md)

-   Aunque puede usar [**GetReplicationStatistics,**](getreplicationstatistics-msvm-replicationservice.md) [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)y [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) siempre para la relación principal, se recomienda usar en su lugar [**GetReplicationStatisticsEx,**](getreplicationstatisticsex-msvm-replicationservice.md) [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)y [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) porque pueden procesar la relación de replicación principal y extendida. Para obtener más información sobre la replicación extendida, vea [**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).
-   Aunque estas propiedades de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) siguen indicando el estado de la relación de replicación principal, use estas propiedades de un objeto [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para determinar el estado actual de la relación de replicación principal y extendida.

    | Nombre de propiedad                                | Tipo        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO) |
    | **ReplicationHealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | DateTime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | DateTime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 



