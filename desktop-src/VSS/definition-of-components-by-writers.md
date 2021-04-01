---
description: Los componentes los definen y crean instancias de los escritores en su documento de metadatos del escritor como respuesta a un evento de identificación al inicio de una operación de copia de seguridad (Consulte información general sobre la inicialización de la copia de seguridad) cuando se rellena el documento de metadatos del escritor.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definición de componentes por escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913381"
---
# <a name="definition-of-components-by-writers"></a>Definición de componentes por escritores

Los componentes los definen y crean instancias de los escritores en su documento de metadatos del escritor como respuesta a un [*evento de identificación*](vssgloss-i.md) al inicio de una operación de copia de seguridad (consulte [información general sobre la inicialización de la copia de seguridad](overview-of-backup-initialization.md)) cuando se rellena el documento de metadatos del escritor.

Al crear un componente en su documento de metadatos de escritura, con [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) y [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), un escritor debe especificar:

-   Si el componente es [ *seleccionable para copia de seguridad*](vssgloss-s.md)
-   Un tipo de componente
-   Un nombre de componente (que debe ser único no solo dentro de una [*instancia de escritor*](vssgloss-w.md) determinada, sino en todas las instancias de escritor)
-   Si el componente tiene metadatos específicos del escritor asociados a él
-   Si el escritor requiere una notificación después de una copia de seguridad correcta

Los escritores pueden especificar opcionalmente:

-   La ruta de [*acceso lógica*](vssgloss-l.md) de un componente (que debe ser única no solo dentro de una instancia de escritor determinada, sino en todas las instancias del escritor)
-   Una descripción de componente (o título)
-   Un icono que se usará con las GUI para indicar el componente

No es necesario que un componente contenga realmente ningún archivo. Este tipo de componente vacío o "ficticio" puede ser útil para organizar los componentes. Este componente se puede usar para definir un [*conjunto de componentes*](vssgloss-c.md) y un componente del escritor (consulte el apartado [de la acción lógica de los componentes](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configuración de la organización de componentes

La configuración de la [*selección*](vssgloss-s.md) de un componente (su [*selección para la copia de seguridad*](vssgloss-s.md)y su [*selección de restauración*](/windows)) y sus rutas de acceso [*lógicas*](vssgloss-l.md) permiten que un escritor exija o haga opcional la inclusión de determinados componentes en una operación de copia de seguridad o restauración, y para agrupar componentes en [*conjuntos de componentes*](vssgloss-c.md) con un componente seleccionable que actúe como punto de entrada para todo el grupo.

La pertenencia a estas agrupaciones determina qué componentes se utilizarán durante las operaciones de copia de seguridad y restauración. Al usar "Selectable" para hacer que la operación de copia de seguridad sea seleccionable para la operación de copia de seguridad y Selectable para la restauración de la operación de restauración, los desarrolladores deben comprender lo siguiente:

-   Si se realiza una copia de seguridad de los componentes administrados por un escritor determinado, un solicitante debe [*incluir explícitamente*](vssgloss-e.md) todos los [*componentes*](vssgloss-c.md) no seleccionables sin antecesores seleccionables en su [*ruta de acceso lógica*](vssgloss-l.md) al documento componentes de copia de seguridad, así como realizar una copia de seguridad y restaurar esos componentes como un grupo.
-   Un solicitante tiene la opción de agregar explícitamente componentes seleccionables al documento componentes de copia de seguridad durante las operaciones de copia de seguridad y restauración. una vez agregado, se debe realizar una copia de seguridad o una restauración del componente.
-   Si un componente es seleccionable, el componente y todos sus [*subcomponentes*](vssgloss-s.md) (como se define en rutas de acceso lógicas) forman un conjunto de componentes, que se puede tratar como una unidad única que puede participar opcionalmente en operaciones de copia de seguridad y restauración.
-   Un solicitante no agrega nunca explícitamente un componente no seleccionable con antecesores seleccionables, un subcomponente en un conjunto de componentes, a su documento componentes de copia de seguridad durante las operaciones de copia de seguridad y restauración. Estos componentes se deben [*incluir implícitamente*](/windows) si su antecesor seleccionable se agrega explícitamente, en cuyo caso se deben realizar copias de seguridad o restaurar (consulte [uso de componentes por parte del solicitante](use-of-components-by-the-requestor.md)).
-   Un componente seleccionable con un antecesor seleccionable sigue siendo un [*subcomponente*](vssgloss-s.md) (un miembro de un conjunto de componentes) y puede incluirse implícitamente si su antecesor seleccionable se incluye explícitamente en la operación. En este caso, su información no se agrega al documento componentes de copia de seguridad. Si su antecesor seleccionable no se incluye en la operación, el componente se puede seleccionar explícitamente para su inclusión en la operación, en cuyo caso su información se incluye en el documento componentes de copia de seguridad.
-   Un subcomponente incluido implícitamente en una copia de seguridad se puede incluir explícitamente en una operación de restauración, independientemente del estado de cualquier antecesor seleccionable, si es seleccionable para la restauración. Cualquier subcomponente seleccionable para restauración incluido durante una operación de restauración debe agregar su información al documento componentes de copia de seguridad.
-   Un escritor que no ha agregado explícitamente ningún componente al documento de componentes de copia de seguridad antes de la generación de eventos de [*PrepareForBackup*](vssgloss-p.md) y [*prerestore*](vssgloss-p.md) no recibirá más eventos de VSS.

Para obtener más información, vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md).

## <a name="adding-files-to-a-component"></a>Agregar archivos a un componente

Un componente contiene información de archivo en forma de un [*conjunto de archivos*](vssgloss-f.md) que contiene:

-   Directorio raíz de los archivos del componente.
-   Especificación de archivo para los archivos del componente.
-   Marca que indica si la especificación del componente es recursiva.

Dependiendo del tipo de componente, que puede ser una base de datos o un grupo de archivos, y (en el caso de los componentes de base de datos) si los archivos que se van a cargar son archivos de datos o de registro, un escritor llama a [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para agregar un conjunto de archivos.

Al usar estas funciones, debe especificar los archivos que se van a agregar al conjunto de archivos como se indica a continuación:

-   *wszPath*: esta es la ruta de acceso al directorio que contiene los archivos que se van a agregar al conjunto de archivos. Si el parámetro *bRecursive* se establece en **true**, el parámetro *wszPath* especifica una jerarquía de directorios que se va a recorrer de forma recursiva y se deben volver a crear todos los directorios, incluidos los directorios vacíos.
-   *wszFilespec*: esta cadena especifica los archivos de cada directorio que se van a agregar al conjunto de archivos.

Por ejemplo, supongamos que existe la siguiente estructura de directorios:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
C: \\ Directory1 \\ Directory3\\  
</dl>

Si el escritor especifica "C: \\ Directory1" para *wszPath*, "archivo1. \* " para *wszFilespec* y **true** para *bRecursive*, el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Si en su lugar el escritor especifica "C: \\ Directory1" para *wszPath*, \* "" para *wszFilespec* y **true** para *bRecursive*, el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Si el escritor especifica "C: \\ Directory1" para *wszPath*, " \* " para *wszFilespec* y **false** para *bRecursive*, el solicitante debe incluir estos archivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

En todos los ejemplos anteriores, siempre que el escritor especifique **true** para *bRecursive*, \\ \\ se debe volver a crear el directorio vacío C: Directory1 Directory3 \\ .

Para un conjunto de archivos agregado a un componente de grupo de archivos, en los casos en los que los archivos que se encuentran actualmente en el disco no están en lo que el escritor consideraría la ubicación adecuada o predeterminada, un escritor tiene la opción de agregar una ruta de acceso alternativa. En estos casos, la definición del conjunto de archivos de la ruta de acceso contiene la ubicación normal de los archivos y el lugar donde se deben restaurar los archivos, mientras que la ruta de acceso alternativa contiene la ubicación actual de los archivos de los que se va a hacer una copia de seguridad.

Todos los archivos del conjunto de archivos deben existir en el momento de la copia de seguridad. Los solicitantes deben suponer que todos los archivos enumerados en el conjunto de archivos son necesarios para la copia de seguridad y que no se realizará la copia de seguridad si faltan archivos. Tenga en cuenta que cuando \* se especifica "" para el parámetro *wszFilespec* , puede coincidir con cero o más archivos.

Tenga en cuenta que estos atributos de documento de metadatos de escritor como asignaciones de ubicación alternativas, archivos incluidos y excluidos explícitamente y métodos de restauración se establecen en el nivel del escritor, no en el nivel de componente. (Para obtener más información, vea [trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md)).

## <a name="component-definition-for-backup-and-restore-operations"></a>Definición de componentes para operaciones de copia de seguridad y restauración

Las operaciones de restauración y de copia de seguridad generan necesariamente un [*evento de identificación*](vssgloss-i.md)y, para las copias de seguridad y las restauraciones, se controlarán mediante el mismo método [**CVssWriter::**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Durante las operaciones de copia de seguridad, los solicitantes utilizan la información devuelta por los métodos [**CVssWriter::**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de un escritor para determinar qué escritores están presentes en el sistema y, a continuación, determinar de qué archivos se debe hacer una copia de seguridad.

Durante las operaciones de restauración, la información devuelta por el evento [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de un escritor se utiliza únicamente para establecer la identidad y el estado de los escritores actualmente presentes en el sistema. no se utiliza la información de especificación de archivo generada durante una restauración. En su lugar, los documentos de metadatos de escritor almacenados en el momento de la copia de seguridad se usan para obtener estos datos.

Una vez que se genera durante una operación de copia de seguridad, se guarda la información del componente de escritor, junto con el resto de la información del escritor, para que se recupere para admitir las operaciones de restauración. Normalmente, es responsabilidad del solicitante almacenar esta información.

 

 
