---
description: El concepto de componente es fundamental para organizar los archivos de los que se va a realizar una copia de seguridad o restauración del escritor.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componentes de metadatos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac121ae62798d0318233dba48e6d0b56c36e2065a71fe8e12af9c963893dd027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751441"
---
# <a name="vss-metadata-components"></a>Componentes de metadatos de VSS

El concepto de componente es fundamental para organizar los archivos de los que se va a realizar una copia de seguridad o restauración del sistema de [*escritura.*](vssgloss-c.md)

Los componentes permiten a un escritor indicar a un motor de copia de seguridad cómo se van a organizar sus archivos, las dependencias entre archivos y qué tipo de datos pueden contener esos archivos. Esto permite que un motor de copia de seguridad decida cómo almacenar archivos para lograr la máxima eficacia.

Además, las aplicaciones basadas en VSS usan componentes como bloques de creación para sus metadatos y el medio para la comunicación entre escritor y solicitante.

Los escritores y solicitantes almacenan información sobre los componentes por separado (en el documento de metadatos del escritor y en el documento de componentes de copia de seguridad, respectivamente), y la información difiere en cada representación.

La información de componentes de los documentos de metadatos del escritor incluye lo siguiente:

-   Información de un solo escritor en cada documento
-   Todos los componentes de ese escritor, [](vssgloss-e.md) tanto si se pueden incluir explícitamente como si deben incluirse implícitamente [*en*](vssgloss-i.md) una operación de copia de seguridad o restauración
-   [*Información de ruta de*](vssgloss-l.md) acceso lógica utilizada para asociar un componente seleccionable para copia de seguridad con un determinado no seleccionable para los componentes de copia de seguridad, formando así un conjunto de componentes
-   La [*información del conjunto*](vssgloss-f.md) de archivos (ruta de acceso, especificación de archivo y marca de recursividad) administrada para cada componente

Los documentos de metadatos de escritor también contienen información de metadatos de nivel de escritor, como métodos de restauración y asignaciones de ubicación alternativas para la restauración. Los documentos de metadatos del escritor son de solo lectura. La interfaz para examinar esta información es [**IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

La información de componentes de los documentos de componentes de copia de seguridad incluye lo siguiente:

-   Solo información sobre componentes incluidos explícitamente
-   Información de metadatos de nivel de escritor, como asignaciones de ubicación alternativas y restauración
-   Información de estado que describe una operación de copia de seguridad o restauración

Los documentos de componentes de copia de seguridad no contienen información sobre los conjuntos de [*archivos de los componentes.*](vssgloss-f.md) Los documentos de componente de copia de seguridad no son de solo lectura y el escritor puede modificarlo. La interfaz para acceder a esta información es [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

El ciclo de vida y la relación entre las dos expresiones de un componente se pueden entender de la siguiente manera:

-   Los escritores son responsables de las definiciones iniciales de los componentes.
-   Un solicitante examina los metadatos de todos los escritores y sus componentes.
-   A partir de la información de selección y ruta de acceso lógica de los componentes, un solicitante determina qué componentes deben incluirse explícitamente, que se pueden incluir explícitamente, que definen conjuntos de componentes y que son miembros de conjuntos de componentes.
-   Un solicitante agrega esos componentes que requieren inclusión explícita e incluye implícitamente subcomponentes en conjuntos de componentes [*(cuya*](/windows) información no está en el documento Componentes de copia de seguridad).
-   Al controlar eventos, los escritores y solicitantes pueden modificar y examinar la información de componentes almacenada en el documento Componentes de copia de seguridad para coordinar su actividad.

Tanto el escritor como la información del componente de versiones del solicitante son necesarios para ejecutar correctamente las operaciones de copia de seguridad y restauración, y ambos deben almacenarse con cualquier dato de copia de seguridad:

-   [Tipos de componentes](component-types.md)
-   [Definición de componentes por escritores](definition-of-components-by-writers.md)
-   [Uso de componentes por parte del solicitante](use-of-components-by-the-requestor.md)

 

 
