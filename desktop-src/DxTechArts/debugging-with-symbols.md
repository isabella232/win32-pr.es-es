---
title: Depurar con símbolos
description: En este artículo se proporciona información general de alto nivel sobre cómo usar mejor los símbolos en el proceso de depuración.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff63e2404a07a2f0ab5adcb156d83dc989b42fd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533327"
---
# <a name="debugging-with-symbols"></a>Depurar con símbolos

En este artículo se proporciona información general de alto nivel sobre cómo usar mejor los símbolos en el proceso de depuración. Explica cómo usar el servidor de símbolos de Microsoft y también cómo configurar y usar su propio servidor de símbolos privado. Estos procedimientos recomendados pueden ayudar a aumentar la eficacia y la capacidad de depurar problemas, incluso en los casos en los que todos los símbolos y archivos ejecutables relacionados con un problema no se encuentran en el equipo.

-   [Symbols](#debugging-with-symbols)
-   [Usar símbolos para la depuración](#using-symbols-for-debugging)
-   [Obtener los símbolos necesarios](#getting-the-symbols-you-need)
    -   [Comprobar si un archivo DLL o. exe determinado y PDB en la misma carpeta coinciden](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Compruebe si todos los archivos dll y ejecutables de un conjunto de carpetas tienen PDB coincidentes](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Cómo funciona Symchk](#how-symchk-works)
-   [Servidores de símbolos](#symbol-servers)
-   [Usar el servidor de símbolos de Microsoft](#using-the-microsoft-symbol-server)
-   [Obtener símbolos manualmente](#getting-symbols-manually)
-   [Configuración de un servidor de símbolos](#setting-up-a-symbol-server)
-   [Agregar símbolos a un servidor de símbolos](#adding-symbols-to-a-symbol-server)
-   [Procedimientos recomendados](#best-practices)

## <a name="symbols"></a>Símbolos

Hay varios tipos diferentes de símbolos disponibles para la depuración. Incluyen símbolos CodeView, COFF, DBG, SYM, PDB e incluso exportan símbolos generados a partir de una tabla de exportación de archivos binarios. En estas notas del producto solo se describen los símbolos de formato de VS.NET y PDB, ya que son el formato preferido más reciente. Se generan de forma predeterminada para los proyectos que se compilan con Visual Studio.

La generación de archivos PDB para archivos ejecutables de versión no afecta a las optimizaciones ni altera significativamente el tamaño de los archivos generados. Normalmente, la única diferencia es la ruta de acceso y el nombre de archivo del archivo PDB se incrusta en el ejecutable. Por esta razón, siempre debe generar archivos PDB, incluso si no desea enviarlos con el archivo ejecutable.

Los archivos PDB se generan si un proyecto se genera mediante el modificador de compilador **/Zi** o **/Zi** (generar información de PDB), junto con el modificador **/Debug** (generar información de depuración) del enlazador. Los archivos PDB generados por el compilador se combinan y se escriben en un único archivo PDB que se coloca en el mismo directorio que el ejecutable.

De forma predeterminada, los archivos PDB contienen la siguiente información:

-   Símbolos públicos (normalmente todas las funciones, variables estáticas y globales)
-   Una lista de archivos objeto que son responsables de las secciones de código del archivo ejecutable
-   Información de optimización del puntero de marco (FPO)
-   Información de nombre y tipo para las variables locales y las estructuras de datos
-   Información del archivo de código fuente y del número de línea

Si le preocupa que los usuarios usen la información del archivo PDB para ayudarles a aplicar ingeniería inversa a su archivo ejecutable, también puede generar archivos PDB eliminados mediante la opción del enlazador **/PDBSTRIPPED: filename** . Si tiene archivos PDB existentes de los que desea quitar información privada, puede usar una herramienta denominada pdbcopy, que forma parte de las herramientas de depuración para Windows.

De forma predeterminada, los archivos PDB eliminados contienen la siguiente información:

-   Símbolos públicos (normalmente solo funciones no estáticas y variables globales)
-   Una lista de archivos objeto que son responsables de las secciones de código del archivo ejecutable
-   Información de optimización del puntero de marco (FPO)

Esta es la información mínima necesaria para permitir la depuración confiable. La información mínima también dificulta la obtención de información adicional sobre el código fuente original. Dado que se generan tanto un archivo PDB eliminado como un archivo PDB normal, puede proporcionar la versión descargada a los usuarios que puedan necesitar capacidades de depuración limitadas, pero mantener la confidencialidad de los PDB completos. Tenga en cuenta que **/PDBSTRIPPED** genera un segundo archivo PDB más pequeño, por lo que debe asegurarse de que usa el archivo PDB correcto al generar las compilaciones para distribuir de manera amplia. En un proyecto típico, un archivo PDB normal puede tener unos pocos megabytes de tamaño, pero una versión desutilizada de la PDB puede tener solo unos pocos cientos de kilobytes.

## <a name="using-symbols-for-debugging"></a>Usar símbolos para la depuración

Al depurar una aplicación que se ha bloqueado, el depurador intenta mostrarle las funciones de la pila que dieron lugar al bloqueo. Sin un archivo PDB, el depurador no puede resolver los nombres de función, sus parámetros o las variables locales almacenadas en la pila. Si depura ejecutables de 32 bits, existen situaciones en las que no puede incluso obtener seguimientos de pila confiables sin símbolos. A veces es posible examinar los valores sin formato de la pila y averiguar qué valores se pueden devolver direcciones, pero se pueden confundir fácilmente con las referencias a funciones o los datos.

Si las funciones de la pila actual se compilaron mediante la optimización del método omitir punteros de marco (**/Oy**) y si los símbolos no están presentes, el depurador no puede determinar de forma confiable qué función llamó a la función actual. Esto se debe a que, sin la información de optimización del puntero de marco (FPO) que contienen los archivos PDB, el depurador no puede confiar en el registro de puntero de marco (EBP) para apuntar al puntero de marco anterior guardado y en la dirección de devolución de la función primaria. En su lugar, se adivina. A veces, se obtiene correcto. Sin embargo, a menudo se equivoca, lo que puede ser engañoso. Si aparece una advertencia sobre los símbolos que faltan o no se han cargado símbolos, como en el ejemplo siguiente, no confíe en la pila desde ese punto hacia abajo.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

En muchos casos, es posible continuar con la depuración sin símbolos, ya que el problema se encuentra en una ubicación con símbolos precisos y no es necesario examinar las funciones más abajo en la pila de llamadas. Incluso si una biblioteca que está en la pila de llamadas no tiene archivos PDB disponibles, siempre y cuando se compilaran con punteros de Marcos, el depurador debería ser capaz de adivinar correctamente en las funciones primarias. A partir de Windows XP Service Pack 2, todos los archivos ejecutables y DLL de Windows se compilan con FPO deshabilitado, ya que hace que la depuración sea más precisa. Deshabilitar FPO también permite que los profileres de muestreo recorran la pila durante el tiempo de ejecución, con un impacto mínimo en el rendimiento. En las versiones de Windows anteriores a Windows XP SP2, todos los archivos binarios del sistema operativo requieren archivos de símbolos coincidentes que contengan información de FPO, para permitir la depuración y generación de perfiles precisas.

Si depura ejecutables nativos de 64 bits, no necesita archivos de símbolos para generar seguimientos de pila válidos, ya que los sistemas operativos y los compiladores x64 están diseñados para no requerirlos. Sin embargo, todavía necesita archivos de símbolos para recuperar los nombres de función, llamar a parámetros y variables locales.

Sin embargo, algunos casos son especialmente difíciles de depurar sin símbolos. Por ejemplo, si depura un programa para el que ha generado un archivo PDB y se bloquea en una devolución de llamada de una función de un archivo DLL para el que no tiene símbolos, no podrá ver qué función produjo la devolución de llamada, porque no podrá descodificar la pila. Esto sucede con frecuencia en bibliotecas de terceros, si no se proporcionan PDB o en componentes del sistema operativo anteriores, si los archivos PDB no están disponibles. Las devoluciones de llamada suelen ocurrir durante el paso de mensajes, la enumeración, la asignación de memoria o el control de excepciones. La depuración de estas funciones sin una pila precisa puede ser frustrante.

Para depurar de forma confiable los minivolcados que se generan en un equipo diferente o que se bloquean en código que no es de su propiedad, es importante poder tener acceso a todos los símbolos y archivos binarios de los ejecutables a los que se hace referencia en el minivolcado. Si los símbolos y los archivos binarios están disponibles en un servidor de símbolos, el depurador los obtiene automáticamente. Para obtener más información acerca de los volcados de memoria, vea las notas del producto [análisis de volcado](/windows/desktop/DxTechArts/crash-dump-analysis) de memoria.

## <a name="getting-the-symbols-you-need"></a>Obtener los símbolos necesarios

Visual Studio y otros depuradores de Microsoft, como WinDbg, se configuran normalmente para que solo funcionen si va a compilar una aplicación y depurarla en su propio equipo. Si tiene que proporcionar su archivo ejecutable a otra persona, si tiene varias versiones de un archivo DLL o. exe en el equipo, o si desea depurar con precisión una aplicación que usa Windows u otras bibliotecas, como DirectX, debe entender cómo los depuradores detectan y cargan los símbolos. El depurador utiliza la ruta de acceso de búsqueda de símbolos especificada por el usuario, que se encuentra en opciones de \\ depuración \\ de símbolos en Visual Studio, o en la \_ variable de entorno de ruta de acceso de símbolos NT \_ \_ . Normalmente, el depurador busca archivos PDB coincidentes en las siguientes ubicaciones:

-   La ubicación que se especifica dentro del archivo DLL o el archivo ejecutable.

    Si ha creado una DLL o un archivo ejecutable en el equipo, de forma predeterminada el vinculador coloca la ruta de acceso completa y el nombre de archivo del archivo PDB asociado dentro de la DLL o el archivo ejecutable. Al depurar, el depurador comprueba primero si el archivo de símbolos existe en la ubicación especificada dentro de la DLL o el archivo ejecutable. Esto resulta útil porque siempre hay símbolos disponibles para el código que ha compilado en el equipo.

-   PDB que pueden encontrarse en la misma carpeta que la DLL o el archivo ejecutable.
-   Cualquier carpeta de caché de símbolos local.
-   Cualquier servidor de símbolos de recurso compartido de archivos de red local.
-   Cualquier servidor de símbolos de Internet, como el servidor de símbolos de Microsoft.

Para asegurarse de que tiene todos los archivos PDB necesarios para la depuración precisa, instale las herramientas de depuración para Windows. Las versiones 32 y 64 de bits se pueden encontrar en [herramientas de depuración para Windows](/windows-hardware/drivers/debugger/).

Una herramienta útil que se instala con este paquete es symchk.exe. Puede ayudar a identificar símbolos que faltan o son incorrectos. Esta herramienta tiene un gran número de posibles opciones de la línea de comandos. Estos son dos de los más útiles y más útiles.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Comprobar si un archivo DLL o. exe determinado y PDB en la misma carpeta coinciden

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

La opción **/s** indica a **Symchk** que busque símbolos solo en la carpeta actual y que no busque en ningún servidor de símbolos.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Compruebe si todos los archivos dll y ejecutables de un conjunto de carpetas tienen PDB coincidentes

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

La opción **/r** establece **Symchk** para recorrer de forma recursiva las carpetas para comprobar que todos los archivos ejecutables tienen PDB coincidentes. Sin la opción **/s** , **Symchk** usa la \_ ruta de acceso del símbolo NT actual \_ \_ para buscar símbolos en cualquier servidor local o privado, o en los servidores de símbolos de Microsoft. La herramienta **Symchk** busca solo símbolos para los archivos ejecutables (. exe,. dll y similares). No se pueden usar comodines para buscar símbolos para archivos no ejecutables.

### <a name="how-symchk-works"></a>Cómo funciona Symchk

Cuando el vinculador genera archivos. dll, ejecutable y PDB, almacena GUID idénticos en cada archivo. Las herramientas de usan el GUID para determinar si un archivo PDB determinado coincide con una DLL o un archivo ejecutable. Si modifica una DLL o un archivo ejecutable (mediante el uso de un editor de recursos o la codificación de la protección de copia, o modificando su información de versión), se actualiza el GUID y el depurador no puede cargar el archivo PDB. Por esta razón, es muy importante evitar manipular la DLL o el archivo ejecutable una vez creado por el enlazador.

También puede usar la utilidad DUMPBIN incluida en VS.NET para mostrar las rutas de acceso de símbolos que se buscan y para ver si se encuentran archivos de símbolos que coinciden con un archivo ejecutable o DLL determinado. Por ejemplo:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Servidores de símbolos

Un servidor de símbolos es un repositorio para varias versiones de archivos ejecutables y de símbolos. Contiene los propios archivos de símbolos o punteros a los archivos de símbolos asociados. Los depuradores saben cómo usar los servidores de símbolos y pueden usarlos para buscar símbolos que faltan o desconocidos.

Los archivos DLL y ejecutables también están disponibles en el servidor de símbolos de Microsoft. Esto permite depurar bloqueos y examinar el código de los archivos del sistema operativo que puede que no existan en el equipo. Si un depurador encuentra un archivo ejecutable o un archivo DLL que no existe en el sistema que está utilizando para la depuración, solicita automáticamente los símbolos y una copia del archivo binario de los servidores de símbolos de Microsoft. Esto resulta útil si está depurando un componente que tiene muchas versiones (por ejemplo, msvcrt.dll) y necesita examinar el código para obtener una versión que no existe en el equipo. Esto también ayuda a depurar los minivolcados que se generan en un sistema operativo diferente del sistema que se usa para la depuración.

Microsoft publica todos los archivos PDB de todos los sistemas operativos y otros componentes redistribuidos, como el SDK de DirectX, en el servidor de símbolos accesible externamente. Esto facilita la depuración de una aplicación que usa estos archivos DLL o ejecutables. Puede usar el servidor de símbolos de Microsoft para resolver símbolos, junto con cualquier símbolo local para los componentes que se generaron en el equipo.

Puede configurar el equipo para usar el servidor de símbolos de Microsoft, que le proporciona acceso a todos los archivos de símbolos de Microsoft. También puede configurar un servidor de símbolos privado para su empresa, equipo o red, que se puede usar para almacenar varias versiones anteriores de un proyecto en el que está trabajando, o para proporcionar una caché local para los símbolos que se usan desde el servidor de símbolos de Microsoft.

Para usar un servidor de símbolos, especifique la ruta de acceso de búsqueda en una variable de entorno denominada \_ \_ ruta de acceso de símbolos NT \_ . Los depuradores y las herramientas modernas, como WinDbg, NTSD o Visual Studio, usan automáticamente esta ruta de acceso para buscar símbolos.

Cuando un depurador busca símbolos, primero busca localmente. A continuación, busca en los servidores de símbolos. Cuando encuentra un símbolo coincidente, transfiere el archivo de símbolos a la memoria caché local. Los símbolos para un archivo ejecutable o DLL típico oscilan entre 1 y 100 MB de tamaño. Por consiguiente, si depura un proceso que incluye muchos archivos dll, puede tardar algún tiempo en resolver todos los símbolos y transferirlos a una caché local.

## <a name="using-the-microsoft-symbol-server"></a>Usar el servidor de símbolos de Microsoft

El servidor de símbolos de Microsoft permite obtener todos los símbolos más recientes, incluidos los símbolos de los archivos actualizados o revisados. El servidor de símbolos de Microsoft está disponible en <https://msdl.microsoft.com/download/symbols> .

Puede tener acceso al servidor de símbolos de una de las siguientes maneras:

-   Escriba la dirección del servidor directamente. En Visual Studio, en el menú **herramientas** , elija **Opciones**, elija **depuración** y, a continuación, elija **símbolos**.
-   Use la variable de \_ entorno \_ path de símbolos de NT \_ . Se recomienda este método.

    Lo usan todas las herramientas de depuración. También se usa en Visual Studio y se lee y descodifica cuando se abre Visual Studio. Por lo tanto, si lo cambia, deberá reiniciar Visual Studio.

    Esta variable de entorno le permite especificar varios servidores de símbolos, por ejemplo, un servidor de símbolos privado interno. También permite especificar un directorio de caché local para almacenar los archivos PDB para todos los símbolos que se buscan desde servidores de símbolos, tanto internos como a través de Internet.

La sintaxis de la \_ variable de ruta de acceso de símbolos de NT \_ \_ es:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Reemplace \[ caché local \] por el nombre de un directorio del equipo en el que desea almacenar una memoria caché de los símbolos utilizados (por ejemplo,% SystemRoot% \\ Symbols o c: \\ Symbols).

El \[ servidor de símbolos privado \] es opcional. Puede apuntar a un servidor de símbolos que se encuentra en la red, o puede apuntar a un servidor de símbolos compartido por su equipo, grupo de productos o empresa.

Para usar solo el servidor de símbolos de Microsoft junto con una memoria caché local de símbolos, para acelerar el acceso a través de Internet, use la siguiente configuración para la ruta de acceso de \_ símbolos de NT \_ \_ :

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Puede encontrar otras opciones para la \_ ruta de \_ acceso de símbolos \_ de NT en el archivo de ayuda que se instala con el paquete de herramientas de depuración de Microsoft para Windows.

Los ejecutables sin símbolos pueden aumentar el tiempo necesario para iniciar un depurador si se usa un servidor de símbolos. Esto se debe a que el depurador consulta el servidor de símbolos cada vez que intenta cargar el archivo ejecutable. Por esta razón, es mejor solicitar siempre símbolos para todos los componentes.

Es posible que no se puedan solicitar símbolos para cada componente; por ejemplo, los controladores de vídeo pueden tener archivos dll en el espacio de proceso y los archivos PDB necesarios están disponibles en el servidor de símbolos de Microsoft. En este caso, hay un pequeño retraso al iniciar una sesión de depuración.

Para evitar incluso este pequeño retraso, puede ejecutar el depurador una vez, para almacenar en caché todos los símbolos localmente desde el servidor de símbolos de Microsoft. A continuación, modifique la \_ ruta de acceso de símbolos de NT \_ \_ para quitar el servidor de símbolos de Microsoft. A menos que cambien los archivos ejecutables, las comprobaciones de los archivos ejecutables que no tienen símbolos no requerirán una consulta a través de Internet, porque tiene copias en caché locales de todos los símbolos que necesita del servidor de símbolos de Microsoft.

## <a name="getting-symbols-manually"></a>Obtener símbolos manualmente

Si ha configurado el depurador correctamente, carga automáticamente los símbolos que requiera desde la memoria caché local o desde un servidor de símbolos. Si desea obtener los símbolos para un solo archivo ejecutable o para una carpeta de ejecutables, puede usar **Symchk**. Por ejemplo, si desea descargar los símbolos para el \_ archivo d3dx930.dll en la carpeta del sistema de Windows en el directorio actual, puede usar el siguiente comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

La herramienta **Symchk** tiene muchos otros usos. Para obtener más información, consulte **Symchk/?** o busque en la documentación de las herramientas de depuración de Microsoft para Windows.

## <a name="setting-up-a-symbol-server"></a>Configuración de un servidor de símbolos

La configuración de un servidor de símbolos es muy sencilla. Es útil por los siguientes motivos:

-   Para ahorrar ancho de banda o para acelerar la resolución de símbolos para su empresa, equipo o producto. Un servidor de símbolos interno en un recurso compartido de archivos local de la red almacena en caché las referencias a los servidores de símbolos externos, como el servidor de símbolos de Microsoft. Muchos usuarios pueden acceder rápidamente a un servidor de símbolos local o interno. Por lo tanto, ahorra ancho de banda y la latencia que pueden crear las solicitudes de símbolos duplicados.
-   Para almacenar símbolos para compilaciones anteriores, versiones o versiones externas de la aplicación. Al almacenar los símbolos para estas compilaciones en un servidor de símbolos al que puede acceder fácilmente, puede depurar bloqueos y problemas en estas compilaciones en cualquier equipo que tenga un depurador y una conexión al servidor de símbolos local. Esto es especialmente útil si depura los minivolcados generados por los ejecutables que no ha creado usted mismo, es decir, las compilaciones generadas por otro programador o por un equipo de compilación. Si los símbolos de estas compilaciones se almacenan en el servidor de símbolos, tendrá una depuración confiable y precisa.
-   Para mantener actualizados los símbolos. Cuando se actualizan los componentes, como los componentes del sistema operativo modificados por Windows Update o por el SDK de DirectX, puede depurar con todos los símbolos más recientes.

La configuración de un servidor de símbolos en su propia red local es tan sencilla como crear un recurso compartido de archivos en un servidor y ofrecer a los usuarios permisos totales para tener acceso al recurso compartido para crear archivos y carpetas. Este recurso compartido debe crearse en un sistema operativo de servidor, como Windows Server 2003, de modo que el número de personas que pueden tener acceso al recurso compartido simultáneamente no sea limitado.

Por ejemplo, si configura un recurso compartido de archivos en \\ \\ \\ símbolos mainserver, los miembros del equipo establecerán la \_ ruta de \_ acceso del símbolo NT \_ en lo siguiente:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

A medida que se recuperan los símbolos, los archivos y las carpetas aparecen en el \\ \\ \\ directorio compartido de símbolos de mainserver, así como en las memorias caché individuales, en el directorio c: \\ Symbols.

Suele ser todo lo que implica la configuración y el uso de su propio servidor de símbolos o del servidor de símbolos de Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Agregar símbolos a un servidor de símbolos

Para agregar, eliminar o editar archivos en un recurso compartido de servidor de símbolos, use la herramienta symstore.exe. Esta herramienta forma parte del paquete de herramientas de depuración de Microsoft para Windows. En el paquete de herramientas de depuración para Windows se incluye la documentación completa de los servidores de símbolos, la herramienta symstore y los símbolos de indización.

Puede que desee agregar símbolos directamente a su propio servidor de símbolos, como parte de un proceso de compilación, o para que los símbolos estén disponibles para todo el equipo para herramientas o bibliotecas de terceros. El proceso de agregar un símbolo a un recurso compartido de archivos del servidor de símbolos se denomina indexación de símbolos. Hay dos maneras comunes de indizar símbolos. Un archivo de símbolos se puede copiar en el servidor de símbolos. O bien, se puede copiar un puntero a la ubicación del símbolo en el servidor de símbolos. Si tiene una carpeta de archivo que contiene las compilaciones anteriores, puede que desee indizar punteros a los archivos PDB que ya están en el recurso compartido, en lugar de duplicar símbolos. Dado que los símbolos a veces pueden tener decenas de megabytes de tamaño, es una buena idea planear con anterioridad el espacio que puede necesitar para archivar todas las compilaciones del proyecto en todo el desarrollo. Si solo indiza punteros a símbolos, es posible que tenga problemas si quita las compilaciones anteriores o cambia el nombre de un recurso compartido de archivos.

Por ejemplo, para indexar de forma recursiva todos los símbolos de c: \\ dxsym \\ extra \\ Symbols que obtuvo del SDK de DirectX de octubre de 2006 en un recurso compartido de archivos de servidor de símbolos denominado \\ \\ símbolos de mainserver \\ , puede usar el siguiente comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

El parámetro **/t "comentario"** se usa para agregar una descripción a la transacción que agregó los símbolos. Esto puede ser útil cuando se realizan tareas administrativas en los símbolos.

## <a name="best-practices"></a>Prácticas recomendadas

-   Configure su propio recurso compartido de archivos del servidor de símbolos para el equipo, la compañía o el producto.
-   Configure \_ \_ \_ la ruta de acceso de símbolos de NT para que apunte a una caché local, a un servidor de símbolos privado y al servidor de símbolos de Microsoft.
-   Si un depurador no puede cargar símbolos para un componente que está depurando, póngase en contacto con el propietario del componente para solicitar símbolos, al menos un PDB eliminado.
-   Configure un sistema de compilación automatizado para indexar símbolos en el servidor de símbolos privado para cada compilación que se genera. Asegúrese de que las compilaciones que distribuya son las compilaciones generadas por este proceso. Esto garantiza que los símbolos siempre estén disponibles para los problemas de depuración.
-   Configure un servidor de símbolos para permitir que los depuradores obtengan acceso al código fuente de un módulo específico directamente desde un sistema de control de código fuente de Visual Source SAFE o Perforce. Si la información del archivo de código fuente y los símbolos de una versión de lanzamiento de un juego están indexados, los desarrolladores que tienen acceso al servidor de símbolos pueden tener depuración completa de los problemas detectados sin mantener entornos de compilación ni versiones anteriores de los archivos de código fuente en sus equipos de desarrollo. Para configurar el servidor de símbolos para permitir la indexación de la información del archivo de origen, consulte la documentación del servidor de origen.

 

 