---
description: 'Durante una operación de copia de seguridad, el solicitante usa IVssBackupComponents:: SetBackupState para definir el tipo de operación en curso.'
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Estado de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809824"
---
# <a name="vss-backup-state"></a>Estado de copia de seguridad de VSS

Durante una operación de copia de seguridad, el solicitante usa [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para definir el tipo de operación en curso.

Esta información no se incluye en un formulario fácil de recuperar en el documento componentes de copia de seguridad, por lo que los programadores del solicitante deben almacenar esta información de forma independiente en cualquier medio de copia de seguridad.

El estado de copia de seguridad contiene lo siguiente:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo de copia de seguridad
</dt> <dd>

El tipo de copia de seguridad especifica los criterios para identificar los archivos de los que se va a hacer una copia de seguridad. La evaluación de estos criterios debe realizarse mediante la API de VSS.

Al decidir el tipo de copia de seguridad que se va a llevar a cabo y con qué escritores trabajar, los solicitantes deben examinar los tipos (o esquemas; vea [compatibilidad con esquemas de copia de seguridad del escritor](writer-backup-schema-support.md)) de las operaciones de copia de seguridad que admite cada uno de los escritores del sistema. Las copias de seguridad en VSS pueden ser los siguientes tipos:

-   Completo (VSS \_ BT \_ Full): se realizará una copia de seguridad de los archivos, independientemente de la fecha de la última copia de seguridad. Se actualizará el historial de copia de seguridad de cada archivo y este tipo de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial. La restauración de una copia de seguridad completa requiere una sola imagen de copia de seguridad.
-   Copia de seguridad ( \_ copia \_ de VSS BT): al igual que el \_ tipo de copia de seguridad completa de VSS BT, se realizará \_ una copia de seguridad de los archivos, independientemente de la fecha de la última copia de seguridad. Sin embargo, el historial de copia de seguridad de cada archivo no se actualizará y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial.
-   Incremental ( \_ de VSS BT \_ incremental): la API de VSS se usa para garantizar que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de almacenamiento. La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.
-   Diferencial ( \_ \_ diferencial de VSS BT): la API de VSS se usa para garantizar que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copien en un medio de almacenamiento; se omite toda la información de copia de seguridad intermedia. La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.
-   Archivo de registro ( \_ \_ registro de VSS BT): solo se realizará una copia de seguridad de los archivos de registro del escritor (los archivos agregados a un componente con el método [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) y recuperados mediante una llamada a [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)). Este tipo de copia de seguridad es específico de VSS.

Es posible que los solicitantes implementen estas copias de seguridad con la información y los métodos externos a VSS. Solo cuando un solicitante implementa una copia de seguridad mediante la API de VSS, se dice que tiene uno de los tipos de copia de seguridad enumerados. Por ejemplo, un solicitante participa en un \_ \_ tipo de registro de VSS BT de copia de seguridad solo si usó la información devuelta por [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) para identificar los archivos de registro. De forma similar, \_ los \_ tipos de diferencia incremental de VSS BT y \_ de VSS BT \_ solo se aplican a las operaciones incrementales o diferenciales, como se describe en [copias de seguridad incrementales y diferenciales](incremental-and-differential-backups.md).

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Especificación sobre la selección
</dt> <dd>

Una copia de seguridad de VSS puede optar por respetar las nociones de VSS de selección de componentes, lo que se conoce como ejecución en [*modo de componente*](vssgloss-c.md), o para omitirlos.

Un ejemplo de que no se está ejecutando en modo de componente sería realizar una copia de seguridad de imagen del sistema, donde la aplicación de copia de seguridad necesitaría la cooperación del escritor para garantizar la estabilidad de los datos, pero cuando la selección de los componentes sería irrelevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Guardando el estado de arranque
</dt> <dd>

VSS permite guardar el estado del sistema en ejecución en una configuración de arranque completo. Sin embargo, esto no siempre es necesario y la preparación del escritor para guardar un estado de arranque a veces puede degradar el rendimiento en tiempo real de un sistema en ejecución.

Por lo tanto, los solicitantes indican si una copia de seguridad incluirá un estado del sistema de arranque como argumento para [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Los escritores determinan si deben admitir el guardado del estado del sistema de arranque mediante una llamada a [**CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Incluso si el estado del sistema de arranque no está seleccionado, se realizarán instantáneas de los archivos del sistema y se puede realizar una copia de seguridad de los archivos.

Sin embargo, se debe prestar mucha atención a la restauración de archivos del sistema si la copia de seguridad no guardó el estado del sistema de arranque (consulte [copia de seguridad y restauración del estado del sistema en Windows server 2003 R2 y Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

No es posible recuperar esta información de un documento de componentes de copia de seguridad recuperados, por lo que los autores del solicitante deben almacenar si se realizó una copia de seguridad del sistema con un estado del sistema de arranque o no.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Compatibilidad con archivos parciales
</dt> <dd>

Algunos escritores admiten la restauración de archivos a través de la sobrescritura de partes de los archivos que administran. Un solicitante puede estar diseñado para aprovecharse de esto y, si es así, lo indica estableciendo la información en [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



