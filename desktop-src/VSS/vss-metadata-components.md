---
description: Crítico para organizar los archivos de los que se va a realizar la copia de seguridad o la restauración del escritor es el concepto de componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componentes de metadatos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696466"
---
# <a name="vss-metadata-components"></a>Componentes de metadatos de VSS

Crítico para organizar los archivos de los que se va a realizar la copia de seguridad o la restauración del escritor es el concepto de [*componente*](vssgloss-c.md).

Los componentes permiten a un sistema de escritura indicar a un motor de copia de seguridad cómo se van a organizar sus archivos, las dependencias entre archivos y el tipo de datos que estos archivos pueden contener. Esto permite a un motor de copia de seguridad decidir cómo almacenar archivos para obtener la máxima eficacia.

Además, las aplicaciones basadas en VSS usan componentes como los bloques de creación de sus metadatos y el medio para la comunicación entre el autor y el solicitante.

Los escritores y los solicitantes almacenan información sobre los componentes por separado, en el documento de metadatos de escritor y en el documento de componentes de copia de seguridad, respectivamente, y la información difiere en cada representación.

La información de los componentes de los documentos de metadatos del escritor incluye lo siguiente:

-   Información de un solo escritor en cada documento
-   Todos los componentes de ese escritor, tanto si se pueden [*incluir explícitamente*](vssgloss-e.md) como si se deben [*incluir implícitamente*](vssgloss-i.md) en una operación de copia de seguridad o restauración.
-   Información de [*ruta de acceso lógica*](vssgloss-l.md) que se usa para asociar un componente seleccionable para copia de seguridad con determinados elementos no seleccionables para los componentes de copia de seguridad, formando así un conjunto de componentes.
-   La información del [*conjunto de archivos*](vssgloss-f.md) (ruta de acceso, especificación de archivo y marca de recursividad) administrada para cada componente

Los documentos de metadatos del escritor también contienen información de metadatos de nivel de escritor, como métodos de restauración y asignaciones de ubicación alternativas para la restauración. Los documentos de metadatos del escritor son de solo lectura. La interfaz para examinar esta información es [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

La información del componente en los documentos de componentes de copia de seguridad incluye lo siguiente:

-   Solo información sobre componentes incluidos explícitamente
-   Información de metadatos de nivel de escritor, como asignaciones de ubicación alternativas y restauración
-   Información de estado que describe una operación de copia de seguridad o restauración

Los documentos de componentes de copia de seguridad no contienen información sobre los [*conjuntos de archivos*](vssgloss-f.md)de los componentes. Los documentos de componentes de copia de seguridad no son de solo lectura y pueden ser modificados por el escritor. La interfaz para tener acceso a esta información es [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

El ciclo de vida y la relación entre las dos expresiones de un componente se pueden entender de la siguiente manera:

-   Los escritores son responsables de las definiciones iniciales de los componentes.
-   Un solicitante examina los metadatos de todos los escritores y sus componentes.
-   A partir de la información de selección y ruta de acceso lógica de los componentes, un solicitante determina qué componentes deben incluirse explícitamente, que se pueden incluir explícitamente, que definen conjuntos de componentes y que son miembros de conjuntos de componentes.
-   Un solicitante agrega los componentes que requieren una inclusión explícita e incluye implícitamente subcomponentes en [*conjuntos de componentes*](/windows) (cuya información no se encuentra en el documento componentes de copia de seguridad).
-   Al controlar los eventos, los escritores y los solicitantes pueden modificar y examinar la información de componente almacenada en el documento componentes de copia de seguridad para coordinar su actividad.

Tanto el escritor como la información del componente de versiones del solicitante son necesarios para ejecutar correctamente las operaciones de copia de seguridad y restauración, y ambos deben almacenarse con los datos de copia de seguridad:

-   [Tipos de componentes](component-types.md)
-   [Definición de componentes por escritores](definition-of-components-by-writers.md)
-   [Uso de componentes por parte del solicitante](use-of-components-by-the-requestor.md)

 

 
