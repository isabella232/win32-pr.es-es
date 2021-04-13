---
title: Acerca de las tablas Atom
description: En esta sección se describen las tablas Atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- átomos
- tablas Atom
- nombres de Atom
- Intercambio dinámico de datos (DDE), átomos
- DDE (Intercambio dinámico de datos), átomos
- tablas de Atom globales
- tablas de Atom locales
- átomos enteros
- átomos de cadena
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 27f7cdb4bb2dc2fd97b4dba6909022b297df1a1d
ms.sourcegitcommit: e985e0532f0f895ae418e8c2658dac819cdae3b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "104421496"
---
# <a name="about-atom-tables"></a>Acerca de las tablas Atom

Una *tabla Atom* es una tabla definida por el sistema que almacena cadenas e identificadores correspondientes. Una aplicación coloca una cadena en una tabla Atom y recibe un entero de 16 bits, denominado *Atom*, que se puede usar para tener acceso a la cadena. Una cadena que se ha colocado en una tabla Atom se denomina *nombre Atom*.

El sistema proporciona varias tablas Atom. Cada tabla Atom sirve para un propósito diferente. Por ejemplo, las aplicaciones Intercambio dinámico de datos (DDE) utilizan la [tabla global Atom](#global-atom-table) para compartir cadenas de nombre de elemento y de nombre de tema con otras aplicaciones. En lugar de pasar cadenas reales, una aplicación DDE pasa los átomos globales a su aplicación de asociado. El asociado usa los átomos para obtener las cadenas de la tabla Atom.

Las aplicaciones pueden usar tablas Atom locales para almacenar sus propias asociaciones de nombre de elemento.

El sistema utiliza tablas Atom que no son directamente accesibles para las aplicaciones. Sin embargo, la aplicación usa estos átomos al llamar a una variedad de funciones. Por ejemplo, los formatos de Portapapeles registrados se almacenan en una tabla Atom interna utilizada por el sistema. Una aplicación agrega átomos a esta tabla Atom con la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Además, las clases registradas se almacenan en una tabla Atom interna utilizada por el sistema. Una aplicación agrega átomos a esta tabla Atom con la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) o [**RegisterClassEx**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) .

Los temas siguientes se describen en esta sección.

-   [Tabla de átomo global](#global-atom-table)
-   [Tabla Atom de usuario](#user-atom-table)
-   [Tablas de Atom locales](#local-atom-tables)
-   [Tipos Atom](#atom-types)
    -   [Átomos de cadena](#string-atoms)
    -   [Átomos enteros](#integer-atoms)
-   [Creación y recuento de uso de Atom](#atom-creation-and-usage-count)
-   [Consultas de tabla Atom](#atom-table-queries)
-   [Formatos de cadena Atom](#atom-string-formats)

## <a name="global-atom-table"></a>Tabla de átomo global

La tabla global Atom está disponible para todas las aplicaciones. Cuando una aplicación coloca una cadena en la tabla global Atom, el sistema genera un átomo que es único en todo el sistema. Cualquier aplicación que tenga el átomo puede obtener la cadena que identifica consultando la tabla de Atom global.

Una aplicación que define un formato de datos DDE privado para compartir datos con otras aplicaciones debe colocar el nombre de formato en la tabla de Atom global. Esta técnica evita conflictos con los nombres de formatos definidos por el sistema o por otras aplicaciones, y hace que los identificadores (átomos) de los mensajes o formatos estén disponibles para las demás aplicaciones.

## <a name="user-atom-table"></a>Tabla Atom de usuario

Además de la tabla global Atom, la tabla Atom de usuario es otra tabla Atom del sistema que también se comparte entre todos los procesos. La tabla Atom de usuario se usa para un pequeño número de escenarios internos a Win32k; por ejemplo, nombres de módulos de Windows, cadenas conocidas en Win32k, formatos OLE, etc. Aunque las aplicaciones no interactúan directamente con la tabla de Atom de usuario, llaman a varias API, como [RegisterClass](/windows/win32/api/winuser/nf-winuser-registerclassexa), [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)y [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata), que agregan entradas a la tabla de Atom del usuario. Puede eliminar las entradas agregadas por `RegisterClass` `UnregisterClass` . Sin embargo, las entradas agregadas por `RegisterWindowMessage` y `RegisterClipboardFormat` no se eliminan hasta que finaliza la sesión. Si la tabla Atom de usuario no tiene más espacio y la cadena que se pasa todavía no está en la tabla, se producirá un error en la llamada. 

### <a name="atom-table-size"></a>Tamaño de tabla Atom
 
Muchas API críticas, incluido [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa), se basan en átomos de usuario. Por lo tanto, el agotamiento de espacio en la tabla Atom de usuario producirá problemas graves. por ejemplo, puede que todas las aplicaciones no se inicien. Estas son algunas recomendaciones para asegurarse de que la aplicación use las tablas Atom de forma eficaz y conserve la confiabilidad y el rendimiento de la aplicación y del sistema:  

1. Debe limitar el uso de la aplicación de la tabla Atom de usuario. Almacenar cadenas únicas mediante API como `RegisterClass` , `RegisterWindowMessage` o `RegisterClipboardFormat` ocupa espacio en la tabla Atom de usuario, que otras aplicaciones usan globalmente para registrar clases de ventana mediante cadenas. Si es posible, debe usar [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw) / [DeleteAtom](/windows/desktop/api/Winbase/nf-winbase-deleteatom) para almacenar las cadenas en una tabla Atom local o [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) si los átomos son necesarios entre procesos.

1. Si hay algún problema con respecto a la aplicación que causa problemas en las tablas Atom de usuario, puede investigar la causa raíz conectando el depurador del kernel y entrando en el proceso en las llamadas a `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Busque `user32!` en la pila de llamadas para ver a qué API se está llamando. La metodología es similar a la detección de problemas de tabla de átomo global explicada en [identificación de pérdidas de tabla de átomo global](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks). Otra manera de volcar el contenido de la tabla de Atom de usuario es mediante una llamada a [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) en el intervalo de átomos posibles de 0XC000 a 0xFFFF. Si el número total de átomos aumenta de forma continua mientras la aplicación se está ejecutando o no vuelve a la línea base cuando se cierra la aplicación, hay un problema.

## <a name="local-atom-tables"></a>Tablas de Atom locales

Una aplicación puede usar una tabla Atom local para administrar de forma eficaz un gran número de cadenas usadas solo dentro de la aplicación. Estas cadenas y los átomos asociados solo están disponibles para la aplicación que creó la tabla.

Una aplicación que requiere la misma cadena en un número de estructuras puede reducir el uso de memoria mediante una tabla Atom local. En lugar de copiar la cadena en cada estructura, la aplicación puede colocar la cadena en la tabla Atom e incluir el átomo resultante en las estructuras. De esta manera, una cadena solo aparece una vez en la memoria, pero se puede usar muchas veces en la aplicación.

Las aplicaciones también pueden usar tablas Atom locales para ahorrar tiempo al buscar una cadena determinada. Para realizar una búsqueda, una aplicación solo necesita colocar la cadena de búsqueda en la tabla de Atom y comparar el átomo resultante con los átomos en las estructuras pertinentes. La comparación de átomos suele ser más rápida que la comparación de cadenas.

Las tablas Atom se implementan como tablas hash. De forma predeterminada, una tabla Atom local usa cubos 37 para su tabla hash. Sin embargo, puede cambiar el número de depósitos que se utilizan llamando a la función [**InitAtomTable**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) . Sin embargo, si la aplicación llama a **InitAtomTable**, debe hacerlo antes de llamar a cualquier otra función de administración Atom.

## <a name="atom-types"></a>Tipos Atom

Las aplicaciones pueden crear dos tipos de átomos: cadena y átomos enteros. Los valores de átomos enteros y átomos de cadena no se superponen, por lo que ambos tipos de átomos se pueden usar en el mismo bloque de código.

Varias funciones aceptan cadenas o átomos como parámetros. Al pasar un átomo a estas funciones, una aplicación puede usar la macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) para convertir el átomo en un formato que pueda usar la función.

En las secciones siguientes se describen los tipos Atom.

-   [Átomos de cadena](#string-atoms)
-   [Átomos enteros](#integer-atoms)

### <a name="string-atoms"></a>Átomos de cadena

Cuando las aplicaciones pasan cadenas terminadas en null a las funciones [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)y [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) , reciben *átomos de cadena* (enteros de 16 bits) a la vuelta. Los átomos de cadena tienen las siguientes propiedades:

-   Los valores de los átomos de cadena están en el intervalo 0xC000 (MAXINTATOM) a 0xFFFF.
-   El caso no es significativo en las búsquedas de un nombre Atom en una tabla Atom. Además, toda la cadena debe coincidir en una operación de búsqueda; no se realiza ninguna coincidencia de subcadenas.
-   La cadena asociada a un átomo de cadena no puede tener más de 255 bytes de tamaño. Esta limitación se aplica a todas las funciones Atom.
-   Un *recuento de referencias* está asociado a cada nombre Atom. El recuento se incrementa cada vez que se agrega el nombre Atom a la tabla y se reduce cada vez que se elimina el nombre Atom. Esto evita que distintos usuarios del mismo átomo de cadena destruyan los nombres Atom de los demás. Cuando el recuento de referencias de un nombre Atom es igual a cero, el sistema quita el átomo y el nombre Atom de la tabla.

### <a name="integer-atoms"></a>Átomos enteros

Los átomos enteros se diferencian de los átomos de cadena de las siguientes maneras:

-   Los valores de los átomos enteros se encuentran en el intervalo de 0x0001 a 0xBFFF (**MAXINTATOM**– 1).
-   La representación de cadena de un átomo de entero es \# *dddd*, donde los valores representados por *dddd* son dígitos decimales. Los ceros a la izquierda se omiten.
-   No hay ninguna sobrecarga de almacenamiento o recuento de referencias asociada a un Atom entero.

## <a name="atom-creation-and-usage-count"></a>Creación y recuento de uso de Atom

Una aplicación crea un átomo local llamando a la función [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) . crea un átomo global mediante una llamada a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) . Ambas funciones requieren un puntero a una cadena. El sistema busca la cadena en la tabla Atom adecuada y devuelve el átomo correspondiente a la aplicación. En el caso de un átomo de cadena, si la cadena ya reside en la tabla de Atom, el sistema incrementa el recuento de referencias para la cadena durante este proceso.

Las llamadas repetidas para agregar el mismo nombre Atom devuelven el mismo átomo. Si el nombre de Atom no existe en la tabla cuando se llama a [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) , el nombre de Atom se agrega a la tabla y se devuelve un nuevo Atom. Si es un átomo de cadena, su recuento de referencias también se establece en uno.

Una aplicación debe llamar a la función [**DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) cuando ya no necesita usar un átomo local. debe llamar a la función [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) cuando ya no necesite un átomo global. En el caso de un átomo de cadena, cualquiera de estas funciones reduce el recuento de referencias del Atom correspondiente en uno. Cuando el recuento de referencias llega a cero, el sistema elimina el nombre de Atom de la tabla.

El nombre Atom de un átomo de cadena permanece en la tabla global Atom, siempre que su recuento de referencias sea mayor que cero, incluso después de que finalice la aplicación que la colocó en la tabla. Una tabla Atom local se destruye cuando finaliza la aplicación asociada, independientemente de los recuentos de referencia de los átomos de la tabla.

## <a name="atom-table-queries"></a>Consultas Atom-Table

Una aplicación puede determinar si una cadena determinada ya está en una tabla Atom mediante la función [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) o [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) . Estas funciones buscan en una tabla Atom la cadena especificada y, si la cadena está ahí, devuelven el átomo correspondiente.

Una aplicación puede usar la función [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) o [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar una cadena de nombre Atom de una tabla Atom, siempre que la aplicación tenga el átomo correspondiente a la cadena que se busca. Ambas funciones copian la cadena de nombre Atom del átomo especificado en un búfer y devuelven la longitud de la cadena que se copió. **GetAtomName** recupera una cadena de nombre Atom de una tabla Atom local y **GlobalGetAtomName** recupera una cadena de nombre Atom de la tabla global Atom.

## <a name="atom-string-formats"></a>Formatos de cadena Atom

Las funciones [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)y [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) toman un puntero a una cadena terminada en NULL. Una aplicación puede especificar este puntero de una de las siguientes maneras.



|                    |                                                                                                    |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*dddd*           | Entero especificado como una cadena decimal. Se usa para crear o buscar un Atom entero.                  |
| *nombre de Atom de cadena* | Nombre de Atom de cadena. Se usa para agregar un nombre Atom de cadena a una tabla Atom y recibir un átomo en la devolución. |



 

 

 
