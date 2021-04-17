---
description: Resumen de los cambios de la API de VSS en Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Resumen de los cambios de la API de VSS en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696964"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a>Resumen de los cambios de la API de VSS en Windows Server 2003

## <a name="changes-in-the-vss-service"></a>Cambios en el servicio VSS

<dl> <dt>

<span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Eventos agregados:
</dt> <dd>

[*BackupShutdown*](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a>Cambios en la funcionalidad de VSS

<dl> <dt>

<span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Funcionalidad adicional:
</dt> <dd>

[*compatibilidad con archivos parciales*](vssgloss-p.md)

[*destinatarios dirigidos*](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a>Nuevas interfaces VSS

[**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a>Modificaciones de la interfaz de VSS existentes

<dl> <dt>

<span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>Interfaz [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Métodos modificados:
</dt> <dd>

[**IVssAsync:: wait**](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) (interfaz)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[**IVssBackupComponents:: QueryRevertStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[**IVssBackupComponents:: RevertToSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[**IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>Interfaz [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Métodos modificados:
</dt> <dd>

[**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>Interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>Interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Métodos quitados:
</dt> <dd>

**IVssComponent::AddNewTarget**

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Los métodos ya no están reservados:
</dt> <dd>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>Interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>Interfaz [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a>Modificaciones de clases de VSS existentes

<dl> <dt>

<span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>Clase [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Métodos modificados:
</dt> <dd>

[**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Métodos agregados:
</dt> <dd>

[**CVssWriter:: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[**CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**esquema de copia de seguridad de VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd></dd> <dt>

<span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**\_marcas de componentes de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd></dd> <dt>

<span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**\_tipo de \_ copia de seguridad de especificación de archivo VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)
</dt> <dd></dd> <dt>

<span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**\_tipo de restauración de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)
</dt> <dd></dd> </dl>

## <a name="existing-vss-enumeration-modifications"></a>Modificaciones de la enumeración de VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) Enumeración de tipo de copia de seguridad
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

copia de VSS \_ BT \_

</dd> </dl> </dd> <dt>

<span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) Enumeración de destino de restauración
</dt> <dd>

<dl> <dt>

<span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Valores quitados:
</dt> <dd>

VSS \_ RT \_ nuevo

</dd> </dl> </dd> <dt>

<span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) Enumeración de ENUMERAción RESTOREMETHOD
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

\_ \_ restauración de RME \_ de VSS en el \_ reinicio \_ si \_ no puede \_ reemplazar

</dd> </dl> </dd> <dt>

<span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) Enumeración de estado de instantánea
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

postcommit de procesamiento de VSS \_ SS \_ \_

procesamiento de VSS \_ SS \_ \_ PREFINALCOMMIT

PREFINALCOMMITTED de VSS \_ SS \_

procesamiento de VSS \_ SS \_ \_ POSTFINALCOMMIT

</dd> </dl> </dd> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeración de [**\_ \_ atributos de \_ instantánea \_ de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ Autorrecuperación

</dd> <dt>

<span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Los valores reservados ahora admiten:
</dt> <dd>

VSS \_ VOLSNAP \_ atributo \_ \_ asistido por hardware

\_atributo VOLSNAP de VSS \_ \_ importado

VSS \_ VOLSNAP \_ ATTR \_ expuesto \_ localmente

VSS \_ VOLSNAP \_ ATTR \_ expuesto de \_ forma remota

</dd> </dl> </dd> <dt>

<span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) Enumeración de estado del escritor
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

\_ \_ error de VSS WS \_ en \_ BACKUPSHUTDOWN

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a>Cambios en las estructuras de VSS

<dl> <dt>

<span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS \_ Estructura COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)
</dt> <dd>

<dl> <dt>

<span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Miembros agregados:
</dt> <dd>

**bSelectableForRestore**

**dwComponentFlags**

**cDependencies**

</dd> </dl> </dd> </dl>

 

 



