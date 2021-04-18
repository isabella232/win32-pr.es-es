---
description: Los solicitantes tienen la responsabilidad principal del ciclo de vida de un documento de componentes de copia de seguridad.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Ciclo de vida de documentos de componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bcb0263f46466d7be2bc19f3c8809167b2da08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697792"
---
# <a name="backup-components-document-life-cycle"></a>Ciclo de vida de documentos de componentes de copia de seguridad

Los solicitantes tienen la responsabilidad principal del ciclo de vida de un documento de componentes de copia de seguridad.

Este control lo ejercita una instancia del objeto de interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) devuelto por [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Un solicitante debe inicializar un documento de componentes de copia de seguridad antes de realizar una copia de seguridad o una restauración mediante una llamada a [**ivssbackupcomponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) o [**Ivssbackupcomponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). El solicitante puede inicializar el documento como vacío o puede cargar una copia almacenada previamente del documento.

En el caso de las operaciones de copia de seguridad, un documento de componentes de copia de seguridad se inicializa normalmente como vacío. Sus datos se rellenarán con la cooperación de los escritores del sistema durante el procesamiento de la copia de seguridad.

En el caso de las operaciones de restauración, un documento de componentes de copia de seguridad se inicializa normalmente a partir de un documento almacenado generado durante la copia de seguridad inicial. Esto permite la restauración (junto con el examen de los documentos de metadatos del escritor almacenados) para determinar en qué datos se hizo una copia de seguridad inicialmente y cómo debe restaurarse.

La realización de copias de seguridad de las [*instantáneas transportables*](vssgloss-t.md) es una excepción a esta regla. En este caso, es posible que se haya pasado una instantánea de un sistema (donde se creó junto con el documento de componentes de copia de seguridad inicial) a otro por medio de la reasignación de la unidad lógica de un dispositivo de almacenamiento compartido. Para realizar una copia de seguridad en estas circunstancias, un solicitante carga el estado de copia de seguridad almacenado y continúa desde donde se quedó el sistema inicial. (Para obtener más información, vea [importar volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md)).

En el transcurso del procesamiento de una copia de seguridad, el solicitante decide qué componentes se deben copiar realmente en función de qué componentes están marcados como [*seleccionables para la copia de seguridad*](vssgloss-s.md), las rutas de acceso [*lógicas*](vssgloss-l.md)del componente y su propia lógica interna.

Algunos de los componentes se [*incluirán explícitamente*](vssgloss-e.md) en la operación de copia de seguridad; la información sobre el componente se agregará al documento componentes de copia de seguridad. Otros se [*incluirán implícitamente*](vssgloss-i.md) en la copia de seguridad; la información sobre los componentes agregados no se agregará al documento componentes de copia de seguridad.

Todas las opciones no seleccionables de un escritor para los componentes de copia de seguridad sin un antecesor seleccionable en su ruta de acceso lógica, y las que seleccionan los componentes de copia de seguridad que elige el solicitante, se agregan explícitamente.

Los componentes de copia de seguridad no seleccionables y seleccionables se pueden agregar implícitamente si tienen un antecesor seleccionable en su ruta de acceso lógica, que se incluye explícitamente en la copia de seguridad. Estos componentes ([*subcomponentes*](vssgloss-s.md)) son miembros de los [*conjuntos de componentes*](vssgloss-s.md) definidos por su antecesor seleccionable.

Al controlar las operaciones de restauración, el solicitante usa la [*selección de la restauración*](vssgloss-s.md) en lugar de la selección para la copia de seguridad junto con la información de ruta de acceso lógica y su propia lógica interna para decidir qué archivos se van a restaurar.

Si un componente que se ha agregado implícitamente a la copia de seguridad ahora se va a agregar explícitamente a la restauración, el solicitante actualizará el documento de componentes de copia de seguridad con la información de ese componente.

La información sobre los componentes almacenados está disponible para los solicitantes y escritores a través de instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Es a través de las interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que los escritores pueden consultar y (hasta el final de los eventos [**postsnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) y [**postrestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) ) modificar la información del documento componentes de copia de seguridad.

Cuando se llama al controlador de eventos [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)o [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) , un escritor recibe una instancia de una interfaz [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) .

Tenga en cuenta que, tras la generación del evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , el documento componentes de copia de seguridad se convierte en solo lectura y, por lo tanto, [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) no puede usar la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para modificarlo.

Desde la interfaz [**IVSSWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) , el escritor puede recuperar instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que le permitirá tener acceso a todos sus componentes agregados explícitamente al documento componentes de copia de seguridad y modificar su estado. Para obtener más información, vea información [General sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md) e [información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md).

Los documentos de componentes de copia de seguridad se quitan de la memoria cuando se libera la interfaz [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y deben almacenarse mediante [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml), o toda su información se perderá.

Además, cuando un documento [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se libera correctamente, se genera un evento [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) y se eliminan las [*instantáneas de liberación automática*](vssgloss-a.md) .

 

 



