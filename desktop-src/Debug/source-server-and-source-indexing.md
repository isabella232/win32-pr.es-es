---
description: El servidor de origen permite a un cliente recuperar la versión exacta de los archivos de origen que se usaron para compilar una aplicación.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Servidor de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1938a617cd6c8f613df2a1113288a27f6593336f819cde2f5380a8420c329d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815515"
---
# <a name="source-server"></a>Servidor de origen

El servidor de origen permite a un cliente recuperar la versión exacta de los archivos de origen que se usaron para compilar una aplicación. Dado que el código fuente de un módulo puede cambiar entre versiones y a lo largo de varios años, es importante ver el código fuente tal como existía cuando se creó la versión del módulo en cuestión.

El servidor de origen recupera los archivos adecuados del control de código fuente. Para usar el servidor de origen, la aplicación debe haber sido indexada de origen.

## <a name="source-indexing"></a>Indexación de origen

El sistema de indexación de origen es una colección de archivos ejecutables y scripts Perl. Los scripts de Perl requieren Perl 5.6 o superior.

Por lo general, los archivos binarios se indexa en el origen durante el proceso de compilación después de que se haya compilado la aplicación. La información necesaria para el servidor de origen se almacena en los archivos PDB.

El servidor de origen se suministra actualmente con scripts que deben funcionar con los siguientes sistemas de control de código fuente.

-   Team Foundation Server
-   Forzosamente
-   Visual SourceSafe
-   Cvs
-   Subversion

También puede crear un script personalizado para indexar el código para un sistema de control de código fuente diferente.

En la tabla siguiente se enumeran las herramientas del servidor de origen.



| Herramienta        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Este archivo es la lista maestra de todos los servidores de control de código fuente. Cada entrada tiene el formato siguiente:*MYSERVER* = *serverinfo*<br/> Cuando se usa Perforce, la información del servidor consta de la ruta de acceso de red completa al servidor, seguida de dos puntos, seguido del número de puerto que usa. Por ejemplo:<br/> MYSERVER=machine.corp.company.com:1666<br/> Este archivo se puede instalar en el equipo que ejecuta el depurador. Cuando se inicia el servidor de origen, busca Srcsrv.ini valores; Estos valores invalidarán la información contenida en el archivo PDB. Esto permite a los usuarios configurar un depurador para que use un servidor de control de código fuente alternativo en tiempo de depuración.<br/> Para obtener más información, vea el ejemplo Srcsrv.ini instalado con las herramientas del servidor de origen.<br/> |
| Ssindex.cmd | Este script compila la lista de archivos registrados en el control de código fuente junto con la información de versión de cada archivo. Almacena un subconjunto de esta información en los archivos .pdb generados al generar la aplicación. El script usa uno de los siguientes módulos perl para la interfaz con el control de código fuente: P4.pm (Perforce) o Vss.pm (Visual Source Caja fuerte). Para obtener más información, ejecute el script con -? o -?? (ayuda detallada) o examine el script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Esta utilidad enumera todos los archivos indexados dentro de un archivo .pdb. Para cada archivo, muestra la ruta de acceso completa, el servidor de control de código fuente y el número de versión del archivo. Puede usar esta información para recuperar archivos sin usar el servidor de origen. Para obtener más información, ejecute la utilidad con /? .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Los scripts de indexación usan esta utilidad para insertar la información del control de versiones en la secuencia alternativa "srcsrv" del archivo .pdb de destino. También puede leer cualquier secuencia de un archivo .pdb. Puede usar esta información para comprobar que los scripts de indexación funcionan correctamente. Para obtener más información, ejecute la utilidad con /? .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Recuperar el archivo de origen

DbgHelp API proporciona acceso a la funcionalidad del servidor de origen a través de [**la función SymGetSourceFile.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) Para recuperar el nombre del archivo de origen que se va a recuperar, llame a la función [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) o [**SymGetLineFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)

## <a name="using-source-server-with-a-debugger"></a>Usar el servidor de origen con un depurador

Para usar el servidor de origen con WinDbg, KD, NTSD o CDB, asegúrese de que ha instalado una versión reciente del paquete Herramientas de depuración para Windows (versión 6.3 o posterior). A continuación, incluya srv \* en el comando .srcpath como se muestra a continuación:

**\. srcpath srv \* ;** _c: \\ mysource_

Tenga en cuenta que este ejemplo también incluye una ruta de acceso de origen tradicional. Si el depurador no puede recuperar el archivo del servidor de origen, buscará la ruta de acceso especificada.

Si el servidor de origen recupera un archivo de origen, permanecerá en el disco duro una vez que la sesión de depuración ha terminado. Los archivos de origen se almacenan localmente en el subdirectorio src del directorio Debugging Tools for Windows installation (Herramientas de depuración para Windows instalación).

## <a name="source-server-data-blocks"></a>Bloques de datos del servidor de origen

El servidor de origen se basa en dos bloques de datos dentro del archivo PDB.

-   Lista de archivos de origen. La compilación de un módulo crea automáticamente una lista de rutas de acceso completas a los archivos de origen utilizados para compilar el módulo.
-   Bloque de datos. Al indexar el origen como se describió anteriormente, se agrega una secuencia alternativa al archivo PDB denominado "srcsrv". El script que inserta estos datos depende del proceso de compilación específico y del sistema de control de código fuente en uso.

En la versión 1 de la especificación del lenguaje, el bloque de datos se divide en tres secciones: ini, variables y archivos de origen. Tiene la sintaxis siguiente.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Todo el texto se interpreta literalmente, excepto el texto incluido en signos de porcentaje (%). El texto incluido en signos de porcentaje se trata como un nombre de variable que se va a resolver de forma recursiva, a menos que sea una de las siguientes funciones:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

El texto del parámetro debe incluirse en signos de porcentaje y tratarse como una variable que se va a expandir.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Todas las barras diagonales (/) del texto del parámetro deben reemplazarse por barras diagonales anteriores ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Toda la información de ruta de acceso del texto del parámetro se debe quitar, dejando solo el nombre de archivo.

</dd> </dl>

La sección ini contiene variables que describen los requisitos. El script de indexación puede agregar cualquier número de variables a esta sección. A continuación, se muestran algunos ejemplos:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Versión
</dt> <dd>

Versión de especificación del lenguaje. Esta variable es necesaria.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Cadena que describe el producto de control de código fuente. Esta variable es opcional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>Datetime
</dt> <dd>

Cadena que indica la fecha y hora en que se procesó el archivo PDB. Esta variable es opcional.

</dd> </dl>

La sección variables contiene variables que describen cómo extraer un archivo del control de código fuente. También se puede usar para definir el texto que se usa normalmente como variables para reducir el tamaño del bloque de datos.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Describe cómo compilar la ruta de acceso de destino para el archivo extraído. Se trata de una variable obligatoria.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Describe cómo compilar el comando para extraer el archivo del control de código fuente. Esto incluye el nombre del archivo ejecutable y sus parámetros de línea de comandos. Se trata de una variable obligatoria.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Cadena que enumera las variables de entorno que se crearán durante la extracción de archivos. Separe varias entradas con un carácter de retroceso ( \\ b). Se trata de una variable opcional.

</dd> </dl>

La sección de archivos de origen contiene una entrada para cada archivo de origen que se ha indexado. El contenido de cada línea se interpreta como variables con los nombres VAR1, VAR2, VAR3, y así sucesivamente hasta VAR10. Las variables están separadas por asteriscos. VAR1 debe especificar la ruta de acceso completa al archivo de origen como se muestra en otra parte del archivo PDB. Por ejemplo, la siguiente línea:

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

se interpreta de la siguiente manera:

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

En este ejemplo, VAR4 es un número de versión. Sin embargo, la mayoría de los sistemas de control de código fuente admiten el etiquetado de archivos de forma que se pueda restaurar el estado de origen de una compilación determinada. Por lo tanto, también puede usar la etiqueta para la compilación. El bloque de datos de ejemplo se puede modificar para que contenga una variable como la siguiente:

``` syntax
LABEL=BUILD47
```

A continuación, presumiendo que el sistema de control de código fuente usa at sign (@) para indicar una etiqueta, puede modificar la variable SRCSRVCMD como se indica a continuación:

**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**

## <a name="how-source-server-works"></a>Funcionamiento del servidor de origen

El cliente del servidor de origen se implementa en Symsrv.dll. El cliente no extrae información directamente del archivo PDB; usa un controlador de símbolos como el implementado en Dbghelp.dll. Básicamente, es un motor de sustitución de variables recursiva que crea una línea de comandos que se puede usar para extraer el archivo de código fuente adecuado del sistema de control de código fuente. El código no debe llamar a Symsrv.dll directamente. Para integrar su funcionalidad en la aplicación, use la [**función SymGetSourceFile.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)

La primera versión del servidor de origen funciona de la siguiente manera. Este comportamiento puede cambiar en versiones futuras.

-   El cliente llama a la **función SrcSrvInit con** la ruta de acceso de destino que se usará como base para todas las extracciones de archivos de origen. Almacena esta ruta de acceso en la variable TARG.
-   El cliente extrae la secuencia Srcsrv de la PDB cuando se carga el módulo PDB y llama a la función **SrcSrvLoadModule** para pasar el bloque de datos al servidor de origen.
-   Cuando Dbghelp recupera un archivo de código fuente, el cliente llama a la función **SrcSrvGetFile** para recuperar los archivos de código fuente del control de código fuente.
-   El servidor de origen busca en las entradas del archivo de origen del bloque de datos una entrada que coincida con el archivo solicitado. Rellena VAR1 a VAR *n con* el contenido de la entrada del archivo de origen. A continuación, expande la variable SRCSRVTRG mediante VAR1 a VAR *n*. Si el archivo ya está en esta ubicación, devuelve la ubicación al autor de la llamada. De lo contrario, expande la variable SRCSRVCMD para compilar el comando necesario para recuperar el archivo del control de código fuente y copiarlo en la ubicación de destino. Por último, ejecuta este comando.

## <a name="creating-a-source-control-provider-module"></a>Crear un módulo de proveedor de control de código fuente

El servidor de origen incluye módulos de proveedor para Perforce (p4.pm) y Visual Source Caja fuerte (vss.pm). Para crear su propio módulo de proveedor, debe implementar el siguiente conjunto de interfaces.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**
</dt> <dd>

Propósito: muestra información de uso de módulo simple en STDOUT.

Parámetros: None

Valor devuelto: None

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**
</dt> <dd>

Propósito: muestra información detallada sobre el uso de módulos en STDOUT.

Parámetros: None

Valor devuelto: None

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new( \@ CommandArguments)**
</dt> <dd>

Propósito: inicializa una instancia del módulo del proveedor.

Parámetros: todos @ARGV los argumentos no reconocidos por SSIndex.cmd como argumentos generales.

Valor devuelto: referencia que se puede usar en operaciones posteriores.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**
</dt> <dd>

Propósito: permite al módulo recopilar la información de indexación de origen necesaria para el directorio especificado por el $SourcePath parámetro . El módulo no debe suponer que esta entrada se llamará solo una vez para cada instancia de objeto, ya que SSIndex.cmd puede llamarla varias veces para distintas rutas de acceso.

Parámetros: (1) El directorio local que contiene el origen que se va a indexar. (2) Referencia a un hash que contiene todas las entradas del archivo Srcsrv.ini especificado.

Valor devuelto: None

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**
</dt> <dd>

Propósito: proporciona la información necesaria para extraer un único archivo específico del sistema de control de código fuente.

Parámetros: nombre de archivo completo

Valor devuelto: (1) Referencia hash de las variables necesarias para interpretar el valor devuelto $FileEntry. SSIndex.cmd almacena en caché estas variables para cada archivo de origen utilizado por un único archivo de depuración para reducir la cantidad de información escrita en el flujo de índice de origen. (2) Entrada de archivo que se va a escribir en el flujo de índice de origen para permitir que SrcSrv.dll extraer este archivo del control de código fuente. El formato exacto de esta línea es específico del sistema de control de código fuente.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**
</dt> <dd>

Propósito: proporciona una cadena descriptiva para identificar el proveedor de control de código fuente al usuario final.

Parámetros: None

Valor devuelto: nombre descriptivo del sistema de control de código fuente.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**
</dt> <dd>

Propósito: permite que el proveedor de control de código fuente agregue variables específicas del control de código fuente al flujo de código fuente para cada archivo de depuración. Los módulos de ejemplo usan este método para escribir las variables EXTRACT \_ CMD y EXTRACT TARGET \_ necesarias.

Parámetros: None

Valor devuelto: lista de entradas para las variables de flujo de origen.

</dd> </dl>

 

 




