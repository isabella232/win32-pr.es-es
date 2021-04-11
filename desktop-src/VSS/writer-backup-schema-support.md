---
description: Para implementar completamente una copia de seguridad, es necesario participar en los escritores del sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Compatibilidad con el esquema de copia de seguridad del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275421"
---
# <a name="writer-backup-schema-support"></a>Compatibilidad con el esquema de copia de seguridad del escritor

Para implementar completamente una copia de seguridad, es necesario participar en los escritores del sistema. Los distintos tipos de copias de seguridad admitidas se conocen como esquemas y se indican mediante una máscara de bits (o OR bit a bit) de los miembros de la enumeración de [**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) . Los esquemas válidos que se admiten actualmente son los siguientes:

-   Esquema predeterminado: completo (VSS \_ BS sin \_ definir): indica que un escritor admite una copia de seguridad en la que se realizará la copia de seguridad de todos los archivos, independientemente de la fecha de la última copia de seguridad. El solicitante puede actualizar el historial de copia de seguridad de cada archivo, y los escritores que admiten el \_ \_ valor de enumeración marca de tiempo de VSS BS, almacenarán una marca de tiempo actualizada con el solicitante. Este esquema de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial.

    La restauración de una copia de seguridad completa requiere una sola imagen de copia de seguridad.

-   Copia de seguridad ( \_ copia \_ de VSS BS): al \_ igual \_ que el esquema de copia de seguridad completa de VSS BS, indica que un escritor admite una copia de seguridad en la que se realizará la copia de seguridad de todos los archivos, independientemente de su fecha de copia de seguridad. No obstante, el historial de copia de seguridad de cada archivo no se actualizará mediante el solicitante o el escritor, y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial.
-   Archivo de registro ( \_ \_ registro de VSS BS): solo se realizará una copia de seguridad de los archivos de registro del escritor. Esto requiere que un escritor haya agregado al menos un archivo al menos a un componente mediante el método [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Este tipo de copia de seguridad es específico de VSS.
-   Ubicaciones de restauración personalizadas (VSS \_ BS \_ Writer \_ es compatible con el \_ nuevo \_ destino): indica la compatibilidad del escritor con un solicitante que cambia, en el momento de la restauración, donde se restauran sus archivos. Esto significa que se ha codificado un escritor para comprobar tal reubicación (mediante [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) y tiene la capacidad para trabajar con archivos reubicados.
-   Restore with Move (VSS \_ BS \_ Writer \_ admite \_ restore \_ with \_ Move): indica que el escritor admite la ejecución de varias instancias del escritor con el mismo identificador de clase y que admite un solicitante que mueve un componente a una instancia de escritor diferente en el momento de la restauración. La instancia del escritor se especifica mediante un nombre de instancia de escritor persistente que se pasó como el parámetro *wszWriterInstanceName* al método [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) . Un solicitante puede obtener el nombre de instancia del escritor mediante [**IVssExamineWriterMetadataEx:: GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) y trasladar los componentes durante la restauración con [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Server 2003 con Service Pack 1 (SP1).

-   Incremental (VSS \_ BS \_ incremental): indica que el escritor usa la API de VSS para ayudar al solicitante, lo que garantiza que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de almacenamiento.

    La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.

-   Diferencial (VSS \_ BS \_ diferencial): indica que el escritor usa la API de VSS para ayudar al solicitante a asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se van a copiar en un medio de almacenamiento; se omite toda la información de copia de seguridad intermedia.

    La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.

-   Incremental/diferencial: compatibilidad con la marca de tiempo (VSS \_ BS \_ timestamp): indica que un escritor admite el uso del mecanismo de marca de tiempo de VSS para incluir archivos en operaciones incrementales o diferenciales. En la copia de seguridad, el escritor debe almacenar el sello de la copia [*de seguridad del conjunto de archivos*](vssgloss-f.md) con el método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) y, en la restauración, recuperarlo con [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incremental/diferencial: hora de la última modificación (compatibilidad de VSS \_ BS \_ última \_ modificación): indica que al implementar copias de seguridad incrementales o diferenciales con archivos diferenciados, un escritor puede proporcionar información de hora de última modificación de forma independiente. Esta información se puede proporcionar a un solicitante a través del método [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) .
-   Incremental/diferencial: limitación de compatibilidad ( \_ de VSS BS \_ exclusivo \_ incremental \_ diferencial): indica la compatibilidad del escritor de esquemas de copia de seguridad diferenciales o incrementales, pero solo de forma exclusiva: por ejemplo, no se puede seguir una copia de seguridad incremental con una copia de seguridad diferencial.
-   Estado del sistema independiente (VSS \_ BS \_ independiente \_ del sistema \_ ): indica que el escritor admite la copia de seguridad de los datos que forman parte del estado del sistema, pero también se puede realizar una copia de seguridad del estado del sistema de forma independiente.

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Restauración de Roll-Forward ( \_ \_ restauración con puesta al día de VSS BS \_ ): indica que el escritor admite un solicitante que establezca un punto de restauración de puesta al día mediante [**IVssBackupComponentsEx2:: SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Restore Rename (VSS \_ BS \_ restore \_ Rename): indica que el escritor es compatible con un solicitante que establezca un nombre de restauración mediante [**IVssBackupComponentsEx2:: SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 y Windows XP:** Este valor no se admite hasta Windows Vista.

-   Restauración autoritativa \_ ( \_ restauración autoritativa de VSS BS \_ ): indica que el escritor admite una restauración autoritativa del solicitante mediante [**IVssBackupComponentsEx2:: SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

Los escritores establecen sus esquemas mediante el método [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) y un solicitante obtiene el esquema de cada escritor llamando a [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



