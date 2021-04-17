---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Novedades de VSS en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696438"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Novedades de VSS en Windows Vista

Windows Vista presenta los siguientes cambios en el Servicio de instantáneas de volumen.

Tenga en cuenta que todos los cambios de Windows Vista también se aplican a Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Nuevas interfaces VSS

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Nuevas clases de VSS

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

[**tipo de puesta al día de VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modificaciones de la enumeración de VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Enumeración de esquema de copia de seguridad
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

\_ \_ restauración autoritativa de VSS BS \_

\_ \_ \_ Estado del sistema independiente de VSS BS \_

\_cambio de \_ nombre de restauración de VSS BS \_

restauración con puesta al día de VSS \_ BS \_ \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) Enumeración de marcas de componentes
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

\_ \_ \_ Estado del sistema de VSS CF no \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeración de [**\_ \_ atributos de \_ instantánea \_ de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ no \_ autoRecovery

\_atributo VOLSNAP de VSS \_ \_ no \_ transaccionado

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Seguimiento y registro de eventos de VSS

-   El archivo de seguimiento de VSS ahora se puede encontrar en cualquier volumen local. En las versiones de Windows anteriores a Windows Vista, el archivo de seguimiento de VSS no se encontró en un volumen que se encontraba en el conjunto de instantáneas.
-   Muchas de las entradas del registro de eventos se han reparado para que sean más claras.
-   Todas las entradas del registro de eventos de VSS contienen ahora información de contexto.

## <a name="vss-error-reporting"></a>Informe de errores de VSS

-   Ahora se pueden recuperar las descripciones de todos los códigos de error de VSS mediante una llamada a la función [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con el \_ mensaje Format desde la \_ \_ marca HMODULE especificado en el parámetro *dwFlags* .
-   Los mensajes del código de error de VSS se incluyen en vsstrace.dll. Se debe especificar un identificador para este módulo en el parámetro *lpSource* .

## <a name="excluding-files-from-shadow-copies"></a>Excluir archivos de instantáneas

Las aplicaciones o los servicios pueden usar la clave del registro FilesNotToSnapshot para especificar los archivos que se van a eliminar de las instantáneas recién creadas. Para obtener más información, vea [excluir archivos de instantáneas](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Compatibilidad de aplicaciones de copia de seguridad y restauración

Los desarrolladores de aplicaciones de copia de seguridad y restauración deben tener en cuenta ciertas características nuevas de Windows Vista y Windows Server 2008. Para obtener una lista de comprobación de compatibilidad de aplicaciones, vea [compatibilidad de aplicaciones para copias de seguridad y restauración](application-compatibility-for-backup-and-restore.md).

 

 
