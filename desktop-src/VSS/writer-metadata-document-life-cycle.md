---
description: En respuesta a un evento Identify, cada escritor presente en el sistema construye su propio documento de metadatos del escritor mediante IVssCreateWriterMetadata. Normalmente, un solicitante que llama a IVssBackupComponents::GatherWriterMetadata genera un evento Identify.
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo de vida del documento de metadatos del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2796d1a7b995f13829ac81485f74fa342bebe5e0e312b7b014d761a9962aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121579"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo de vida del documento de metadatos del escritor

En respuesta a un [*evento Identify*](vssgloss-i.md), cada escritor presente en el sistema construye su propio documento de metadatos del escritor [**mediante IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Normalmente, un solicitante que llama a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)genera un evento *Identify.*

Al crear un documento de metadatos del escritor, ya sea a través de la interfaz [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) o mediante la inicialización del escritor [**(CVssWriter::Initialize),**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)un escritor debe especificar explícitamente lo siguiente:

-   [*Método de restauración*](vssgloss-r.md)
-   Nombre del escritor
-   [*Identificador de clase de escritor*](vssgloss-w.md)
-   Uso de datos (vea [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo de origen de fecha (vea [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Además, también puede especificar lo siguiente:

-   Componentes (que pueden o no contener conjuntos de archivos)
-   Agregar asignaciones alternativas
-   Excluir listas de archivos

Puede encontrar información general sobre la creación del documento de metadatos del escritor en [Acciones de escritura durante la inicialización de la copia de seguridad.](overview-of-backup-initialization.md)

Normalmente, los solicitantes usan uno de estos dos métodos para obtener acceso a los metadatos del escritor:

-   Durante la mayoría de las operaciones de copia de seguridad, un solicitante usa [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obtener una instancia de la interfaz [**IVssExgvWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para permitir el acceso a los metadatos de un escritor que se está ejecutando actualmente.
-   Para operaciones de restauración o copias de seguridad que usan instantáneas importadas (vea Importar volúmenes de instantáneas [transportables](importing-transportable-shadow-copied-volumes.md) para obtener más información sobre la importación de instantáneas), un solicitante recupera un documento XML que contiene los metadatos y usa [**CreateVssEx backupsWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para obtener una interfaz [**IVssExrestablecimientoWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) que usa para leer los metadatos de restauración.

Los documentos de metadatos del escritor permiten al solicitante realizar una copia de seguridad para obtener información sobre los escritores que se ejecutan actualmente durante la fase de detección de una copia de seguridad.

Para los escritores elegidos para participar en una copia de seguridad, un solicitante importa gran parte, pero no toda, de la información del documento de metadatos del escritor en su propio documento de componentes de copia de seguridad durante la fase de detección de una copia de seguridad.

Sin embargo, solo los documentos de metadatos del escritor y no el documento de componentes de copia de seguridad contienen las especificaciones de archivo y ruta de acceso.

Para obtener más información sobre cómo se lleva a cabo la fase de detección de una operación de copia de seguridad, consulte Información general de la fase de detección [de copia de seguridad](overview-of-the-backup-discovery-phase.md).

Además, solo los [*componentes incluidos explícitamente*](vssgloss-e.md) tienen su información almacenada en el documento componentes de copia de seguridad durante una operación de copia de seguridad. La información sobre [*los*](vssgloss-i.md) componentes incluidos implícitamente no se incluye en el documento componentes de copia de seguridad durante una operación de copia de seguridad y se debe interpolar con información sobre los componentes incluidos explícitamente y los documentos de metadatos del escritor disponibles.

Los componentes incluidos [](vssgloss-s.md) implícitamente pueden seguir siendo seleccionables para la restauración y es posible que deba incluirse explícitamente en el documento componentes de copia de seguridad en el momento de la restauración. En este caso, al igual que agregar un componente durante una operación de copia de seguridad requería acceso al documento de metadatos del escritor del componente (que luego se recupera del escritor), un solicitante requerirá acceso a una copia de los documentos de metadatos del escritor almacenados en el momento de la copia de seguridad.

Por lo tanto, la única manera de obtener toda la información sobre todos los archivos y componentes implicados en una copia de seguridad o restauración es hacer que cada documento de metadatos del escritor participe en una copia de seguridad almacenada junto con el documento de componentes de copia de seguridad. (Para obtener más información, vea [Información general sobre la restauración real de archivos).](overview-of-actual-file-restoration.md)

 

 



