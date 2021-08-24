---
description: La ruta de acceso lógica se usa para organizar los componentes administrados por un escritor en grupos bien definidos.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Ruta de acceso lógica de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ce4feeeb2147a7be736547eb69cbbb1a254c5940b18e904bc3be3290a2c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767755"
---
# <a name="logical-pathing-of-components"></a>Ruta de acceso lógica de componentes

[*La ruta de acceso*](vssgloss-l.md) lógica se usa para organizar los componentes administrados por un escritor en grupos bien definidos.

La ruta de acceso lógica es análoga en estructura a la ruta de acceso de archivo tradicional, usando la barra diagonal inversa " " " para separar \\ los elementos de la ruta de acceso. A diferencia de las rutas de acceso de archivo, la raíz de una ruta de acceso lógica **es NULL,** en lugar de \\ "".

La ruta de acceso lógica se expresa como una cadena terminada en **NULL** y no hay ninguna otra restricción en los caracteres que la ruta de acceso puede contener.

El uso más importante de la ruta de [](vssgloss-e.md) acceso lógica es definir conjuntos de componentes [*,*](vssgloss-c.md)donde la inclusión explícita de componentes en una operación de copia de seguridad o restauración de un componente seleccionable requiere la inclusión de otros componentes [*(subcomponente*](vssgloss-s.md)). La ruta de acceso lógica del componente de definición de un conjunto de componentes es un elemento primario de las rutas de acceso lógicas de sus subcomponentes y:

-   Los subcomponentes deben compartir como ruta de acceso raíz la ruta de acceso lógica del componente seleccionable que define el conjunto de componentes.
-   Una ruta de acceso raíz **de NULL** es válida.
-   El nombre del componente seleccionable que se define debe ser el primer elemento de ruta de acceso lógico después de la ruta de acceso raíz para cada subcomponente no seleccionable del conjunto de componentes.
-   Los conjuntos de componentes se pueden anidar.
-   La combinación de la ruta de acceso lógica y el nombre del componente debe ser única en todas las instancias de una [*clase de escritor.*](vssgloss-w.md)

El ejemplo hipotético de un *escritor MyWriter con* una estructura de ruta de acceso lógica definida a continuación ilustra la ruta de acceso lógica.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad |
|----------------|-------------------------|-----------------------|
| "Ejecutables"  | ""                      | N                     |
| "ConfigFiles"  | "Ejecutables"           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| "UserInfo"     | "Security"              | N                     |
| "Certificados" | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Query"        | "writerData \\ QueryLogs" | N                     |
| "Uso"        | "writerData"            | Y                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Tenga en cuenta que los componentes "Ejecutables" y "ConfigFile" tienen una relación de elementos primarios y secundarios, pero ambos no se pueden seleccionar. Por lo tanto, no forman un conjunto de componentes. Cada vez que se haga una copia de seguridad o se restaure el escritor *MyWriter,* estos dos componentes tendrán que incluirse [*explícitamente*](vssgloss-e.md) en la operación.

El componente "LicenseInfo" se puede seleccionar sin antecesor ni descendiente. Se puede incluir explícitamente, o no, en una operación de copia de seguridad o restauración a discreción del solicitante.

El componente "Security" define un conjunto de componentes simple, que no contiene ningún conjunto de componentes debajo.

El componente "writerData" define un conjunto de componentes, que contiene una colección compleja de componentes con varias jerarquías de rutas de acceso lógicas bien definidas debajo.

Un subcomponente, "Usage", se puede seleccionar y define un conjunto de componentes.

Varios componentes tienen el mismo nombre y se distinguen por sus rutas de acceso lógicas. Las instancias de los componentes no seleccionables "Dec" y "Jan" existen en los componentes no seleccionables "Set1" y "Set2" y en el subcomponente seleccionable "Usage".

Si el componente "writerData" se incluye explícitamente en una copia de seguridad o restauración, todos sus subcomponentes, incluso los del conjunto de componentes anidados definido por "Usage", se incluirán implícitamente en la operación. [](vssgloss-e.md)[](vssgloss-i.md)

Si el conjunto de componentes definido por "writerData" no se incluye explícitamente en una copia de seguridad o restauración, los componentes "Set1", "Set2" y "QueryLogs" (y sus instancias de subcomponentes "Dec" y "Jan") no se incluirán implícitamente en la operación de copia de seguridad o restauración.

Sin embargo, incluso si "writerData" no está incluido en la operación, el componente "Usage" todavía se puede seleccionar y todavía se puede incluir explícitamente en una operación de copia de seguridad o restauración. Si es así, sus subcomponentes "Jan" y "Dec" se incluirán implícitamente.

Otros puntos que merecen la pena tener en cuenta:

-   Los componentes seleccionables "LicenseInfo" y "writerData" y el componente no seleccionable "Executables" están todos en el mismo nivel en la jerarquía de rutas de acceso lógicas de *MyWriter:* todos tienen la misma ruta de acceso lógica de **NULL** o "", la ruta de acceso lógica raíz.
-   El componente seleccionable "Usage" nunca debe incluirse explícitamente en una copia de seguridad, si su elemento primario seleccionable ("writerData") se incluye explícitamente en una operación de copia de seguridad o restauración.
-   Los componentes que definen conjuntos de componentes pueden existir simplemente por motivos organizativos. Por ejemplo, el componente "writerData" o "Usage", o ambos, podrían estar vacíos; Es decir, [*no*](vssgloss-f.md) se les agregó ningún conjunto de archivos mediante el método [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) o [**IVssCreateWriterMetadata::AddDatabaseLogFiles.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) Los componentes siguen definindo un conjunto de componentes.

 

 



