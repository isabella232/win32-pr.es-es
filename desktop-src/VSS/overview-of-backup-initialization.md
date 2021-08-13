---
description: Esta fase de la copia de seguridad inicializa tanto el escritor como el solicitante, rellenando sus estructuras de datos internas, especificando la copia de seguridad y establece la comunicación entre escritor y solicitante a través de la llamada necesaria a IVssBackupComponents::GatherWriterMetadata. Para obtener más información, vea Información general sobre el procesamiento de una copia de seguridad en VSS.
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Información general sobre la inicialización de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4054dc644056100a4db28ea11b6dcaf9c358084a1b01b9ad28c13e14133fc5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591359"
---
# <a name="overview-of-backup-initialization"></a>Información general sobre la inicialización de copia de seguridad

Esta fase de la copia de seguridad inicializa tanto el escritor como el solicitante, rellenando sus estructuras de datos internas, especificando la copia de seguridad y establece la comunicación entre escritor y solicitante a través de la llamada necesaria a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Para obtener más información, vea [Información general sobre el procesamiento de una copia de seguridad en VSS.](overview-of-processing-a-backup-under-vss.md)

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para la inicialización de la copia de seguridad.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Acción del escritor                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crea una [**interfaz IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e inicializa para administrar una copia de seguridad (vea [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForBackup)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)y, opcionalmente, habilita o deshabilita escritores en el sistema. | None                                                      | None                                                                                                                                                                                                                                                       |
| Opcionalmente, establezca el contexto para las operaciones de instantáneas y, opcionalmente, consulte el sistema sobre los proveedores y las instantáneas que admite (vea [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | None                                                      | None                                                                                                                                                                                                                                                       |
| El solicitante puede proporcionar información adicional sobre cómo controlar las operaciones de copia de seguridad y restauración (vea [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate))                                                                                                                                                        | None                                                      | None                                                                                                                                                                                                                                                       |
| Inicia el contacto asincrónico con los escritores (vea [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Identificar*](vssgloss-i.md) | Crea un documento de metadatos del escritor (vea [Trabajar](working-with-the-writer-metadata-document.md)con el documento de metadatos del escritor , [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Acciones del solicitante durante la inicialización de copia de seguridad

Un [**objeto IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) solo se puede usar para una copia de seguridad. Por lo tanto, un solicitante debe continuar hasta el final de la copia de seguridad, incluida la liberación de la **interfaz IVssBackupComponents.** Si la copia de seguridad debe finalizar prematuramente, el solicitante debe llamar a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) y, a continuación, liberar el objeto **IVssBackupComponents** (vea [Aborting VSS Operations](aborting-vss-operations.md) (Anular operaciones vsS) para obtener más información). No intente reanudar la **interfaz IVssBackupComponents.**

Normalmente, el documento de componentes de copia de seguridad de un solicitante se inicializa como vacío. Se puede cargar un documento de componentes de copia de seguridad almacenado cuando se llama a [**IVssBackupComponents::InitializeForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) normalmente para admitir volúmenes de instantáneas transportables. En este caso, la comunicación escritor-solicitante será algo diferente de lo que se describe a continuación. (Vea [Importar volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md) para obtener más información).

Para agregar volúmenes al conjunto de instantáneas, un solicitante debe establecer primero el contexto de la operación de instantánea llamando a [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Si no se llama a este método, se usa el contexto predeterminado para las instantáneas, VSS \_ CTX \_ BACKUP. Para obtener información sobre cómo establecer el contexto de la instantánea, vea [Configuraciones de contexto de instantáneas.](shadow-copy-context-configurations.md)

Para comenzar la finalización de su instalación antes de la copia de seguridad, un solicitante debe llamar a [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Al hacerlo, un solicitante indica a los escritores:

-   Tipo de copia de seguridad (tal y como se define en [**VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Si la copia de seguridad incluye un estado del sistema de arranque
-   Si el solicitante admite la selección de componentes individuales o hace una copia de seguridad de volúmenes completos.

Todos los solicitantes que participan en las operaciones de copia de seguridad y restauración deben llamar siempre [**a IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Este método inicia la comunicación escritor-solicitante generando un evento VSS [*Identify,*](vssgloss-i.md) en respuesta a la cual un escritor crea su documento de metadatos.

Antes de llamar a [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)un solicitante tiene la oportunidad de habilitar o deshabilitar explícitamente determinados escritores y clases de escritores mediante [**IVssBackupComponents::EnableWriterClasses,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses) [**IVssBackupComponents::D isableWriterInstances e**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances) [**IVssBackupComponents::D isableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (de forma predeterminada, todas las clases están habilitadas). Después **de llamar a IVssBackupComponents::GatherWriterMetadata,** estas llamadas no tienen ningún efecto.

Dado que no hay ninguna manera de obtener una lista de escritores en el sistema antes de llamar a [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)los solicitantes pueden considerar la posibilidad de crear y eliminar una segunda instancia de [**IVssBackupComponents para**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) obtener la lista.

No es necesario llamar a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) después de la finalización de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Los escritores que no puedan procesar el evento [*Identify*](vssgloss-i.md) generado por las llamadas no formarán parte de la lista de escritores que proporcionan metadatos encontrados por [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vea [Determinar](determining-writer-status.md)el estado del escritor).

## <a name="writer-actions-during-backup-initialization"></a>Acciones de escritura durante la inicialización de copia de seguridad

En respuesta al evento Identify, VSS llama al método de controlador virtual de cada escritor, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify). Un escritor crea su documento de metadatos del escritor reemplazando la implementación predeterminada de **CVssWriter::OnIdentify** y usando la [**interfaz IVssCreateWriterMetadata.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)

Tenga en cuenta que las aplicaciones que no sean el solicitante actual (por ejemplo, las aplicaciones del sistema) pueden generar eventos de identificación que debe controlar el escritor. Además, no hay ninguna manera de que un escritor determine desde [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qué aplicación ha generado el evento Identify.

Este es el caso, dado que un escritor puede recibir varios eventos Identify durante el procesamiento de una operación de copia de seguridad, un escritor nunca debe establecer información de estado en el controlador [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

En su lugar, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) debe realizar un algoritmo coherente para crear el documento de metadatos del escritor, especialmente porque, después de que un escritor crea el documento, ni el solicitante ni el escritor pueden modificarlo. A partir de ahora, es un documento de solo lectura.

Esto significa que el [](vssgloss-c.md) número y el tipo de componentes asociados a un escritor, qué archivos forman parte de cada componente, y la exclusión explícita de archivos de las operaciones de copia de seguridad o restauración no se pueden cambiar después de que un escritor vuelva de procesar el evento Identify.

Todos los escritores que participan con VSS deben hacer lo siguiente:

1.  Indique un método de restauración para todos los componentes administrados por el escritor mediante [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Agregue al menos un componente mediante [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (vea [Definición](definition-of-components-by-writers.md) de componentes por escritores para obtener más información sobre la especificación de componentes).

Un sistema de escritura indica los archivos para participar en una operación de copia de seguridad o restauración agregando conjuntos de archivos [*(una*](vssgloss-f.md)combinación de una ruta de acceso, una especificación de archivo y una marca de recursividad) a un componente [](definition-of-components-by-writers.md)determinado mediante [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)según el tipo (vea Agregar archivos a componentes).

Un sistema de escritura también puede tener uno o varios componentes vacíos, componentes a los que no se ha agregado ningún archivo. Son muy útiles para organizar los componentes del escritor. (Vea [Ruta de acceso lógica de componentes).](logical-pathing-of-components.md)

Un escritor usa [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) para evitar explícitamente que los archivos se incluyan en la copia de seguridad. Esta exclusión explícita es útil porque se pueden usar caracteres comodín para especificar archivos para su inclusión (vea [Exclude File List Specification](writer-metadata-document-contents.md)). Tenga en cuenta que la lista de archivos de exclusión tiene prioridad sobre las listas de archivos de componentes.

[**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) se usa para crear asignaciones de ubicación alternativas para conjuntos de archivos [*especificados*](vssgloss-a.md) que se han agregado a uno de los componentes del escritor. Estas asignaciones se usan durante la restauración de archivos cuando la restauración en la ubicación original de un archivo no es posible ni deseable. (Consulte Información [general sobre la restauración de archivos reales y](overview-of-actual-file-restoration.md) las ubicaciones de copia de seguridad y [restauración no predeterminadas).](non-default-backup-and-restore-locations.md)

Dado que el conjunto de archivos de copia de seguridad se especifica en el documento de metadatos del escritor, no se puede modificar más adelante. Por lo tanto, se debe codificar un sistema de escritura para que la definición del conjunto de archivos incluya todos los archivos necesarios en la copia de seguridad, ya sea por nombre o a través de caracteres comodín. Posiblemente, esto puede incluir algunos archivos que se pueden crear después del evento Identify.

 

 



