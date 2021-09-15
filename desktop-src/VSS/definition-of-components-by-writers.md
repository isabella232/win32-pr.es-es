---
description: Los escritores definen y crea instancias de los componentes en su documento de metadatos del escritor en respuesta a un evento Identify al principio de una operación de copia de seguridad (consulte Información general de inicialización de copia de seguridad) cuando se rellena el documento de metadatos del escritor.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definición de componentes por escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473387"
---
# <a name="definition-of-components-by-writers"></a>Definición de componentes por escritores

Los escritores definen y crea instancias de los componentes en su documento de metadatos del escritor en respuesta a un evento [*Identify*](vssgloss-i.md) al principio de una operación de copia de seguridad (vea [Información](overview-of-backup-initialization.md)general de inicialización de copia de seguridad) cuando se rellena el documento de metadatos del escritor.

Al crear un componente en su documento de metadatos del escritor, con [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssCreateWriterMetadata::AddComponent,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)un escritor debe especificar:

-   Si el componente se puede [ *seleccionar para la copia de seguridad*](vssgloss-s.md)
-   Un tipo de componente
-   Un nombre de componente (que debe ser único no solo dentro de una instancia de [*escritor determinada,*](vssgloss-w.md) sino en todas las instancias de escritor)
-   Si el componente tiene metadatos específicos del escritor asociados
-   Si el escritor requiere una notificación después de una copia de seguridad correcta

Los escritores pueden especificar opcionalmente:

-   Ruta de acceso lógica de [*un*](vssgloss-l.md) componente (que debe ser única no solo dentro de una instancia de escritor determinada, sino en todas las instancias de escritor)
-   Descripción de un componente (o título)
-   Icono que se va a usar con las GUI para indicar el componente

No es necesario que un componente contenga realmente ningún archivo. Este tipo de componente vacío o "ficticio" puede ser útil para organizar los componentes. Este componente se puede usar para definir un conjunto [*de*](vssgloss-c.md) componentes y un componente de escritor (vea Ruta de [acceso lógica de componentes](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configuración de la organización de componentes

El establecimiento de la capacidad [](vssgloss-s.md)de selección de un componente [*(su*](vssgloss-s.md) [](vssgloss-l.md) capacidad de selección para la copia de seguridad y su capacidad de selección para [](vssgloss-c.md) la restauración) [](/windows)y sus rutas de acceso lógicas permite a un escritor hacer obligatorio o opcional la inclusión de determinados componentes en una operación de copia de seguridad o restauración, y agrupar componentes en conjuntos de componentes con un componente seleccionable que actúa como punto de entrada para todo el grupo.

La pertenencia a estas agrupaciones determina qué componentes se usarán durante las operaciones de copia de seguridad y restauración. El uso de "seleccionable" para significar que se puede seleccionar de nuevo para la operación de copia de seguridad y que se puede seleccionar para la restauración para la operación de restauración, los desarrolladores deben comprender lo siguiente:

-   Si se hace una copia de seguridad de los componentes administrados por [](vssgloss-c.md) un escritor determinado, un [](vssgloss-l.md) solicitante debe incluir explícitamente todos los componentes no seleccionables sin antecesores seleccionables en su ruta de acceso lógica al documento componentes de copia de seguridad y realizar copias de seguridad y restaurar esos componentes como un grupo. [](vssgloss-e.md)
-   Un solicitante tiene la opción de agregar explícitamente componentes seleccionables al documento componentes de copia de seguridad durante las operaciones de copia de seguridad y restauración. Una vez agregado, se debe realizar una copia de seguridad del componente o restaurarlo.
-   Si se puede seleccionar un componente, el componente y todos sus [*subcomponentes (definidos*](vssgloss-s.md) por rutas de acceso lógicas) forman un conjunto de componentes, que se puede tratar como una sola unidad que, opcionalmente, puede participar en operaciones de copia de seguridad y restauración.
-   Un solicitante nunca agrega explícitamente un componente no seleccionable con antecesores seleccionables, un subcomponente de un conjunto de componentes, a su documento de componentes de copia de seguridad durante las operaciones de copia de seguridad y restauración. Estos componentes [](/windows) deben incluirse implícitamente si su antecesor seleccionable se agrega explícitamente, en cuyo caso se deben realizar una copia de seguridad o restaurarse (vea Uso de componentes por parte del [solicitante).](use-of-components-by-the-requestor.md)
-   Un componente seleccionable con un antecesor seleccionable sigue siendo un [*subcomponente*](vssgloss-s.md) (un miembro de un conjunto de componentes) y se puede incluir implícitamente si su antecesor seleccionable se incluye explícitamente en la operación. En este caso, su información no se agrega al documento componentes de copia de seguridad. Si su antecesor seleccionable no se incluye en la operación, el componente se puede seleccionar explícitamente para su inclusión en la operación, en cuyo caso su información se incluye en el documento componentes de copia de seguridad.
-   Un subcomponente incluido implícitamente en una copia de seguridad se puede incluir explícitamente en una operación de restauración, independientemente del estado de cualquier antecesor seleccionable, si se puede seleccionar para la restauración. Cualquier subcomponente seleccionable para la restauración incluido durante una operación de restauración debe tener su información agregada al documento componentes de copia de seguridad.
-   Un sistema de escritura que no tenga ningún componente agregado explícitamente al documento componentes de copia de seguridad antes de la generación de eventos [*PrepareForBackup*](vssgloss-p.md) y [*PreRestore*](vssgloss-p.md) no recibirá más eventos de VSS.

Para obtener más información, vea [Trabajar con la capacidad de selección y las rutas de acceso lógicas.](working-with-selectability-and-logical-paths.md)

## <a name="adding-files-to-a-component"></a>Agregar archivos a un componente

Un componente contiene información de archivo en forma de un [*conjunto de archivos*](vssgloss-f.md) que contiene:

-   Directorio raíz de los archivos del componente.
-   Especificación de archivo para los archivos del componente.
-   Marca que indica si la especificación del componente es recursiva.

Dependiendo del tipo de componente, que puede ser una base de datos o un grupo de archivos, y (en el caso de los componentes de base de datos) si los archivos que se van a cargar son archivos de datos o de registro, un escritor llama a [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para agregar un conjunto de archivos.

Al usar estas funciones, debe especificar los archivos que se van a agregar al conjunto de archivos como se muestra a continuación:

-   *wszPath:* esta es la ruta de acceso al directorio que contiene los archivos que se van a agregar al conjunto de archivos. Si el *parámetro bRecursive* se establece en **true,** el parámetro *wszPath* especifica una jerarquía de directorios que se recorrerán de forma recursiva y se deben volver a crear todos los directorios, incluidos los directorios vacíos.
-   *wszFilespec:* esta cadena especifica los archivos de cada directorio que se van a agregar al conjunto de archivos.

Por ejemplo, supongamos que existe la siguiente estructura de directorios:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
C: \\ Directory1 \\ Directory3\\  
</dl>

Si el escritor especifica "C: \\ Directory1" para *wszPath*, "File1. \* " para *wszFilespec* y **true** para *bRecursive,* el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Si el escritor especifica en su lugar "C: \\ Directory1" para *wszPath*, " \* " para *wszFilespec* y **true** para *bRecursive*, el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Si el escritor especifica "C: \\ Directory1" para *wszPath*, " \* " para *wszFilespec* y **false** para *bRecursive,* el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

En todos los ejemplos anteriores, siempre que el escritor especifique **true** para *bRecursive,* se debe volver a crear el directorio vacío C: \\ Directory1 \\ \\ Directory3.

Para un conjunto de archivos agregado a un componente de grupo de archivos, en los casos en los que los archivos que se encuentran actualmente en disco no están en lo que el escritor consideraría la ubicación adecuada o predeterminada, un escritor tiene la opción de agregar una ruta de acceso alternativa. En estos casos, la definición del conjunto de archivos de la ruta de acceso contiene la ubicación normal de los archivos y en la que se deben restaurar los archivos, mientras que la ruta de acceso alternativa contiene la ubicación actual de los archivos de los que se va a realizar una copia de seguridad.

Todos los archivos del conjunto de archivos deben existir en el momento de la copia de seguridad. Los solicitantes deben asumir que todos los archivos enumerados en el conjunto de archivos son necesarios para la copia de seguridad y producirán un error en la copia de seguridad si faltan archivos. Tenga en cuenta que cuando \* se especifica " " para el parámetro *wszFilespec,* puede coincidir con cero o más archivos.

Tenga en cuenta que estos atributos del documento de metadatos del escritor como asignaciones de ubicación alternativas, archivos incluidos y excluidos explícitamente, y los métodos de restauración se establecen en el nivel de escritor, no en el nivel de componente. (Para obtener más información, vea [Trabajar con el documento de metadatos del escritor).](working-with-the-writer-metadata-document.md)

## <a name="component-definition-for-backup-and-restore-operations"></a>Definición de componentes para operaciones de copia de seguridad y restauración

Las operaciones de restauración y copia de seguridad generan necesariamente un evento [*Identify*](vssgloss-i.md)y, para las copias de seguridad y restauraciones, se controlará mediante el mismo [**método CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

Durante las operaciones de copia de seguridad, los solicitantes usan la información devuelta por los [**métodos CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de un escritor para determinar qué escritores están presentes en el sistema y, a continuación, para determinar cuáles de los archivos de los que se va a realizar una copia de seguridad.

Durante las operaciones de restauración, la información devuelta por el evento [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de un escritor solo se usa para establecer la identidad y el estado de los escritores presentes actualmente en el sistema. no se usa la información de especificación de archivo generada durante una restauración. En su lugar, los documentos de metadatos del escritor almacenados en tiempo de copia de seguridad se usan para obtener estos datos.

Una vez generado durante una operación de copia de seguridad, la información del componente de escritura, junto con el resto de la información del sistema de escritura, se guarda para recuperarse para admitir las operaciones de restauración. Normalmente es responsabilidad del solicitante almacenar esta información.

 

 
