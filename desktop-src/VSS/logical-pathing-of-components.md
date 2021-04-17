---
description: La acción lógica se usa para organizar los componentes administrados por un escritor en grupos bien definidos.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Acciones lógicas de los componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a591f3eec0e00257740dbbd24ab7c609c53c27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696998"
---
# <a name="logical-pathing-of-components"></a>Acciones lógicas de los componentes

La [*acción lógica*](vssgloss-l.md) se usa para organizar los componentes administrados por un escritor en grupos bien definidos.

La ruta de acceso lógica es análoga en la estructura a la pausa tradicional del archivo, para lo que usa la barra diagonal inversa " \\ " para separar los elementos de la ruta de acceso. A diferencia de las rutas de acceso de archivo, la raíz de una ruta de acceso lógica es **null**, en lugar de " \\ ".

La ruta de acceso lógica se expresa como una cadena terminada en **null** y no hay otras restricciones en los caracteres que puede contener la ruta de acceso.

El uso más importante de las acciones lógicas es definir [*conjuntos de componentes*](vssgloss-c.md), donde la [*inclusión de componentes explícitos*](vssgloss-e.md) en una operación de copia de seguridad o restauración de un componente seleccionable requiere la inclusión de varios componentes ([*subcomponente*](vssgloss-s.md)). La ruta de acceso lógica del componente de definición de un conjunto de componentes es un elemento primario de las rutas de acceso lógicas de sus subcomponentes y:

-   Los subcomponentes deben compartir como ruta de acceso raíz la ruta de acceso lógica del componente seleccionable que define el conjunto de componentes.
-   Una ruta de acceso raíz de **null** es válida.
-   El nombre del componente seleccionable que se va a definir debe ser el primer elemento de ruta de acceso lógica después de la ruta de acceso raíz para cada subcomponente no seleccionable del conjunto de componentes.
-   Los conjuntos de componentes se pueden anidar.
-   La combinación de ruta de acceso lógica y nombre de componente debe ser única en todas las instancias de una [*clase de escritor*](vssgloss-w.md).

En el ejemplo hipotético de un escritor *Alwriter* con una estructura de ruta de acceso lógica definida a continuación se ilustran las acciones lógicas.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad |
|----------------|-------------------------|-----------------------|
| Aplicaciones  | ""                      | N                     |
| "ConfigFiles"  | Aplicaciones           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| UserInfo     | "Security"              | N                     |
| Firma | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| Set1         | "writerData"            | N                     |
| Bernardo          | "writerData \\ Set1"      | N                     |
| Dec          | "writerData \\ Set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Bernardo          | "writerData \\ Set2"      | N                     |
| Dec          | "writerData \\ Set2"      | N                     |
| Misma        | "writerData \\ QueryLogs" | N                     |
| Uso        | "writerData"            | Y                     |
| Bernardo          | "uso de writerData \\ "     | N                     |
| Dec          | "uso de writerData \\ "     | N                     |



 

Tenga en cuenta que los componentes "ejecutables" y "ConfigFile" tienen una relación de elementos primarios y secundarios, pero ambos son no seleccionables. Por lo tanto, no forman un conjunto de componentes. Cada vez que se realiza una copia de seguridad o se restaura *el escritor,* estos dos componentes tendrán que [*incluirse explícitamente*](vssgloss-e.md) en la operación.

El componente "LicenseInfo" es seleccionable sin antecesor ni descendiente. Se puede incluir explícitamente, o no, en una operación de copia de seguridad o restauración a discreción del solicitante.

El componente "seguridad" define un conjunto de componentes sencillo que no contiene ningún conjunto de componentes.

El componente "writerData" define un conjunto de componentes que contiene una colección compleja de componentes con varias jerarquías de rutas de acceso lógicas bien definidas.

Un subcomponente, "Usage", es seleccionable y define un conjunto de componentes.

Varios componentes tienen el mismo nombre y se distinguen por sus rutas de acceso lógicas. Las instancias de los componentes no seleccionables "Dec" y "Jan" existen en los componentes componentes no seleccionables "Set1" y "Set2" y en el subcomponente "Usage" seleccionable.

Si el componente "writerData" se incluye explícitamente en una copia de seguridad o restauración, todos sus subcomponentes, incluso los del conjunto anidado definido por "Usage", se [*incluirán*](vssgloss-e.md)[*implícitamente en la*](vssgloss-i.md) operación.

Si el conjunto de componentes definido por "writerData" no se incluye explícitamente en una copia de seguridad o restauración, los componentes "Set1", "Set2" y "QueryLogs" (y sus instancias de subcomponentes "Dec" y "Jan") no se incluirán implícitamente en la operación de copia de seguridad o restauración.

Sin embargo, incluso si "writerData" no está incluido en la operación, el componente "uso" sigue siendo seleccionable y todavía se puede incluir explícitamente en una operación de copia de seguridad o restauración. Si es así, sus subcomponentes "Jan" y "Dec" se incluirán implícitamente.

Otros puntos merecen la Nota:

-   Los componentes seleccionables "LicenseInfo" y "writerData" y los "ejecutables" del componente no seleccionable están todos en el mismo nivel en la jerarquía de rutas de acceso lógica de la carpeta de *escritura*: todos tienen la misma ruta de acceso lógica de **null** o "", la ruta de acceso lógica raíz.
-   El componente seleccionable "uso" nunca debe incluirse explícitamente en una copia de seguridad, si su elemento primario seleccionable ("writerData") se incluye explícitamente en una operación de copia de seguridad o restauración.
-   Los componentes que definen conjuntos de componentes pueden existir simplemente por motivos organizativos. Por ejemplo, el componente "writerData" o "Usage", o ambos, pueden estar vacíos; es decir, no se agregó ningún [*conjunto de archivos*](vssgloss-f.md) a ellos mediante el método [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Los componentes de siguen definiendo un conjunto de componentes.

 

 



