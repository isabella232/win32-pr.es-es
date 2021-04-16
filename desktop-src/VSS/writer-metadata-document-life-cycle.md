---
description: 'En respuesta a un evento de identificación, cada escritor presente en el sistema construye su propio documento de metadatos de escritor mediante IVssCreateWriterMetadata. Un solicitante suele generar un evento de identificación que llama a IVssBackupComponents:: GatherWriterMetadata.'
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo de vida de documento de metadatos de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45be5748625d21f99abe3e77e0d6474a62210904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696423"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo de vida de documento de metadatos de escritor

En respuesta a un [*evento de identificación*](vssgloss-i.md), cada escritor presente en el sistema construye su propio documento de metadatos de escritor mediante [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Un solicitante suele generar un *evento de identificación* que llama a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Al crear un documento de metadatos de escritor, ya sea a través de la interfaz [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) o a través de la inicialización del escritor ([**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), un escritor debe especificar explícitamente lo siguiente:

-   [*Método de restauración*](vssgloss-r.md)
-   Nombre del escritor
-   [*IDENTIFICADOR de clase del escritor*](vssgloss-w.md)
-   Uso de datos ( [**consulte \_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo de origen de fecha (consulte [**\_ \_ tipo de origen de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Además, también puede especificar lo siguiente:

-   Componentes (que pueden contener o no conjuntos de archivos)
-   Agregar asignaciones alternativas
-   Excluir listas de archivos

Se encontró una introducción a la creación de documentos de metadatos de escritura en [acciones del escritor durante la inicialización](overview-of-backup-initialization.md)de la copia de seguridad.

Los solicitantes suelen usar uno de los dos métodos para obtener acceso a los metadatos del escritor:

-   Durante la mayoría de las operaciones de copia de seguridad, un solicitante usa [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obtener una instancia de la interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para permitir el acceso a los metadatos de un escritor que se ejecuta actualmente.
-   En el caso de las operaciones de restauración o las copias de seguridad con instantáneas importadas (consulte [importación de volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md) para obtener más información sobre la importación de instantáneas), un solicitante recupera un documento XML que contiene los metadatos y usa [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para obtener una interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , que usa para leer los metadatos de restauración.

Los documentos de metadatos de escritor permiten que el solicitante realice una copia de seguridad para obtener información acerca de los escritores que se ejecutan actualmente durante la fase de detección de una copia de seguridad.

En el caso de los escritores elegidos para participar en una copia de seguridad, un solicitante importa gran parte de la información del documento de metadatos del escritor a su propio documento de componentes de copia de seguridad durante la fase de detección de una copia de seguridad.

Sin embargo, solo los documentos de metadatos de escritor y no el documento de componentes de copia de seguridad contienen las especificaciones de archivo y ruta de acceso.

Para obtener más información sobre cómo se realiza la fase de detección de una operación de copia de seguridad, vea [información general sobre la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md).

Además, solo los componentes [*incluidos explícitamente*](vssgloss-e.md) tienen su información almacenada en el documento componentes de copia de seguridad durante una operación de copia de seguridad. La información sobre componentes [*incluidos implícitamente*](vssgloss-i.md) no se incluye en el documento componentes de copia de seguridad durante una operación de copia de seguridad y se debe interpolar con información sobre los componentes incluidos explícitamente y los documentos de metadatos de escritura disponibles.

Los componentes incluidos implícitamente pueden seguir siendo [*seleccionables para la restauración*](vssgloss-s.md) y es posible que deban incluirse explícitamente en el documento componentes de copia de seguridad en el momento de la restauración. En este caso, al igual que cuando se agrega un componente durante una operación de copia de seguridad, se necesita acceso al documento de metadatos del escritor de writer's del componente (que luego se recupera del escritor), un solicitante necesitará acceso a una copia de los documentos de metadatos del escritor del escritor almacenados en el momento de la copia de seguridad.

Por lo tanto, la única manera de obtener toda la información sobre todos los archivos y componentes implicados en una copia de seguridad o restauración es tener cada documento de metadatos de escritor para cada escritor que participa en una copia de seguridad almacenada junto con el documento componentes de copia de seguridad. (Para obtener más información, vea [información general de la restauración de archivos real](overview-of-actual-file-restoration.md)).

 

 



