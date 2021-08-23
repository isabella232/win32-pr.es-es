---
description: Durante una operación de copia de seguridad, el solicitante usa IVssBackupComponents::SetBackupState para definir el tipo de operación en curso.
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Estado de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35701e1b576d9ea2e5464516589ae419dc73b74898768af06e974da05afffa8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056223"
---
# <a name="vss-backup-state"></a>Estado de copia de seguridad de VSS

Durante una operación de copia de seguridad, el solicitante usa [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para definir el tipo de operación en curso.

Esta información no se incluye en un formulario fácilmente recuperable en el documento Componentes de copia de seguridad, por lo que los desarrolladores solicitantes deben almacenar esta información de forma independiente en cualquier medio de copia de seguridad.

El estado de copia de seguridad contiene lo siguiente:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo de copia de seguridad
</dt> <dd>

El tipo de copia de seguridad especifica los criterios para identificar los archivos de los que se va a realizar una copia de seguridad. La evaluación de estos criterios debe realizarse mediante la API de VSS.

Al decidir el tipo de copia de seguridad que se va a llevar a cabo y con qué escritores trabajar, los solicitantes deben examinar los tipos (o esquemas), consulte Writer [Backup Schema Support](writer-backup-schema-support.md)(Compatibilidad con esquemas de copia de seguridad del escritor) de las operaciones de copia de seguridad que admiten cada uno de los escritores del sistema. Las copias de seguridad en VSS pueden ser los siguientes tipos:

-   Full (VSS BT FULL): se realizará una copia de seguridad de los archivos, independientemente \_ de la fecha de la última copia de \_ seguridad. Se actualizará el historial de copia de seguridad de cada archivo y este tipo de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial. La restauración de una copia de seguridad completa solo requiere una sola imagen de copia de seguridad.
-   Copia de seguridad (COPIA DE VSS BT): al igual que el tipo de copia de seguridad COMPLETA de VSS BT, se realizará una copia de seguridad de los archivos independientemente de la fecha de la \_ \_ última copia de \_ \_ seguridad. Sin embargo, el historial de copia de seguridad de cada archivo no se actualizará y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial.
-   Incremental (INCREMENTAL de VSS BT): la API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de \_ \_ almacenamiento. La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.
-   Diferencial (VSS BT DIFFERENTIAL): la API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copiarán en un medio de almacenamiento; se omite toda la información de copia de seguridad \_ \_ intermedia. La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.
-   Archivo de registro (VSS BT LOG): solo se realizará una copia de seguridad de los archivos de registro de un escritor (archivos agregados a un componente con el método \_ \_ [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) y recuperados mediante una llamada a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Este tipo de copia de seguridad es específico de VSS.

Es posible que los solicitantes implementen estas copias de seguridad mediante información y métodos fuera de VSS. Solo cuando un solicitante implementa una copia de seguridad mediante la API de VSS si se dice que tiene uno de los tipos de copia de seguridad enumerados. Por ejemplo, un solicitante participa en un tipo de copia de seguridad de VSS BT LOG solo si usa la información devuelta por \_ \_ [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) para identificar los archivos de registro. De forma similar, los tipos INCREMENTAL y DIFERENCIAL DE VSS BT y VSS BT DIFFERENTIAL solo se aplican a las operaciones incrementales o diferenciales, como se describe en Copias de seguridad \_ \_ \_ \_ [incrementales y diferenciales.](incremental-and-differential-backups.md)

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Especificación sobre la capacidad de selección
</dt> <dd>

Una copia de seguridad de VSS puede optar por respetar las nociones de VSS de la capacidad de selección de componentes (esto se conoce como ejecución en modo [*de*](vssgloss-c.md)componente) o omitirlas.

Un ejemplo de que no se ejecuta en modo de componente sería realizar una copia de seguridad de imagen del sistema, donde la aplicación de copia de seguridad necesitará la cooperación del escritor para garantizar la estabilidad de los datos, pero donde la selección de componentes sería irrelevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Guardar el estado de arranque
</dt> <dd>

VSS admite el guardado del estado del sistema en ejecución en una configuración totalmente de arranque. Sin embargo, esto no siempre es necesario y la preparación del escritor para guardar un estado de arranque a veces puede degradar el rendimiento en tiempo real de un sistema en ejecución.

Por lo tanto, los solicitantes indican si una copia de seguridad incluirá un estado del sistema de arranque como argumento para [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Los escritores determinan si tienen que admitir el guardado del estado del sistema de arranque mediante una llamada [**a CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Incluso si no se selecciona el estado del sistema de arranque, se realizarán instantáneas de los archivos del sistema y se puede realizar una copia de seguridad de los archivos.

Sin embargo, se debe tener mucho cuidado en la restauración de archivos del sistema si la copia de seguridad no ha guardado el estado del sistema de arranque (vea Copia de seguridad y restauración del estado del sistema en [Windows Server 2003 R2 y Windows Server 2003 SP1).](backing-up-and-restoring-system-state-under-vss.md)

No es posible recuperar esta información de un documento de componentes de copia de seguridad recuperado, por lo que los autores de solicitudes deben almacenar si se ha hecho una copia de seguridad del sistema con un estado del sistema de arranque o no.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Compatibilidad con archivos parciales
</dt> <dd>

Algunos escritores admiten la restauración de archivos mediante la sobrescritura de partes de los archivos que administran. Un solicitante puede estar diseñado para aprovechar esto y, si es así, lo indica estableciendo la información en [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



