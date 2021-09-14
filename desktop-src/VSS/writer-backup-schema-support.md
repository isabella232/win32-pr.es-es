---
description: Para implementar completamente una copia de seguridad, es necesario la participación de los escritores del sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Compatibilidad con esquemas de copia de seguridad del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242025"
---
# <a name="writer-backup-schema-support"></a>Compatibilidad con esquemas de copia de seguridad del escritor

Para implementar completamente una copia de seguridad, es necesario la participación de los escritores del sistema. Los distintos tipos de copias de seguridad admitidas se conocen como esquemas y se indican mediante una máscara de bits (o OR bit a bit) de miembros de la enumeración [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Entre los esquemas válidos admitidos actualmente se incluyen los siguientes:

-   Esquema predeterminado: Completo (VSS \_ BS UNDEFINED): indica que un escritor admite una copia de seguridad en la que se realizará una copia de seguridad de todos los archivos, independientemente de la fecha de la última \_ copia de seguridad. El solicitante puede actualizar el historial de copias de seguridad de cada archivo y los escritores que admiten el valor de enumeración TIMESTAMPED de \_ VSS BS almacenarán una marca de tiempo actualizada con el \_ solicitante. Este esquema de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial.

    La restauración de una copia de seguridad completa solo requiere una sola imagen de copia de seguridad.

-   Copia de seguridad (COPIA DE VSS BS): al igual que el esquema de copia de seguridad completa de \_ \_ \_ VSS BS, indica que un escritor admite una copia de seguridad en la que se realizará una copia de seguridad de todos los archivos, independientemente de su última fecha de copia de \_ seguridad. Sin embargo, el solicitante o escritor no actualizará el historial de copias de seguridad de cada archivo, y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial.
-   Archivo de registro (VSS BS LOG): solo se va a hacer una copia de seguridad de los archivos de registro de \_ \_ un escritor. Esto requiere que un escritor haya agregado al menos un archivo a un componente mediante el método [**IVssCreateWriterMetadata::AddDatabaseLogFiles.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) Este tipo de copia de seguridad es específico de VSS.
-   Ubicaciones de restauración personalizadas (VSS BS WRITER ADMITE NUEVO DESTINO): indica la compatibilidad del escritor con un solicitante que cambia, en el momento de la restauración, donde \_ \_ se \_ \_ \_ restauran sus archivos. Esto significa que se ha codificado un sistema de escritura para comprobar dicha reubicación (mediante [**IVssComponent::GetNewTarget)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)y tiene la capacidad de trabajar con archivos reubicados.
-   Restaurar con movimiento (VSS BS WRITER ADMITE RESTORE WITH MOVE): indica que el escritor admite la ejecución de varias instancias de escritor con el mismo identificador de clase y admite que un solicitante mueva un componente a otra instancia de escritor en tiempo de \_ \_ \_ \_ \_ \_ restauración. La instancia de escritor se especifica mediante un nombre de instancia de escritor persistente que se pasó como parámetro *wszWriterInstanceName* al [**método CVssWriter::Initialize.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) Un solicitante puede obtener el nombre de instancia del escritor mediante [**IVssExgvWriterMetadataEx::GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) y mover componentes durante la restauración mediante [**IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Server 2003 con Service Pack 1 (SP1).

-   Incremental (INCREMENTAL de VSS BS): indica que el escritor usa la API de VSS para ayudar al solicitante, lo que garantiza que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de \_ \_ almacenamiento.

    La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.

-   Diferencial (VSS BS DIFFERENTIAL): indica que el escritor usa la API de VSS para ayudar al solicitante a asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copiarán en un medio de almacenamiento; se omite toda la información de copia de seguridad \_ \_ intermedia.

    La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.

-   Incremental/Diferencial: compatibilidad con la marca de tiempo (VSS BS TIMESTAMPED): indica que un escritor admite el uso del mecanismo de marca de tiempo de VSS para incluir archivos en operaciones incrementales o \_ \_ diferenciales. En la copia de [](vssgloss-f.md) seguridad, el escritor debe almacenar la marca de copia de seguridad de un conjunto de archivos con el método [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) y, en la restauración, recuperarlo con [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incremental/Diferencial: tiempo de compatibilidad con la última modificación (VSS BS LAST MODIFY): indica que al implementar copias de seguridad incrementales o diferenciales con archivos diferenciados, un sistema de escritura puede proporcionar información sobre la hora de la última modificación de forma \_ \_ \_ independiente. Esta información se puede proporcionar a un solicitante a través del método [**IVssComponent::AddDifferencedFilesByLastModifyTime.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)
-   Incremental/Diferencial: limitación de compatibilidad (DIFERENCIAL INCREMENTAL EXCLUSIVO de VSS BS): indica la compatibilidad del escritor con esquemas de copia de seguridad diferenciales o incrementales, pero solo exclusivamente: por ejemplo, no se puede seguir una copia de seguridad incremental con una copia de seguridad \_ \_ \_ \_ diferencial.
-   Estado del sistema independiente (ESTADO DEL SISTEMA INDEPENDIENTE DE VSS BS): indica que el sistema de escritura admite la copia de seguridad de datos que forman parte del estado del sistema, pero de los que también se puede hacer una copia de seguridad independientemente del estado del \_ \_ \_ \_ sistema.

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Roll-Forward restore (VSS BS ROLLFORWARD RESTORE): indica que el escritor admite un solicitante que establece un punto de restauración de puesta al día mediante \_ \_ \_ [**IVssBackupComponentsEx2::SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Restore Rename (VSS BS RESTORE RENAME): indica que el escritor admite un solicitante que establece un nombre de restauración mediante \_ \_ \_ [**IVssBackupComponentsEx2::SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Restauración autoritativa (RESTORE AUTORITATIVA de VSS BS): indica que el escritor admite una restauración autoritativa de configuración del solicitante mediante \_ \_ \_ [**IVssBackupComponentsEx2::SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

Los escritores establecen sus esquemas mediante el método [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) y un solicitante obtiene el esquema de cada escritor mediante una llamada a [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



