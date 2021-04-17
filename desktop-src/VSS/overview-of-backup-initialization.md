---
description: 'Esta fase de la copia de seguridad inicializa el escritor y el solicitante, rellenando sus estructuras de datos internas, especificando la copia de seguridad y establece la comunicación entre escritor y solicitante a través de la llamada necesaria a IVssBackupComponents:: GatherWriterMetadata. Para obtener más información, vea información general sobre el procesamiento de una copia de seguridad en VSS.'
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Información general sobre la inicialización de copias de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696993"
---
# <a name="overview-of-backup-initialization"></a>Información general sobre la inicialización de copias de seguridad

Esta fase de la copia de seguridad inicializa el escritor y el solicitante, rellenando sus estructuras de datos internas, especificando la copia de seguridad y establece la comunicación entre escritor y solicitante a través de la llamada necesaria a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Para obtener más información, vea [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md).

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para la inicialización de la copia de seguridad.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Acción del escritor                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crea una interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y la inicializa para administrar una copia de seguridad (vea [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) y, opcionalmente, habilitar o deshabilitar escritores en el sistema. | None                                                      | None                                                                                                                                                                                                                                                       |
| Opcionalmente, puede establecer el contexto de las operaciones de instantáneas y, opcionalmente, consultar el sistema sobre los proveedores y las instantáneas que admite (consulte [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | None                                                      | None                                                                                                                                                                                                                                                       |
| El solicitante puede proporcionar información adicional sobre el control de las operaciones de copia de seguridad y restauración (consulte [**IVssBackupComponents:: SetBackupState).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)                                                                                                                                                        | None                                                      | None                                                                                                                                                                                                                                                       |
| Inicia el contacto asincrónico con escritores (consulte [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).                                                                                                                                                                                           | [*Identificar*](vssgloss-i.md) | Crea un documento de metadatos de escritor (vea [trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md), [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |



 

## <a name="requester-actions-during-backup-initialization"></a>Acciones del solicitante durante la inicialización de la copia de seguridad

Un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) solo se puede usar para una copia de seguridad. Por lo tanto, un solicitante debe continuar hasta el final de la copia de seguridad, incluida la liberación de la interfaz **IVssBackupComponents** . Si la copia de seguridad debe finalizar prematuramente, el solicitante debe llamar a [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) y, a continuación, liberar el objeto **IVssBackupComponents** (consulte [anulación de operaciones de VSS](aborting-vss-operations.md) para más información). No intente reanudar la interfaz **IVssBackupComponents** .

Normalmente, el documento de componentes de copia de seguridad del solicitante se inicializa como vacío. Un documento almacenado de componentes de copia de seguridad se puede cargar cuando se llama a [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) , normalmente para la compatibilidad con volúmenes de instantáneas transportables. En este caso, la comunicación entre escritor y solicitante será algo diferente de lo que se describe a continuación. (Consulte [importación de volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md) para obtener más información).

Para agregar volúmenes al conjunto de instantáneas, un solicitante debe establecer primero el contexto de la operación de instantáneas llamando a [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Si no se llama a este método, se usa el contexto predeterminado para instantáneas, la copia de seguridad de VSS \_ CTX \_ . Para obtener información sobre cómo establecer el contexto de instantáneas, vea [configuraciones de contexto](shadow-copy-context-configurations.md)de instantáneas.

Para iniciar la instalación antes de realizar la copia de seguridad, un solicitante debe llamar a [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Al hacerlo, un solicitante indica a los escritores:

-   El tipo de copia de seguridad (tal y como se define en el [**\_ \_ tipo de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Si la copia de seguridad incluye un estado del sistema de arranque
-   Si el solicitante admite la selección de componentes individuales o realiza una copia de seguridad de volúmenes completos.

Todos los solicitantes que participan en las operaciones de copia de seguridad y restauración deben llamar siempre a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Este método inicia la comunicación del solicitante del escritor mediante la generación de un evento de [*identificación*](vssgloss-i.md) de VSS, en respuesta a la cual un escritor crea su documento de metadatos.

Antes de llamar a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un solicitante tiene la oportunidad de habilitar o deshabilitar explícitamente determinados escritores y clases de escritor específicos mediante [**IVssBackupComponents:: EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**Ivssbackupcomponents::D Isablewriterinstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)y [**IVssBackupComponents::D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (de forma predeterminada, todas las clases están habilitadas). Una vez que se llama a **IVssBackupComponents:: GatherWriterMetadata** , estas llamadas no tienen ningún efecto.

Dado que no hay ninguna manera de obtener una lista de escritores en el sistema antes de llamar a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), los solicitantes pueden considerar la creación y eliminación de una segunda instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para obtener la lista.

No es necesario llamar a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) después de la finalización de [**Ivssbackupcomponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Los escritores que no pueden procesar el evento de [*identificación*](vssgloss-i.md) generado por las llamadas no formarán parte de la lista de escritores que proporcionan los metadatos encontrados por [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) y [**ivssbackupcomponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [determinación del estado del escritor](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Acciones del escritor durante la inicialización de la copia de seguridad

En respuesta al evento de identificación, VSS llama al método de controlador virtual de cada escritor, [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify). Un escritor crea su documento de metadatos de escritor invalidando la implementación predeterminada de **CVssWriter:: he Identify** y usando la interfaz [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) .

Tenga en cuenta que las aplicaciones que no sean el solicitante actual (por ejemplo, aplicaciones del sistema) pueden generar eventos de identificación que deba controlar el escritor. Además, no hay ninguna manera de que un escritor determine desde dentro de [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qué aplicación ha generado el evento de identificación.

Este es el caso, dado que un escritor puede recibir varios eventos de identificación mientras se procesa una operación de copia de seguridad, un escritor nunca debe establecer información de estado en el controlador [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

En su lugar, [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) debe realizar un algoritmo coherente para crear el documento de metadatos del escritor del escritor, especialmente porque, después de que un escritor crea el documento, ni el solicitante ni el escritor pueden modificarlo. A partir de este punto, es un documento de solo lectura.

Esto significa que el número y tipo de [*componentes*](vssgloss-c.md) asociados a un escritor, los archivos que forman parte de cada componente y la exclusión explícita de los archivos de las operaciones de copia de seguridad o restauración no se pueden cambiar después de que un escritor vuelva de procesar el evento de identificación.

Todos los escritores que participan en VSS deben hacer lo siguiente:

1.  Indicar un método de restauración para todos los componentes administrados por el escritor mediante [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Agregue al menos un componente con [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (consulte [definición de componentes de escritores](definition-of-components-by-writers.md) para obtener más información sobre la especificación de componentes).

Un escritor indica los archivos que van a participar en una operación de copia de seguridad o restauración agregando [*conjuntos de archivos*](vssgloss-f.md)(una combinación de una ruta de acceso, especificación de archivo y una marca de recursividad) a un componente determinado mediante [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), dependiendo del tipo (vea [Agregar archivos a los componentes](definition-of-components-by-writers.md)).

Un escritor también puede tener uno o más componentes vacíos, componentes a los que no se ha agregado ningún archivo. Son muy útiles para organizar los componentes del escritor. (Consulte las [acciones lógicas de los componentes](logical-pathing-of-components.md)).

Un escritor utiliza [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) para impedir explícitamente que los archivos se incluyan en la copia de seguridad. Esta exclusión explícita es útil porque se pueden usar caracteres comodín para especificar archivos para su inclusión (vea la especificación de la [lista de exclusión de archivos](writer-metadata-document-contents.md)). Tenga en cuenta que la lista de archivos excluidos tiene prioridad sobre las listas de archivos de componentes.

[**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) se usa para crear [*asignaciones de ubicación alternativas*](vssgloss-a.md) para los conjuntos de archivos especificados que se han agregado a uno de los componentes del escritor. Estas asignaciones se utilizan durante la restauración de archivos cuando no es posible o desea restaurar en la ubicación original de un archivo. (Consulte [información general sobre la restauración de archivos real](overview-of-actual-file-restoration.md) y las [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md)).

Dado que el conjunto de archivos de copia de seguridad se especifica en el documento de metadatos del escritor, no se puede modificar más adelante. Por lo tanto, se debe codificar un escritor para que la definición del conjunto de archivos incluya todos los archivos necesarios en la copia de seguridad, ya sea por nombre o por caracteres comodín. Es posible que se incluyan algunos archivos que podrían crearse después del evento de identificación.

 

 



