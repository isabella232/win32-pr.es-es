---
description: Además de realizar una copia de seguridad o una restauración, y supervisar las instantáneas, un solicitante debe administrar la información sobre los componentes de los sistemas de escritura con los que interactúa.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Uso de componentes por parte del solicitante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83efdb9e80ac0331289c3b611978e66a58098de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541766"
---
# <a name="use-of-components-by-the-requester"></a>Uso de componentes por parte del solicitante

Además de realizar una copia de seguridad o una restauración, y supervisar las instantáneas, un solicitante debe administrar la información sobre los componentes de los sistemas de escritura con los que interactúa. La selección de componentes y la ruta de acceso lógica se usan para incluir o excluir datos de una copia de seguridad, y para decidir qué información de componente se incluye en el documento componentes de copia de seguridad.

## <a name="requester-component-selection-during-backup"></a>Selección del componente solicitante durante la copia de seguridad

Durante las operaciones de copia de seguridad, un solicitante importa los datos del componente de metadatos del escritor mediante los métodos [**ivssbackupcomponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) y [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [información general de la inicialización de copia de seguridad](overview-of-backup-initialization.md) para obtener más información).

Después de examinar la información del escritor con la interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , un solicitante decide en qué escritores se realizará la copia de seguridad y, en un grado limitado, de los componentes de un escritor determinado de los que se realizará la copia de seguridad.

Al realizar una copia de seguridad de un escritor, un solicitante:

-   Debe [*incluir explícitamente*](vssgloss-e.md) el elemento no seleccionable de un escritor para los componentes de copia de seguridad sin seleccionar los antecesores de copia de seguridad mediante [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar el componente al documento componentes de copia de seguridad.
-   Puede incluir explícitamente cualquiera de las opciones seleccionables del escritor para componentes de copia de seguridad mediante [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar el componente al documento componentes de copia de seguridad.
-   Si un componente seleccionable para copia de seguridad define un [*conjunto de componentes*](vssgloss-c.md), su inclusión explícita [*incluye implícitamente*](vssgloss-i.md) todos los miembros del conjunto de componentes, ya sea seleccionable para copia de seguridad o no. Estos componentes no se agregan al documento componentes de copia de seguridad.

En agregar un componente seleccionable para copia de seguridad o una no seleccionable para componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad en su documento de componentes de copia de seguridad, un solicitante especifica lo siguiente:

-   Instancia del escritor que administra el componente.
-   Identificador de clase del escritor.
-   [*Ruta de acceso lógica*](vssgloss-l.md) del componente (que puede ser **null**).
-   Nombre del componente

Si un componente no coincide con la especificación, se devolverá un error.

Si existe este componente, VSS crea una interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para el componente en el documento componentes de copia de seguridad. Esta información será accesible y modificable por el escritor y el solicitante. Para un componente seleccionable que define un [*conjunto de componentes*](vssgloss-c.md), describe no solo las propiedades del componente, sino también todos los subcomponentes que contiene.

La información sobre los componentes agregados implícitamente no está disponible en el documento componentes de copia de seguridad. Además, no hay información de archivo disponible en el documento componentes de copia de seguridad. Para obtener esa información, el solicitante tendrá que examinar los documentos de metadatos del escritor (que ya se habrán leído) en el contexto de los componentes almacenados seleccionados en el documento componentes de copia de seguridad.

## <a name="requester-component-selection-during-restore"></a>Selección del componente solicitante durante la restauración

Durante las operaciones de restauración, un solicitante no debe importar información de componentes de los escritores actualmente activos en el sistema a través de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), porque el estado de los procesos que se están ejecutando actualmente no reflejará necesariamente el estado de los procesos cuando se realizó una copia de seguridad.

Todavía debe generar un [*evento de identificación*](vssgloss-i.md) mediante [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), ambos para crear un *evento de identificación* y determinar qué escritores están actualmente en el sistema y su estado.

El solicitante recupera el documento de componentes de copia de seguridad almacenado durante su inicialización, así como los documentos de metadatos del escritor almacenados (consulte [información general de la inicialización de restauración](overview-of-restore-initialization.md) para obtener más información).

La inclusión de componentes durante la copia de seguridad es en gran medida la misma que para la restauración, salvo que debe considerar [*Selectable para la restauración*](vssgloss-s.md) junto con la [*ruta de acceso lógica*](vssgloss-l.md); no se puede [*seleccionar para la copia de seguridad*](vssgloss-s.md).

Sin embargo, hay algunas diferencias:

-   Si un componente ya se [*incluyó explícitamente*](vssgloss-e.md) en el documento de componentes de copia de seguridad durante la copia de seguridad, si se incluye para la restauración (ya sea de forma explícita o implícita), se utiliza [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) para agregarlo explícitamente al documento de componentes de copia de seguridad para su restauración.
-   Si un componente se [*incluyó implícitamente*](vssgloss-i.md) en la copia de seguridad y no es seleccionable para la restauración sin selección para restaurar antecesores, lo que en el caso de la copia de seguridad implicaría la necesidad de una inclusión explícita, el componente no se incluye explícitamente (es decir, no se agrega al documento componentes de copia de seguridad mediante [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)). Este componente se debe considerar como seleccionado implícitamente para la restauración.
-   De esos componentes seleccionados implícitamente para la copia de seguridad (si ese componente se puede seleccionar para la copia de seguridad o no), solo se pueden agregar al documento componentes de copia de seguridad los elementos que se pueden seleccionar para restaurar mediante [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Selectable for restore Components puede definir un [*conjunto de componentes*](vssgloss-c.md) para la restauración, tal y como se puede seleccionar para los componentes de copia de seguridad. Este componente seleccionable para restauración define este conjunto de componentes para la operación de restauración.

Un escritor sin componentes seleccionados explícitamente para la restauración antes de la generación de un evento de [*prerestauración*](vssgloss-p.md) no recibirá ningún evento de VSS.

Los solicitantes y escritores pueden acceder a la información de los componentes almacenados mediante la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . A través de la interfaz **IVssComponent** , los escritores pueden modificar algunas de las opciones de los componentes incluidos explícitamente en el documento componentes de copia de seguridad para admitir una restauración (como el [*destino de restauración*](vssgloss-r.md)). Si define un conjunto de componentes, las modificaciones del escritor de un componente incluido explícitamente se propagarán a sus [*subcomponentes*](vssgloss-s.md). Además, la interfaz proporciona un mecanismo para pasar información sobre la restauración correcta y errónea entre el escritor y el solicitante.

Al igual que durante la copia de seguridad, no hay suficiente información en el documento componentes de copia de seguridad para implementar la restauración. De nuevo, los documentos de metadatos del escritor deberán proporcionar información sobre las rutas de acceso reales de los archivos que se van a restaurar y detectar qué componentes no seleccionables forman parte del conjunto de componentes seleccionables y, por lo tanto, deben restaurarse.

Vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md) para obtener información sobre los tipos de selección y su uso.

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Uso de la información del documento del componente de escritor por parte del solicitante

Cada componente se identifica de forma única mediante el [*identificador de clase del escritor*](vssgloss-w.md) de su escritor primario, su nombre y su ruta de [*acceso lógica*](vssgloss-l.md).

El solicitante puede usar la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por el método [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) para obtener información sobre cada componente almacenado.

El nombre del componente y la ruta de acceso lógica (entre otros elementos) se pueden encontrar a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) devuelta por [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Durante la fase de restauración, el solicitante debe llamar a [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) o [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) solo después de que se haya devuelto la llamada a [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , para dejar tiempo a que el escritor actualice el documento de componentes de copia de seguridad. Un ejemplo de este tipo de actualización sería cambiar el destino de restauración.

 

Puede encontrar información sobre cada escritor primario del componente seleccionable almacenado mediante [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Con esta información, se pueden consultar los documentos de metadatos del escritor y identificar el documento coincidente. A continuación, mediante la [*ruta de acceso lógica*](vssgloss-l.md), el solicitante puede identificar los componentes no seleccionables dependientes para cada componente seleccionable, es decir, identificar todos los miembros del [*conjunto de componentes*](vssgloss-c.md)del componente seleccionable.

Con la interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , el solicitante tiene ahora información completa del componente, incluida la especificación de la ruta de acceso (desde la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) ), para componentes seleccionables y no seleccionables que necesita para realizar copias de seguridad o restaurar.

Esta es una de las razones por las que es fundamental que un solicitante guarde el estado de su propio documento de componentes de copia de seguridad y los documentos de metadatos del escritor de los escritores de los que está realizando una copia de seguridad.

Vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md) para obtener información más detallada.

 

 
