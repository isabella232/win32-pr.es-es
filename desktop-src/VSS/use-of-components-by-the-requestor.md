---
description: Además de realizar una copia de seguridad o restauración, y supervisar instantáneas, un solicitante debe administrar información sobre los componentes de los escritores con los que interactúa.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Uso de componentes por parte del solicitante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3149800a3f8cb52afff044e593f6b01177b27054c64a2ee19c19cb570ed633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998085"
---
# <a name="use-of-components-by-the-requester"></a>Uso de componentes por parte del solicitante

Además de realizar una copia de seguridad o restauración, y supervisar instantáneas, un solicitante debe administrar información sobre los componentes de los escritores con los que interactúa. La selección de componentes y la ruta de acceso lógica se usan para incluir o excluir datos de una copia de seguridad y para decidir qué información de componente se incluye en el documento Componentes de copia de seguridad.

## <a name="requester-component-selection-during-backup"></a>Selección de componentes del solicitante durante la copia de seguridad

Durante las operaciones de copia de seguridad, un solicitante importa los datos del componente de metadatos de escritor mediante los [](overview-of-backup-initialization.md) [**métodos IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte Información general sobre la inicialización de copia de seguridad para obtener más información).

Después de examinar la información del sistema de escritura con la interfaz [**IVssExgvWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) un solicitante decide los escritores de los que se va a realizar una copia de seguridad y, en una medida limitada, cuáles de los componentes de un escritor determinado copiarán de seguridad.

Al hacer una copia de seguridad de un escritor, un solicitante:

-   Debe [*incluir explícitamente*](vssgloss-e.md) todos los componentes de copia de seguridad no seleccionables de un escritor sin seleccionarlos para los antecesores de copia de seguridad mediante [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar el componente al documento Componentes de copia de seguridad
-   Puede incluir explícitamente cualquiera de los componentes de copia de seguridad seleccionables de un escritor [**mediante IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar el componente al documento Componentes de copia de seguridad.
-   Si un componente seleccionable para copia de [](vssgloss-i.md) seguridad define un conjunto de componentes [*,*](vssgloss-c.md)su inclusión explícita incluye implícitamente todos los miembros del conjunto de componentes, tanto si se puede seleccionar para la copia de seguridad como si no. Estos componentes no se agregan al documento Componentes de copia de seguridad.

Al agregar un componente seleccionable para copia de seguridad o un no seleccionable para los componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad a su documento componentes de copia de seguridad, un solicitante especifica lo siguiente:

-   Instancia del escritor que administra el componente
-   Identificador de clase del escritor
-   Ruta [*de acceso*](vssgloss-l.md) lógica del componente (que puede ser **NULL)**
-   Nombre del componente

Si un componente no coincide con la especificación, se devolverá un error.

Si existe este componente, VSS crea una [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para el componente en el documento Componentes de copia de seguridad. Esta información será accesible y modificable por el escritor y el solicitante. Para un componente seleccionable que define [*un*](vssgloss-c.md)conjunto de componentes , describe no solo las propiedades del componente, sino también todos los subcomponentes que contiene.

La información sobre los componentes agregados implícitamente no está disponible en el documento Componentes de copia de seguridad. Además, no hay información de archivo disponible en el documento Componentes de copia de seguridad. Para obtener esa información, el solicitante tendrá que examinar los documentos de metadatos del escritor (que ya se habrán leído) en el contexto de los componentes almacenados seleccionados en el documento Componentes de copia de seguridad.

## <a name="requester-component-selection-during-restore"></a>Selección de componentes del solicitante durante la restauración

Durante las operaciones de restauración, un solicitante no debe importar información de componentes de los escritores actualmente activos en el sistema a través de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), porque el estado de los procesos que se están ejecutando actualmente no reflejará necesariamente el estado de los procesos cuando se realizó una copia de seguridad.

Todavía debe generar un evento [*Identify*](vssgloss-i.md) a través de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), tanto para crear un evento *Identify* como para determinar qué escritores están actualmente en el sistema y su estado.

El solicitante recupera el documento de componentes de copia de seguridad almacenado durante su inicialización, así como los documentos de metadatos del escritor almacenados (vea [Información](overview-of-restore-initialization.md) general de inicialización de restauración para obtener más información).

La inclusión de componentes durante la copia de seguridad es [](vssgloss-s.md) en gran medida la misma que para la restauración, salvo que debe considerar la posibilidad de seleccionarla para la restauración junto con la ruta de acceso lógica [*,*](vssgloss-l.md)no seleccionable para la copia [*de seguridad.*](vssgloss-s.md)

Sin embargo, hay algunas diferencias:

-   Si un componente [](vssgloss-e.md) ya se ha incluido explícitamente en el documento componentes de copia de seguridad durante la copia de seguridad, si se incluye para la restauración (explícita o implícitamente), se usa [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) para agregarlo explícitamente al documento componentes de copia de seguridad para la restauración.
-   Si un [](vssgloss-i.md) componente se incluyó implícitamente en la copia de seguridad y no se puede seleccionar para la restauración sin ningún elemento seleccionable para los antecesores de restauración (lo que en el caso de la copia de seguridad implicaría la necesidad de inclusión explícita), el componente no se incluye explícitamente (es decir, no se agrega al documento Componentes de copia de seguridad mediante [**IVssBackupComponents::SetSelectedForRestore).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) Este componente debe considerarse seleccionado implícitamente para la restauración.
-   De esos componentes seleccionados implícitamente para la copia de seguridad (independientemente de si ese componente se puede seleccionar para la copia de seguridad o no), solo los que se pueden seleccionar para la restauración se pueden agregar al documento Componentes de copia de seguridad mediante [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Seleccionar los componentes de restauración puede definir un [*conjunto de componentes*](vssgloss-c.md) para la restauración, del mismo modo que se puede seleccionar para los componentes de copia de seguridad. Este componente seleccionable para restaurar define este conjunto de componentes para la operación de restauración.

Un escritor sin componentes seleccionados explícitamente para la restauración antes de la generación de un evento [*PreRestore*](vssgloss-p.md) no recibirá ningún evento de VSS.

Los solicitantes y escritores pueden acceder a la información de componentes almacenada mediante la [**interfaz IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) A través de la **interfaz IVssComponent,** los escritores pueden modificar parte de la configuración de los componentes incluidos explícitamente en el documento Componentes de copia de seguridad para admitir una restauración (por ejemplo, el destino de [*restauración*](vssgloss-r.md)). Si define un conjunto de componentes, las modificaciones de escritura de un componente incluido explícitamente se propagarán a sus [*subcomponentes*](vssgloss-s.md). Además, la interfaz proporciona un mecanismo para pasar información sobre el éxito y el error de restauración entre el escritor y el solicitante.

Al igual que durante la copia de seguridad, no hay suficiente información en el propio documento componentes de copia de seguridad para implementar la restauración. De nuevo, los documentos de metadatos del escritor tendrán que proporcionar información sobre las rutas de acceso reales de los archivos que se van a restaurar y detectar qué componentes no seleccionables forman parte del conjunto de componentes seleccionables y, por tanto, deben restaurarse.

Consulte [Working with Selectability and Logical Paths (Trabajar con selectability y rutas de acceso lógicas)](working-with-selectability-and-logical-paths.md) para obtener información sobre los tipos de selectability y su uso.

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Uso de la información del documento del componente escritor por parte del solicitante

Cada componente se identifica de forma única mediante el [*identificador de clase writer*](vssgloss-w.md) de su sistema de escritura primario, su nombre y su ruta de acceso [*lógica.*](vssgloss-l.md)

El solicitante puede usar la [**interfaz IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por el método [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) para obtener información sobre cada componente almacenado.

El nombre del componente y la ruta de acceso lógica (entre otros elementos) se pueden encontrar a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) devuelta por [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Durante la fase de restauración, el solicitante debe llamar a [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) o [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) solo después de que se haya devuelto la llamada [**a IVssBackupComponents::P reRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) para permitir que el escritor actualice el documento de componentes de copia de seguridad. Un ejemplo de esta actualización sería cambiar el destino de restauración.

 

Puede encontrar información sobre el sistema de escritura primario de cada componente seleccionable almacenado mediante [**IVssWriterComponentsExt::GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Con esta información, se pueden consultar los documentos de metadatos del escritor y identificar el documento correspondiente. A continuación, mediante la ruta de acceso lógica [*,*](vssgloss-l.md)el solicitante puede identificar los componentes dependientes no seleccionables para cada componente seleccionable, es decir, identificar todos los miembros del conjunto de componentes del componente [*seleccionable*](vssgloss-c.md).

Con la interfaz [**IVssExgvWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) el solicitante ahora tiene información completa del componente (incluida la especificación de ruta de acceso (de la interfaz [**IVssWMComponent)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) para los componentes seleccionables y no seleccionables de los que necesita hacer una copia de seguridad o restaurar.

Este es un motivo por el que es fundamental que un solicitante guarde tanto el estado de su propio documento de componentes de copia de seguridad como los documentos de metadatos del escritor de los escritores de los que está haciendo una copia de seguridad.

Consulte [Working with Selectability and Logical Paths (Trabajar con la capacidad de selección y las rutas de acceso lógicas)](working-with-selectability-and-logical-paths.md) para obtener información más detallada.

 

 
