---
description: Los solicitantes tienen la responsabilidad principal del ciclo de vida de un documento de componentes de copia de seguridad.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Ciclo de vida del documento componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124535"
---
# <a name="backup-components-document-life-cycle"></a>Ciclo de vida del documento componentes de copia de seguridad

Los solicitantes tienen la responsabilidad principal del ciclo de vida de un documento de componentes de copia de seguridad.

Este control lo controla una instancia del objeto de interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) devuelto por [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Un solicitante debe inicializar un documento de componentes de copia de seguridad antes de una copia de seguridad o restauración mediante una llamada a [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) o [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). El solicitante puede inicializar el documento como vacío o puede cargar una copia almacenada previamente del documento.

Para las operaciones de copia de seguridad, un documento de componentes de copia de seguridad normalmente se inicializa como vacío. Sus datos se rellenarán con la cooperación de los escritores del sistema durante el procesamiento de la copia de seguridad.

Para las operaciones de restauración, un documento de componentes de copia de seguridad normalmente se inicializa a partir de un documento almacenado generado durante la copia de seguridad inicial. Esto permite que la restauración (junto con el examen de los documentos de metadatos del escritor almacenados) determine qué datos se realizaron inicialmente y cómo se deben restaurar.

La copia de seguridad [*de instantáneas transportables*](vssgloss-t.md) es una excepción a esta regla. En este caso, una instantánea podría haber pasado de un sistema (donde se creó junto con el documento inicial de componentes de copia de seguridad) a otro mediante la reasignación de la unidad lógica de un dispositivo de almacenamiento compartido. Para realizar una copia de seguridad en estas circunstancias, un solicitante carga el estado de copia de seguridad almacenado y continúa desde donde lo dejó el sistema inicial. (Para obtener más información, vea [Importar volúmenes de instantáneas transportables).](importing-transportable-shadow-copied-volumes.md)

Durante el procesamiento de una copia de seguridad, el solicitante decide qué componentes copiar realmente en función de [](vssgloss-l.md)qué componentes se marcan como seleccionables para la copia de [*seguridad,*](vssgloss-s.md)las rutas de acceso lógicas del componente y su propia lógica interna.

Algunos de los componentes se [*incluirán explícitamente en*](vssgloss-e.md) la operación de copia de seguridad. se agregará información sobre el componente al documento Componentes de copia de seguridad. Otros se [*incluirán implícitamente en*](vssgloss-i.md) la copia de seguridad; No se agregará información sobre los componentes agregados al documento componentes de copia de seguridad.

Todos los componentes de copia de seguridad que no se pueden seleccionar de un escritor sin un antecesor seleccionable en su ruta de acceso lógica y los que se pueden seleccionar para los componentes de copia de seguridad que elija el solicitante se agregarán explícitamente.

Tanto los componentes de copia de seguridad no seleccionables como los seleccionables se pueden agregar implícitamente si tienen un antecesor seleccionable en su ruta de acceso lógica, que se incluye explícitamente en la copia de seguridad. Estos componentes ([*subcomponentes*](vssgloss-s.md)) son miembros de conjuntos [*de componentes*](vssgloss-s.md) definidos por su antecesor seleccionable.

Al controlar las operaciones de [](vssgloss-s.md) restauración, el solicitante usa la capacidad de selección para la restauración en lugar de la capacidad de selección para la copia de seguridad junto con la información de ruta de acceso lógica y su propia lógica interna para decidir qué archivos restaurar.

Si un componente que se había agregado implícitamente a la copia de seguridad ahora se va a agregar explícitamente a la restauración, el solicitante actualizará el documento de componentes de copia de seguridad con la información de ese componente.

La información sobre los componentes almacenados está disponible tanto para los solicitantes como para los escritores a través de instancias de la [**interfaz IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Es a través de las interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que los escritores pueden consultar y (hasta el final de los eventos [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) y [**PostRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) modificar información en el documento componentes de copia de seguridad.

Cuando se llama al controlador de eventos [**CVssWriter::OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter::OnPostSnapshot,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)o [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) un escritor recibe una instancia de una [**interfaz IVssWriterComponents.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

Tenga en cuenta que, tras la generación del evento [**BackupComplete,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) el documento de componentes de copia de seguridad se hace de solo lectura y, por tanto, [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) no puede usar la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para modificarlo.

Desde la [**interfaz IVSSWriterComponents,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) el escritor puede recuperar instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que le permitirán tener acceso a todos sus componentes agregados explícitamente al documento componentes de copia de seguridad y modificar su estado. Para obtener más información, vea Información general sobre el procesamiento de una copia de [seguridad en VSS](overview-of-processing-a-backup-under-vss.md) e Información general sobre el procesamiento de una [restauración en VSS.](overview-of-processing-a-restore-under-vss.md)

Los documentos de componentes de copia de seguridad se quitan de la memoria cuando se libera la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y se deben almacenar mediante [**IVssBackupComponents::SaveAsXML,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)o bien se perderá toda su información.

Además, cuando se publica correctamente un documento [**IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se genera un evento [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) y se eliminan las instantáneas [*de*](vssgloss-a.md) versión automática.

 

 



