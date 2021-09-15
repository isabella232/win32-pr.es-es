---
description: Al inicializar una operación de restauración de VSS, un solicitante debe recuperar el documento del componente de copia de seguridad y cada documento de metadatos de escritor pertinente creado y guardado durante la operación de copia de seguridad.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Información general sobre la inicialización de restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb62e5282a74e38cd53d36c8ba004f4b8069746
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473365"
---
# <a name="overview-of-restore-initialization"></a>Información general sobre la inicialización de restauración

Al inicializar una operación de restauración de VSS, un solicitante debe recuperar el documento del componente de copia de seguridad y cada documento de metadatos de escritor pertinente creado y guardado durante la operación de copia de seguridad. El sistema de escritura tendrá su estado actual al controlar el [*evento Identify*](vssgloss-i.md) que genera el solicitante. Para obtener más información, vea [Información general sobre el procesamiento de una restauración en VSS.](overview-of-processing-a-restore-under-vss.md)

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para inicializar una operación de restauración.



| Acción del solicitante                                                                                                                                                                                                                                                                                                       | Evento                                                     | Acción del escritor                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cree una [**interfaz IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) inicialízcala para administrar una restauración y cargue los metadatos del solicitante almacenados (vea [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForRestore).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) | None                                                      | None                                                                                                                                                                                                                                                                                                                      |
| Llame [**a CreateVssExgvWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para crear [**interfaces IVssExwriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) y cargarlas con metadatos de escritor almacenados.                                                                                                           | None                                                      | None                                                                                                                                                                                                                                                                                                                      |
| Inicie el contacto asincrónico con los escritores (vea [**IVssBackupComponents::GatherWriterMetadata).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)                                                                                                                                                                      | [*Identificar*](vssgloss-i.md) | El escritor comienza el control de eventos en apoyo de la restauración. Crea el documento de metadatos del escritor (vea Trabajar con el documento [de](working-with-the-writer-metadata-document.md)metadatos del escritor , [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| El solicitante espera a que los escritores se inicialicen mediante una [**llamada a IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync).                                                                                                                                                                                                                               | None                                                      | None                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Acciones del solicitante durante la inicialización de la restauración

Durante la fase de inicialización de una restauración, el solicitante debe tener acceso al documento de componentes de copia de seguridad almacenado y a todos los documentos de metadatos del escritor.

Dependiendo de la implementación, esto significará que el solicitante requerirá que los medios de copia de seguridad estén montados y legibles, o que algún otro mecanismo para acceder a los metadatos almacenados esté disponible.

El solicitante usa el documento XML almacenado que contiene el documento de componentes de copia de seguridad del solicitante que realizó la copia de seguridad para inicializar su documento de componentes de copia de seguridad mediante [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) puede acceder a la información.

Como era el caso durante la copia de seguridad, el documento componentes de copia de seguridad no tiene información suficiente para admitir una restauración. Por lo tanto, el solicitante necesita acceso a los documentos de metadatos del escritor almacenados durante la copia de seguridad (vea Uso de [componentes por parte del solicitante).](use-of-components-by-the-requestor.md)

El solicitante recupera los metadatos de escritor almacenados mediante una llamada a [**CreateVssExgvWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para cada escritor cuyos datos se realizaron de copia de seguridad y ahora se restaurarán. Esta función crea un [**objeto IVssExgvWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para cada escritor y carga el documento de metadatos del escritor en el objeto .

Como era el caso durante la copia de seguridad, para iniciar la cooperación entre sí y los escritores del sistema, un solicitante debe generar un evento [*Identify*](vssgloss-i.md) llamando a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). No es necesario llamar a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) después de la finalización de [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Los escritores que no puedan procesar el evento [*Identify*](vssgloss-i.md) no se incluirán en la lista de escritores que proporcionan los metadatos que [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vea [Determinar](determining-writer-status.md)el estado del escritor).

Al igual que con la operación de copia de seguridad, un solicitante deberá consultar y analizar la información del documento Componentes de copia de seguridad [](overview-of-preparing-for-restore.md)y compararla con los datos de los documentos de metadatos del escritor para determinar qué componentes se han hecho copias de seguridad y elegir los que se van a restaurar (consulte Información general sobre la preparación para la restauración). Además, el solicitante deberá generar una lista detallada que contenga información sobre los archivos del medio de copia de seguridad seleccionado para la restauración, así como cómo y dónde se van a restaurar. (Vea [Generar un conjunto de restauración).](generating-a-restore-set.md)

Por lo tanto, algunas aplicaciones de copia de seguridad pueden resultar útiles haber almacenado en el medio de copia de seguridad su propia lista (en su propio formato optimizado) de los archivos y su escritor, componente, procedimiento de restauración e información de ubicación asociados. Esta lista se puede usar para minimizar la cantidad de análisis y comparación de los documentos de metadatos del escritor y los documentos de componente de copia de seguridad necesarios para admitir una restauración.

## <a name="writer-actions-during-restore-initialization"></a>Acciones de escritor durante la inicialización de la restauración

Igual que se hace durante una operación de restauración, en respuesta al evento Identify, VSS llama al método de controlador virtual de cada escritor [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify).

Tenga en cuenta que las aplicaciones que no sean el solicitante actual (por ejemplo, las aplicaciones del sistema) pueden generar eventos De identificación, que debe controlar el escritor. Además, no hay ninguna manera de que un escritor determine desde [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qué aplicación ha generado el evento Identify.

Dado que un escritor puede recibir varios eventos Identify durante el procesamiento de una operación de restauración, los escritores nunca deben establecer información de estado en el [**controlador CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) En su lugar, deben usar el mismo algoritmo para crear su [](overview-of-backup-initialization.md) documento de metadatos del escritor que se hizo durante las operaciones de copia de seguridad (vea Acciones de escritura durante la inicialización de copia de seguridad para obtener más información).

 

 



