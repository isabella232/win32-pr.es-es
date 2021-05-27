---
title: Acerca de las tablas Atom
description: En esta sección se deba a las tablas atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- átomos
- tablas atom
- nombres atom
- Intercambio dinámico de datos (DDE),atoms
- DDE (Intercambio dinámico de datos),atoms
- tablas atom globales
- tablas atom locales
- enteros atoms
- atoms de cadena
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 92a8304e1e96c7385ddb11ba6391258acbe62a26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549610"
---
# <a name="about-atom-tables"></a>Acerca de las tablas Atom

Una *tabla atom* es una tabla definida por el sistema que almacena cadenas e identificadores correspondientes. Una aplicación coloca una cadena en una tabla atom y recibe un entero de 16 bits, denominado *atom*, que se puede usar para acceder a la cadena. Una cadena que se ha colocado en una tabla atom se denomina nombre *atom*.

El sistema proporciona varias tablas atom. Cada tabla atom tiene un propósito diferente. Por ejemplo, Intercambio dinámico de datos (DDE) usan la tabla [atom global](#global-atom-table) para compartir cadenas item-name y topic-name con otras aplicaciones. En lugar de pasar cadenas reales, una aplicación DDE pasa los átomos globales a su aplicación asociada. El asociado usa los átomos para obtener las cadenas de la tabla atom.

Las aplicaciones pueden usar tablas atom locales para almacenar sus propias asociaciones de nombre de elemento.

El sistema usa tablas atom que no son accesibles directamente para las aplicaciones. Sin embargo, la aplicación usa estos átomos al llamar a una variedad de funciones. Por ejemplo, los formatos registrados del Portapapeles se almacenan en una tabla atom interna que usa el sistema. Una aplicación agrega átomos a esta tabla atom mediante [**la función RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) Además, las clases registradas se almacenan en una tabla atom interna utilizada por el sistema. Una aplicación agrega átomos a esta tabla atom mediante [**las funciones RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) [**o RegisterClassEx.**](/windows/desktop/api/winuser/nf-winuser-registerclassexa)

En esta sección se tratan los temas siguientes.

-   [Tabla atom global](#global-atom-table)
-   [Tabla Atom de usuario](#user-atom-table)
-   [Tablas atom locales](#local-atom-tables)
-   [Tipos atom](#atom-types)
    -   [Átomos de cadena](#string-atoms)
    -   [Átomos enteros](#integer-atoms)
-   [Recuento de creación y uso de Atom](#atom-creation-and-usage-count)
-   [Consultas de atom-table](#atom-table-queries)
-   [Formatos de cadena atom](#atom-string-formats)

## <a name="global-atom-table"></a>Tabla atom global

La tabla atom global está disponible para todas las aplicaciones. Cuando una aplicación coloca una cadena en la tabla atom global, el sistema genera un átomo que es único en todo el sistema. Cualquier aplicación que tenga el átomo puede obtener la cadena que identifica consultando la tabla atom global.

Una aplicación que define un formato de datos DDE privado para compartir datos con otras aplicaciones debe colocar el nombre de formato en la tabla atom global. Esta técnica evita conflictos con los nombres de formatos definidos por el sistema o por otras aplicaciones, y hace que los identificadores (atoms) de los mensajes o formatos estén disponibles para las otras aplicaciones.

## <a name="user-atom-table"></a>Tabla Atom de usuario

Además de la tabla atom global, la tabla atom del usuario es otra tabla atom del sistema que también se comparte entre todos los procesos. La tabla atom del usuario se usa para un pequeño número de escenarios internos a win32k. por ejemplo, nombres de módulo de Windows, cadenas conocidas en win32k, formatos OLE, etc. Aunque las aplicaciones no interactúan directamente con la tabla atom del usuario, llaman a varias API, como [RegisterClass,](/windows/win32/api/winuser/nf-winuser-registerclassexa) [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)y [RegisterClipboardFormat,](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)que agregan entradas a la tabla atom del usuario. Las entradas agregadas por `RegisterClass` pueden eliminarse mediante `UnregisterClass` . Sin embargo, las entradas agregadas por `RegisterWindowMessage` y no se eliminan hasta que finaliza la `RegisterClipboardFormat` sesión. Si la tabla atom del usuario no tiene más espacio y la cadena que se pasa aún no está en la tabla, se producirá un error en la llamada. 

### <a name="atom-table-size"></a>Atom Table Size
 
Muchas API críticas, como [CreateWindow,](/windows/win32/api/winuser/nf-winuser-createwindowa)dependen de los atomes de usuario. Por lo tanto, el agotamiento del espacio en la tabla atom del usuario dará lugar a problemas graves. Por ejemplo, es posible que todas las aplicaciones no se inicien. Estas son algunas recomendaciones para asegurarse de que la aplicación utiliza tablas atom de forma eficaz y conserva la confiabilidad y el rendimiento de la aplicación y el sistema:  

1. Debe limitar el uso de la aplicación de la tabla atom del usuario. El almacenamiento de cadenas únicas mediante API como , o ocupa espacio en la tabla atom del usuario, que otras aplicaciones usan globalmente para registrar clases de ventana mediante `RegisterClass` `RegisterWindowMessage` `RegisterClipboardFormat` cadenas. Si es posible, debe usar [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw)DeleteAtom para almacenar cadenas en una tabla / [](/windows/desktop/api/Winbase/nf-winbase-deleteatom) atom local o [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) si los átomos son necesarios entre procesos.

1. Si hay preocupación sobre la aplicación que causa problemas con la tabla atom del usuario, puede investigar la causa principal conectando el depurador del kernel e iniciando el proceso en las llamadas a `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Busque en `user32!` la pila de llamadas para ver a qué API se llama. La metodología es similar a la detección de problemas de tabla atom global que se explica en [Identificación de pérdidas globales de tablas atom.](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks) Otra manera de volcar el contenido de la tabla atom del usuario es llamar a [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) en el intervalo de posibles átomos 0xC000 a 0xFFFF. Si el recuento total de átomos aumenta constantemente mientras la aplicación se está ejecutando o no vuelve a la línea de base cuando se cierra la aplicación, hay un problema.

## <a name="local-atom-tables"></a>Tablas atom locales

Una aplicación puede usar una tabla atom local para administrar eficazmente un gran número de cadenas usadas solo dentro de la aplicación. Estas cadenas y los átomos asociados solo están disponibles para la aplicación que creó la tabla.

Una aplicación que requiere la misma cadena en varias estructuras puede reducir el uso de memoria mediante una tabla atom local. En lugar de copiar la cadena en cada estructura, la aplicación puede colocar la cadena en la tabla atom e incluir el átomo resultante en las estructuras. De este modo, una cadena solo aparece una vez en memoria, pero se puede usar muchas veces en la aplicación.

Las aplicaciones también pueden usar tablas atom locales para ahorrar tiempo al buscar una cadena determinada. Para realizar una búsqueda, una aplicación solo necesita colocar la cadena de búsqueda en la tabla atom y comparar el átomo resultante con los átomos de las estructuras pertinentes. Comparar átomos suele ser más rápido que comparar cadenas.

Las tablas atom se implementan como tablas hash. De forma predeterminada, una tabla atom local usa 37 depósitos para su tabla hash. Sin embargo, puede cambiar el número de cubos usados llamando a la [**función InitAtomTable.**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) Sin embargo, si la aplicación llama a **InitAtomTable,** debe hacerlo antes de llamar a cualquier otra función de administración de átomos.

## <a name="atom-types"></a>Tipos atom

Las aplicaciones pueden crear dos tipos de átomos: atomes de cadena y enteros. Los valores de los átomos enteros y los de cadena no se superponen, por lo que ambos tipos de átomos se pueden usar en el mismo bloque de código.

Varias funciones aceptan cadenas o atoms como parámetros. Al pasar un atom a estas funciones, una aplicación puede usar la macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) para convertir el atom en un formulario que la función pueda usar.

En las secciones siguientes se describen los tipos atom.

-   [Atoms de cadena](#string-atoms)
-   [Atoms enteros](#integer-atoms)

### <a name="string-atoms"></a>Atoms de cadena

Cuando las aplicaciones pasan cadenas terminadas en NULL a las funciones [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)y [**FindAtom,**](/windows/desktop/api/Winbase/nf-winbase-findatoma) reciben los *atomes* de cadena (enteros de 16 bits) a cambio. Los átomos de cadena tienen las siguientes propiedades:

-   Los valores de los átomos de cadena se encuentran en el intervalo 0xC000 (TOM) a 0xFFFF.
-   El caso no es significativo en las búsquedas de un nombre atom en una tabla atom. Además, toda la cadena debe coincidir en una operación de búsqueda; no se realiza ninguna coincidencia de subcadena.
-   La cadena asociada a un atom de cadena no puede tener más de 255 bytes de tamaño. Esta limitación se aplica a todas las funciones atom.
-   Se *asocia un recuento* de referencias a cada nombre de atom. El recuento se incrementa cada vez que se agrega el nombre atom a la tabla y se disminuye cada vez que se elimina el nombre atom de ella. Esto evita que distintos usuarios del mismo atom de cadena destruyan los nombres de los demás. Cuando el recuento de referencias de un nombre atom es igual a cero, el sistema quita el atom y el nombre atom de la tabla.

### <a name="integer-atoms"></a>Atoms enteros

Los átomos enteros difieren de los átomos de cadena de las maneras siguientes:

-   Los valores de los átomos enteros se encuentran en el intervalo 0x0001 a 0xBFFF **(DICONTATOM**– 1).
-   La representación de cadena de un átomo entero es dddd , donde los valores representados por \#  *dddd* son dígitos decimales. Se omiten los ceros iniciales.
-   No hay ningún recuento de referencias ni sobrecarga de almacenamiento asociada a un átomo entero.

## <a name="atom-creation-and-usage-count"></a>Recuento de creación y uso de Atom

Una aplicación crea un átomo local mediante una llamada a [**la función AddAtom;**](/windows/desktop/api/Winbase/nf-winbase-addatomw) crea un átomo global mediante una llamada a la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) Ambas funciones requieren un puntero a una cadena. El sistema busca la cadena en la tabla atom adecuada y devuelve el átomo correspondiente a la aplicación. En el caso de un átomo de cadena, si la cadena ya reside en la tabla atom, el sistema incrementa el recuento de referencias de la cadena durante este proceso.

Las llamadas repetidas para agregar el mismo nombre de átomo devuelven el mismo átomo. Si el nombre del átomo no existe en la tabla cuando se llama a [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) el nombre del átomo se agrega a la tabla y se devuelve un nuevo átomo. Si es un átomo de cadena, su recuento de referencias también se establece en uno.

Una aplicación debe llamar a [**la función DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) cuando ya no necesite usar un átomo local. debe llamar a la [**función GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) cuando ya no necesite un átomo global. En el caso de un átomo de cadena, cualquiera de estas funciones reduce el recuento de referencias del átomo correspondiente en uno. Cuando el recuento de referencias alcanza cero, el sistema elimina el nombre del átomo de la tabla.

El nombre de átomo de un átomo de cadena permanece en la tabla atom global siempre que su recuento de referencias sea mayor que cero, incluso después de que finalice la aplicación que lo colocó en la tabla. Una tabla atom local se destruye cuando finaliza la aplicación asociada, independientemente de los recuentos de referencias de los átomos de la tabla.

## <a name="atom-table-queries"></a>Atom-Table consultas

Una aplicación puede determinar si una cadena determinada ya está en una tabla atom mediante la función [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) [**o GlobalFindAtom.**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) Estas funciones buscan en una tabla atom la cadena especificada y, si la cadena está ahí, devuelven el atom correspondiente.

Una aplicación puede usar la función [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) o [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar una cadena de nombre atom de una tabla atom, siempre que la aplicación tenga el atom correspondiente a la cadena que se busca. Ambas funciones copian la cadena de nombre atom del atom especificado en un búfer y devuelven la longitud de la cadena que se copió. **GetAtomName recupera** una cadena de nombre atom de una tabla atom local y **GlobalGetAtomName** recupera una cadena de nombre atom de la tabla atom global.

## <a name="atom-string-formats"></a>Formatos de cadena atom

Las [**funciones AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom,**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)y [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) toman un puntero a una cadena terminada en NULL. Una aplicación puede especificar este puntero de una de las maneras siguientes.



|     Formato de cadena               |    Descripción                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*Dddd*           | Entero especificado como una cadena decimal. Se usa para crear o buscar un atom entero.                  |
| *nombre de atom de cadena* | Nombre de un atom de cadena. Se usa para agregar un nombre de atom de cadena a una tabla atom y recibir un atom a cambio. |



 

 

 
