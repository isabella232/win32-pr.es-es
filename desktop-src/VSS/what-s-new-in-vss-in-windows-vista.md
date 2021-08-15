---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Novedades de VSS en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751147"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Novedades de VSS en Windows Vista

Windows Vista presenta los siguientes cambios en el Servicio de instantáneas de volumen.

Tenga en cuenta que todos los cambios de Windows Vista también se aplican a Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Nuevas interfaces vss

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExgvWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Nuevas clases vss

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

[**VSS \_ ROLLFORWARD \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modificaciones de enumeración de VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ BACKUP \_ SCHEMA (enumeración)**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

RESTAURACIÓN \_ AUTORITATIVA DE VSS BS \_ \_

ESTADO DEL \_ SISTEMA INDEPENDIENTE DE VSS BS \_ \_ \_

CAMBIO DE NOMBRE \_ DE LA RESTAURACIÓN DE VSS BS \_ \_

RESTAURACIÓN \_ \_ ROLLFORWARD DE VSS BS \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ COMPONENT \_ FLAGS (enumeración)**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

VSS \_ CF \_ NOT \_ SYSTEM \_ STATE

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ ENUMERACIÓN \_ DE ATRIBUTOS DE \_ INSTANTÁNEAS DE VOLUMEN \_ DE VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY

VSS \_ VOLSNAP \_ ATTR \_ NOT \_ TRANSACTED

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Seguimiento y registro de eventos de VSS

-   El archivo de seguimiento de VSS ahora se puede encontrar en cualquier volumen local. En versiones de Windows anteriores a Windows Vista, el archivo de seguimiento de VSS no se podía encontrar en un volumen que estaba en el conjunto de instantáneas.
-   Muchas entradas del registro de eventos se han reelabdado para que se aclaren más.
-   Todas las entradas del registro de eventos de VSS ahora contienen información de contexto.

## <a name="vss-error-reporting"></a>Informes de errores de VSS

-   Ahora se pueden recuperar descripciones de todos los códigos de error de VSS llamando a la función [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT MESSAGE FROM HMODULE especificada en el \_ parámetro \_ \_ *dwFlags.*
-   Los mensajes de código de error de VSS se incluyen en vsstrace.dll. Se debe especificar un identificador para este módulo en el *parámetro lpSource.*

## <a name="excluding-files-from-shadow-copies"></a>Exclusión de archivos de instantáneas

Las aplicaciones o servicios pueden usar la clave del Registro FilesNotToSnapshot para especificar los archivos que se eliminarán de las instantáneas recién creadas. Para obtener más información, vea [Excluir archivos de instantáneas.](excluding-files-from-shadow-copies.md)

## <a name="backup-and-restore-application-compatibility"></a>Compatibilidad de aplicaciones de copia de seguridad y restauración

Los desarrolladores de aplicaciones de copia de seguridad y restauración deben tener en cuenta ciertas características nuevas en Windows Vista y Windows Server 2008. Para obtener una lista de comprobación de compatibilidad de aplicaciones, vea [Compatibilidad de aplicaciones para copias de seguridad y restauración.](application-compatibility-for-backup-and-restore.md)

 

 
