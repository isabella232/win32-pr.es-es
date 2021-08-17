---
title: Depuración con símbolos
description: En este artículo se proporciona información general de alto nivel sobre cómo usar mejor los símbolos en el proceso de depuración.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdabd1a99f203adb2422cc4bbc71c3fb2f6108a0a3869077e97683bdcf830100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070565"
---
# <a name="debugging-with-symbols"></a>Depuración con símbolos

En este artículo se proporciona información general de alto nivel sobre cómo usar mejor los símbolos en el proceso de depuración. Se explica cómo usar el servidor de símbolos de Microsoft y también cómo configurar y usar su propio servidor de símbolos privado. Estos procedimientos recomendados pueden ayudar a aumentar su eficacia y capacidad para depurar problemas, incluso en los casos en los que todos los símbolos y archivos ejecutables relacionados con un problema no se encuentran en el equipo.

-   [Symbols](#debugging-with-symbols)
-   [Usar símbolos para la depuración](#using-symbols-for-debugging)
-   [Obtención de los símbolos que necesita](#getting-the-symbols-you-need)
    -   [Compruebe si un archivo DLL o .exe archivo y PDB en la misma carpeta coinciden](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Compruebe si todos los archivos DLL y ejecutables de un conjunto de carpetas tienen archivos PDU correspondientes.](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Funcionamiento de symchk](#how-symchk-works)
-   [Servidores de símbolos](#symbol-servers)
-   [Uso del servidor de símbolos de Microsoft](#using-the-microsoft-symbol-server)
-   [Obtención manual de símbolos](#getting-symbols-manually)
-   [Configurar un servidor de símbolos](#setting-up-a-symbol-server)
-   [Agregar símbolos a un servidor de símbolos](#adding-symbols-to-a-symbol-server)
-   [Procedimientos recomendados](#best-practices)

## <a name="symbols"></a>Símbolos

Hay varios tipos diferentes de símbolos disponibles para la depuración. Incluyen símbolos CodeView, COFF, DBG, SYM, PDB e incluso símbolos de exportación generados a partir de una tabla de exportación de archivos binarios. En estas white paper solo se de VS.NET y los símbolos de formato PDB, ya que son el formato preferido más reciente. Se generan de forma predeterminada para los proyectos que se compilan mediante Visual Studio.

La generación de archivos PDB para archivos ejecutables de versión no afecta a las optimizaciones ni modifica significativamente el tamaño de los archivos generados. Normalmente, la única diferencia es la ruta de acceso y el nombre de archivo del archivo PDB se incrusta en el ejecutable. Por este motivo, siempre debe generar archivos PDB, incluso si no desea enviarlos con el archivo ejecutable.

Los archivos PDB se generan si un proyecto se compila mediante el modificador del compilador **/Zi** o **/ZI** (Generar información de PDB), junto con el modificador del vinculador **/DEBUG** (Generar información de depuración). Los archivos PDB generados por el compilador se combinan y escriben en un único archivo PDB que se coloca en el mismo directorio que el ejecutable.

De forma predeterminada, los archivos PDB contienen la siguiente información:

-   Símbolos públicos (normalmente todas las funciones, variables estáticas y globales)
-   Lista de archivos objeto que son responsables de las secciones de código en el archivo ejecutable
-   Información de optimización de puntero de marco (FPO)
-   Información de nombre y tipo para variables locales y estructuras de datos
-   Información de número de línea y archivo de origen

Si le preocupa que las personas usen la información del archivo PDB para ayudarles a diseñar el archivo ejecutable de forma inversa, también puede generar archivos PDB quitados mediante la opción del vinculador **/PDBSTRIPPED:filename.** Si tiene archivos PDB existentes de los que desea quitar información privada, puede usar una herramienta denominada pdbcopy, que forma parte de las herramientas de depuración para Windows.

De forma predeterminada, los archivos PDB quitados contienen la siguiente información:

-   Símbolos públicos (normalmente solo funciones no estáticas y variables globales)
-   Lista de archivos objeto que son responsables de las secciones de código en el archivo ejecutable
-   Información de optimización de puntero de marco (FPO)

Esta es la información mínima necesaria para permitir la depuración confiable. La información mínima también dificulta la obtención de información adicional sobre el código fuente original. Dado que se generan tanto un archivo PDB quitado como un archivo PDB normal, puede proporcionar la versión quitada a los usuarios que pueden necesitar capacidades de depuración limitadas, pero mantener la confidencialidad de los archivos PDB completos. Tenga en cuenta que **/PDBSTRIPPED** genera un segundo archivo PDB más pequeño, por lo que debe asegurarse de usar el archivo PDB correcto al generar compilaciones para distribuirlas ampliamente. Para un proyecto típico, una PDB normal puede tener un tamaño de algunos megabytes, pero una versión quitada de la PDB puede tener solo unos cientos de kilobytes.

## <a name="using-symbols-for-debugging"></a>Usar símbolos para la depuración

Al depurar una aplicación que se ha bloqueado, el depurador intenta mostrar las funciones de la pila que provocaron el bloqueo. Sin un archivo PDB, el depurador no puede resolver los nombres de función, sus parámetros ni las variables locales almacenadas en la pila. Si depura archivos ejecutables de 32 bits, hay situaciones en las que ni siquiera puede obtener seguimientos de pila confiables sin símbolos. A veces es posible ver los valores sin procesar de la pila y averiguar qué valores pueden ser direcciones de retorno, pero estos se pueden confundir fácilmente con referencias de función o datos.

Si las funciones de la pila actual se compilaron mediante la optimización Omitir punteros de marco (**/Oy**) y si los símbolos no están presentes, el depurador no puede determinar de forma confiable qué función llamó a la función actual. Esto se debe a que, sin la información de optimización de puntero de marco (FPO) que contienen los PDU, el depurador no puede confiar en el registro de puntero de marco (EBP) para apuntar al puntero de marco anterior guardado y a la dirección de retorno de la función primaria. En su lugar, supone. A veces, lo hace correcto. Sin embargo, a menudo se equivocó, lo que puede ser confuso. Si ve una advertencia sobre los símbolos que faltan o no hay símbolos cargados, como en el ejemplo siguiente, no confíe en la pila desde ese punto hacia abajo.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

En muchos casos, es posible continuar la depuración sin símbolos, ya que el problema se encuentra en una ubicación que tiene símbolos precisos y no es necesario mirar las funciones más abajo en la pila de llamadas. Incluso si una biblioteca que se encuentra en la pila de llamadas no tiene archivos PDU disponibles, siempre y cuando se compilaron con punteros de marco, el depurador debe poder adivinar correctamente en las funciones primarias. A partir Windows XP Service Pack 2, todos los archivos dll y ejecutables Windows se compilan con FPO deshabilitado, ya que hace que la depuración sea más precisa. Deshabilitar FPO también permite a los perfiles de muestreo recorrer la pila durante el tiempo de ejecución, con un impacto mínimo en el rendimiento. En las versiones de Windows antes de Windows XP SP2, todos los archivos binarios del sistema operativo requieren archivos de símbolos que coincidan con la información de FPO, para permitir la depuración y generación de perfiles precisas.

Si depura archivos ejecutables nativos de 64 bits, no necesita archivos de símbolos para generar seguimientos de pila válidos, ya que los compiladores y sistemas operativos x64 están diseñados para no requerirlos. Sin embargo, todavía necesita archivos de símbolos para recuperar los nombres de función, los parámetros de llamada y las variables locales.

Sin embargo, algunos casos son especialmente difíciles de depurar sin símbolos. Por ejemplo, si depura un programa para el que ha compilado un archivo PDB y se bloquea en una devolución de llamada de una función de un archivo DLL para el que no tiene símbolos, no podrá ver qué función produjo la devolución de llamada, ya que no podrá descodificar la pila. Esto suele ocurrir en bibliotecas de terceros, si no se proporcionan archivos PDU, o en componentes antiguos del sistema operativo, si no están disponibles. Las devoluciones de llamada suelen producirse durante el paso de mensajes, la enumeración, la asignación de memoria o el control de excepciones. Depurar estas funciones sin una pila precisa puede resultar frustrante.

Para depurar de forma confiable minivolcaciones que se generan en un equipo diferente o que se bloquean en código que no es de su propiedad, es importante poder acceder a todos los símbolos y archivos binarios de los ejecutables a los que se hace referencia en el minivolcar. Si los símbolos y archivos binarios están disponibles en un servidor de símbolos, el depurador los obtiene automáticamente. Para obtener más información sobre los minivolcadores, consulte las white paper crash dump analysis (Análisis de volcado de [memoria).](/windows/desktop/DxTechArts/crash-dump-analysis)

## <a name="getting-the-symbols-you-need"></a>Obtención de los símbolos que necesita

Visual Studio y otros depuradores de Microsoft, como WinDbg, se suelen configurar para que funcionen simplemente si va a compilar una aplicación y depurarla en su propio equipo. Si necesita proporcionar el archivo ejecutable a otra persona, si tiene varias versiones de un archivo DLL o un archivo .exe en el equipo, o si desea depurar con precisión una aplicación que usa Windows u otras bibliotecas, como DirectX, debe comprender cómo los depuradores encuentran y cargan símbolos. El depurador usa la ruta de acceso de búsqueda de símbolos especificada por el usuario (que se encuentra en Opciones de depuración de símbolos en Visual Studio) o la variable de entorno \\ \\ NT SYMBOL \_ \_ \_ PATH. Normalmente, el depurador busca archivos PDU que coincidan en las siguientes ubicaciones:

-   La ubicación que se especifica dentro del archivo DLL o el archivo ejecutable.

    Si ha compilado un archivo DLL o un archivo ejecutable en el equipo, el vinculador coloca de forma predeterminada la ruta de acceso completa y el nombre de archivo del archivo PDB asociado dentro del archivo DLL o ejecutable. Al depurar, el depurador comprueba primero si el archivo de símbolos existe en la ubicación especificada dentro de la DLL o el archivo ejecutable. Esto resulta útil, ya que siempre tiene símbolos disponibles para el código que ha compilado en el equipo.

-   ARCHIVOS PDF que pueden estar presentes en la misma carpeta que el archivo DLL o ejecutable.
-   Cualquier carpeta de caché de símbolos local.
-   Cualquier servidor de símbolos de recurso compartido de archivos de red local.
-   Cualquier servidor de símbolos de Internet, como el servidor de símbolos de Microsoft.

Para asegurarse de que tiene todos los archivos PDU que necesita para una depuración precisa, instale las herramientas de depuración para Windows. Las versiones de 32 y 64 bits se pueden encontrar en Herramientas de depuración [para Windows](/windows-hardware/drivers/debugger/).

Una herramienta útil que se instala con este paquete es symchk.exe. Puede ayudar a identificar símbolos que faltan o son incorrectos. Esta herramienta tiene un gran número de posibles opciones de línea de comandos. Estos son dos de los más útiles y de uso frecuente.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Compruebe si un archivo DLL o .exe archivo y PDB en la misma carpeta coinciden

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s .

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

/s **.** Option indica **a symchk** que busque símbolos solo en la carpeta actual y que no busque en ningún servidor de símbolos.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Compruebe si todos los archivos DLL y ejecutables de un conjunto de carpetas tienen archivos PDU correspondientes.

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

La **opción /r** establece **symchk** para recorrer de forma recursiva las carpetas, con el fin de comprobar que todos los archivos ejecutables tienen archivos PDU correspondientes. Sin la **opción /s,** **symchk** usa la ruta de acceso actual de SÍMBOLO DE NT para buscar símbolos en cualquier servidor privado o local, o en los servidores de símbolos \_ \_ de \_ Microsoft. La **herramienta symchk** solo busca símbolos para archivos ejecutables (.exe, .dll y similares). No se pueden usar caracteres comodín para buscar símbolos para archivos no ejecutables.

### <a name="how-symchk-works"></a>Funcionamiento de symchk

Cuando el vinculador genera archivos .dll, ejecutables y PDB, almacena GUID idénticos en cada archivo. Las herramientas usan el GUID para determinar si un archivo PDB determinado coincide con un archivo DLL o un archivo ejecutable. Si modifica un archivo DLL o ejecutable (mediante un editor de recursos o la codificación de protección de copia o modificando su información de versión), el GUID se actualiza y el depurador no puede cargar el archivo PDB. Por este motivo, es muy importante evitar manipular el archivo DLL o ejecutable después de que lo haya creado el vinculador.

También puede usar la utilidad DUMPBIN que se incluye con VS.NET para mostrar las rutas de acceso de símbolos que se buscan y para ver si se encuentran archivos de símbolos que coincidan con un archivo DLL o ejecutable determinado. Por ejemplo:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Servidores de símbolos

Un servidor de símbolos es un repositorio para varias versiones de archivos ejecutables y de símbolos. Contiene los propios archivos de símbolos o punteros a los archivos de símbolos asociados. Los depuradores comprenden cómo usar servidores de símbolos y pueden usarlos para buscar símbolos que faltan o desconocidos.

Los archivos DLL y ejecutables también están disponibles en el servidor de símbolos de Microsoft. Esto permite depurar bloqueos y examinar el código de los archivos del sistema operativo que pueden no existir en el equipo. Si un depurador encuentra un archivo ejecutable o un archivo DLL que no existe en el sistema que se usa para la depuración, solicita automáticamente los símbolos y una copia del archivo binario de los servidores de símbolos de Microsoft. Esto resulta útil si está depurando un componente que tiene muchas versiones (por ejemplo, msvcrt.dll) y necesita examinar el código de una versión que no existe en el equipo. Esto también ayuda a depurar minivolcaciones que se generan en un sistema operativo diferente del sistema que se usa para la depuración.

Microsoft publica todos los archivos PDB para todos los sistemas operativos y otros componentes redistribuidos, como el SDK de DirectX, en su servidor de símbolos accesible externamente. Esto facilita la depuración de una aplicación que usa estos archivos DLL o ejecutables. Puede usar el servidor de símbolos de Microsoft para resolver símbolos, junto con los símbolos locales para los componentes que se crearon en el equipo.

Puede configurar el equipo para que use el servidor de símbolos de Microsoft, que proporciona acceso a todos los archivos de símbolos de Microsoft. También puede configurar un servidor de símbolos privado para su empresa, equipo o red, que se puede usar para almacenar varias versiones anteriores de un proyecto en el que está trabajando, o para proporcionar una caché local para los símbolos que usa desde el servidor de símbolos de Microsoft.

Para usar un servidor de símbolos, especifique la ruta de acceso de búsqueda en una variable de entorno denominada \_ NT \_ SYMBOL \_ PATH. Los depuradores y herramientas modernas, como WinDbg, NTSD o Visual Studio, usan automáticamente esta ruta de acceso para buscar símbolos.

Cuando un depurador busca símbolos, primero busca localmente. A continuación, busca en servidores de símbolos. Cuando encuentra un símbolo que coincide, transfiere el archivo de símbolos a la memoria caché local. Los símbolos de un archivo DLL o ejecutable típico oscilan entre 1 y 100 MB de tamaño. Por lo tanto, si está depurando un proceso que incluye muchos archivos DLL, puede tardar algún tiempo en resolver todos los símbolos y transferirlos a una caché local.

## <a name="using-the-microsoft-symbol-server"></a>Uso del servidor de símbolos de Microsoft

El servidor de símbolos de Microsoft permite obtener todos los símbolos más recientes, incluidos los símbolos de los archivos con revisión o actualizados. El servidor de símbolos de Microsoft está disponible en <https://msdl.microsoft.com/download/symbols> .

Puede acceder al servidor de símbolos de una de las maneras siguientes:

-   Escriba la dirección del servidor directamente. En Visual Studio, en el **menú Herramientas,** elija **Opciones,** depuración y **símbolos.**
-   Use la variable de entorno \_ NT \_ SYMBOL \_ PATH. Se recomienda este método.

    Se usa en todas las herramientas de depuración. También lo usa Visual Studio y se lee y descodifica cuando se Visual Studio. Por lo tanto, si lo cambia, debe reiniciar Visual Studio.

    Esta variable de entorno permite especificar varios servidores de símbolos, por ejemplo, un servidor de símbolos privado interno. También permite especificar un directorio de caché local para almacenar archivos PDU para todos los símbolos que busque en los servidores de símbolos, tanto internamente como a través de Internet.

La sintaxis de la \_ variable NT SYMBOL PATH \_ \_ es:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Reemplace la memoria caché local por el nombre de un directorio en el equipo en el que desea almacenar una memoria caché de los símbolos usados, por \[ \] ejemplo, símbolos %SYSTEMROOT% o \\ símbolos \\ c:.

El \[ servidor de símbolos privado es \] opcional. Puede apuntar a un servidor de símbolos que se encuentra en la red o a un servidor de símbolos compartido por su equipo, grupo de productos o empresa.

Para usar solo el servidor de símbolos de Microsoft junto con una caché local de símbolos, para acelerar el acceso a través de Internet, use la siguiente configuración para \_ NT \_ SYMBOL \_ PATH:

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Puede encontrar otras opciones para NT SYMBOL PATH en el archivo de ayuda que se instala con Microsoft \_ \_ \_ Debugging Tools for Windows package.

Los ejecutables sin símbolos pueden aumentar el tiempo que se tarda en iniciar un depurador si se usa un servidor de símbolos. Esto se debe a que el depurador consulta el servidor de símbolos cada vez que intenta cargar el ejecutable. Por este motivo, es mejor solicitar siempre símbolos para todos los componentes.

Es posible que no sea posible solicitar símbolos para cada componente; por ejemplo, los controladores de vídeo pueden tener archivos DLL en el espacio de proceso y los archivos PDB necesarios están disponibles en el servidor de símbolos de Microsoft. En este caso, hay un pequeño retraso al iniciar una sesión de depuración.

Para evitar incluso este pequeño retraso, puede ejecutar el depurador una vez para almacenar en caché todos los símbolos localmente desde el servidor de símbolos de Microsoft. A continuación, modifique \_ la RUTA DE ACCESO DEL SÍMBOLO DE NT para quitar el servidor de símbolos de \_ \_ Microsoft. A menos que cambien los archivos ejecutables, las comprobaciones de archivos ejecutables que no tengan símbolos no requerirán una consulta a través de Internet, ya que tiene copias en caché locales de todos los símbolos que necesita del servidor de símbolos de Microsoft.

## <a name="getting-symbols-manually"></a>Obtención manual de símbolos

Si ha configurado el depurador correctamente, carga automáticamente los símbolos que necesita de la memoria caché local o de un servidor de símbolos. Si desea obtener los símbolos para un solo archivo ejecutable o para una carpeta de ejecutables, puede usar **symchk**. Por ejemplo, si desea descargar los símbolos del archivo30.dll d3dx9 de la carpeta Windows System en el directorio actual, puede usar \_ el siguiente comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

La **herramienta symchk** tiene muchos otros usos. Para obtener más información, **vea symchk /?** o busque en la documentación de Microsoft Debugging Tools for Windows .

## <a name="setting-up-a-symbol-server"></a>Configurar un servidor de símbolos

La configuración de un servidor de símbolos es muy sencilla. Es útil por los siguientes motivos:

-   Para ahorrar ancho de banda o para acelerar la resolución de símbolos para su empresa, equipo o producto. Un servidor de símbolos interno en un recurso compartido de archivos local de la red almacena en caché las referencias a servidores de símbolos externos, como el servidor de símbolos de Microsoft. Muchas personas pueden acceder rápidamente a un servidor de símbolos local o interno al mismo tiempo. Por lo tanto, ahorra ancho de banda y la latencia que pueden crear las solicitudes de símbolos duplicadas.
-   Para almacenar símbolos para compilaciones antiguas, versiones o versiones externas de la aplicación. Al almacenar los símbolos de estas compilaciones en un servidor de símbolos al que puede acceder fácilmente, puede depurar bloqueos y problemas en estas compilaciones en cualquier equipo que tenga un depurador y una conexión al servidor de símbolos local. Esto es especialmente útil si depura minivolcaciones generadas por archivos ejecutables que no ha creado usted mismo, es decir, compilaciones generadas por otro programador o por una máquina de compilación. Si los símbolos de estas compilaciones se almacenan en el servidor de símbolos, tendrá una depuración confiable y precisa.
-   Para mantener los símbolos actualizados. Cuando se actualizan los componentes, como los componentes del sistema operativo que se modifican mediante Windows Update o el SDK de DirectX, puede seguir depurando con todos los símbolos más recientes.

Configurar un servidor de símbolos en su propia red local es tan sencillo como crear un recurso compartido de archivos en un servidor y conceder a los usuarios permisos completos para acceder al recurso compartido, para crear archivos y carpetas. Este recurso compartido debe crearse en un sistema operativo de servidor, como Windows Server 2003, para que el número de personas que pueden acceder al recurso compartido simultáneamente no esté limitado.

Por ejemplo, si configura un recurso compartido de archivos en símbolos mainserver, los miembros del equipo establecen \\ \\ nt symbol path en \\ \_ lo \_ \_ siguiente:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

A medida que se recuperan los símbolos, los archivos y las carpetas aparecen en el directorio compartido de símbolos mainserver, así como en las memorias caché individuales, en el \\ \\ \\ directorio c: \\ symbols.

Esto suele ser todo lo que implica la configuración y el uso de su propio servidor de símbolos o el servidor de símbolos de Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Agregar símbolos a un servidor de símbolos

Para agregar, eliminar o editar archivos en un recurso compartido de servidor de símbolos, use la herramienta symstore.exe símbolos. Esta herramienta forma parte de las Herramientas de depuración de Microsoft para Windows paquete. La documentación completa sobre los servidores de símbolos, la herramienta symstore y los símbolos de indexación se incluye en herramientas de depuración Windows paquete.

Es posible que quiera agregar símbolos directamente a su propio servidor de símbolos, como parte de un proceso de compilación, o que los símbolos estén disponibles para todo el equipo para bibliotecas o herramientas de terceros. El proceso de agregar un símbolo a un recurso compartido de archivos de servidor de símbolos se denomina símbolos de indexación. Hay dos maneras comunes de indexar símbolos. Se puede copiar un archivo de símbolos en el servidor de símbolos. O bien, se puede copiar un puntero a la ubicación del símbolo en el servidor de símbolos. Si tiene una carpeta de archivo que contiene las compilaciones antiguas, puede indexar punteros a los archivos PDB que ya están en el recurso compartido, en lugar de duplicar símbolos. Dado que los símbolos a veces pueden tener decenas de megabytes de tamaño, es una buena idea planear con antelación cuánto espacio puede necesitar para archivar todas las compilaciones del proyecto a lo largo del desarrollo. Si indexa solo punteros a símbolos, puede tener problemas si quita compilaciones antiguas o cambia el nombre de un recurso compartido de archivos.

Por ejemplo, para indexar recursivamente todos los símbolos de c: dxsym Extras Symbols que obtuvo del SDK de DirectX de octubre de \\ \\ 2006 en un recurso compartido de archivos de servidor de símbolos denominado \\ \\ \\ mainserver symbols, puede usar el \\ siguiente comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

El **parámetro /t "comment"** se usa para agregar una descripción a la transacción que agregó los símbolos. Esto puede ser útil al realizar tareas administrativas en los símbolos.

## <a name="best-practices"></a>Procedimientos recomendados

-   Configure su propio recurso compartido de archivos de servidor de símbolos para su equipo, empresa o producto.
-   Configure NT SYMBOL PATH para que apunte a una caché local, a un servidor de \_ símbolos privado y al servidor de símbolos de \_ \_ Microsoft.
-   Si un depurador no puede cargar símbolos para un componente que está depurando, póngase en contacto con el propietario del componente para solicitar símbolos, al menos una PDB quitada.
-   Configure un sistema de compilación automatizado para indexar símbolos en el servidor de símbolos privado para cada compilación que se genere. Asegúrese de que las compilaciones que distribuye son las compilaciones generadas por este proceso. Esto garantiza que los símbolos estén siempre disponibles para depurar problemas.
-   Configure un servidor de símbolos para permitir que los depuradores accedan al código fuente de un módulo específico directamente desde un sistema de control de código fuente basado en Visual Source Caja fuerte o Perforce. Si se indexan la información del archivo de origen y los símbolos de una versión publicada de un juego, los desarrolladores que tienen acceso al servidor de símbolos pueden tener una depuración de nivel de origen completa de los problemas notificados, sin mantener los entornos de compilación ni las versiones anteriores de los archivos de origen en sus equipos de desarrollo. Para configurar el servidor de símbolos para permitir la indexación de la información del archivo de origen, consulte la documentación del servidor de origen.

 

 
