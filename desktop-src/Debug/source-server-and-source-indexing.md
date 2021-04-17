---
description: El servidor de origen permite a un cliente recuperar la versión exacta de los archivos de origen que se usaron para compilar una aplicación.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Servidor de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105660001"
---
# <a name="source-server"></a>Servidor de origen

El servidor de origen permite a un cliente recuperar la versión exacta de los archivos de origen que se usaron para compilar una aplicación. Dado que el código fuente de un módulo puede cambiar entre versiones y a lo largo de un año, es importante examinar el código fuente tal como existía cuando se compiló la versión del módulo en cuestión.

El servidor de origen recupera los archivos correspondientes del control de código fuente. Para usar el servidor de origen, la aplicación debe haber sido indizada por el origen.

## <a name="source-indexing"></a>Indexación de origen

El sistema de indexación de origen es una colección de archivos ejecutables y scripts Perl. Los scripts Perl requieren Perl 5,6 o superior.

Por lo general, los archivos binarios se indizan en el origen durante el proceso de compilación una vez que se ha compilado la aplicación. La información que necesita el servidor de origen se almacena en los archivos PDB.

El servidor de origen se distribuye actualmente con scripts que deben funcionar con los siguientes sistemas de control de código fuente.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   CSV
-   Subversion

También puede crear un script personalizado para indizar el código para un sistema de control de código fuente diferente.

En la tabla siguiente se enumeran las herramientas de servidor de origen.



| Herramienta        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Este archivo es la lista maestra de todos los servidores de control de código fuente. Cada entrada tiene el siguiente *formato:* = *ServerInfo*<br/> Al usar Perforce, la información del servidor se compone de la ruta de acceso de red completa al servidor, seguida de dos puntos, seguido del número de puerto que usa. Por ejemplo:<br/> MiEquipo = Machine. Corp. Company. com: 1666<br/> Este archivo se puede instalar en el equipo que ejecuta el depurador. Cuando se inicia el servidor de origen, examina Srcsrv.ini para los valores; Estos valores reemplazarán la información contenida en el archivo PDB. Esto permite a los usuarios configurar un depurador para utilizar un servidor de control de código fuente alternativo en tiempo de depuración.<br/> Para obtener más información, vea el ejemplo Srcsrv.ini instalado con las herramientas del servidor de origen.<br/> |
| Ssindex. cmd | Este script crea la lista de archivos protegidos en el control de código fuente junto con la información de versión de cada archivo. Almacena un subconjunto de esta información en los archivos. pdb generados al compilar la aplicación. El script usa uno de los siguientes módulos Perl para interactuar con el control de código fuente: P4.pm (Perforce) o Vss.pm (visual Source Safe). Para obtener más información, ejecute el script con el comando-? o-?? opción (ayuda detallada) o examine el script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Esta utilidad enumera todos los archivos indizados dentro de un archivo. pdb. Para cada archivo, se muestra la ruta de acceso completa, el servidor de control de código fuente y el número de versión del archivo. Puede usar esta información para recuperar archivos sin usar el servidor de origen. Para obtener más información, ejecute la utilidad con el .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Esta utilidad la usan los scripts de indización para insertar la información de control de versiones en la secuencia alternativa "srcsrv" del archivo. pdb de destino. También puede leer cualquier flujo de un archivo. pdb. Puede usar esta información para comprobar que los scripts de indización funcionan correctamente. Para obtener más información, ejecute la utilidad con el .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Recuperando el archivo de código fuente

La API de DbgHelp proporciona acceso a la funcionalidad del servidor de origen a través de la función [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) . Para recuperar el nombre del archivo de código fuente que se va a recuperar, llame a la función [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) o [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .

## <a name="using-source-server-with-a-debugger"></a>Usar el servidor de origen con un depurador

Para usar el servidor de origen con WinDbg, KD, NTSD o CDB, asegúrese de que ha instalado una versión reciente del paquete de herramientas de depuración para Windows (versión 6,3 o posterior). A continuación, incluya SRV \* en el comando. SRCPATH de la siguiente manera:

**\. SRCPATH SRV \* ;** _c: \\ origen_

Tenga en cuenta que en este ejemplo también se incluye una ruta de acceso de origen tradicional. Si el depurador no puede recuperar el archivo del servidor de origen, buscará en la ruta de acceso especificada.

Si el servidor de origen recupera un archivo de origen, permanecerá en el disco duro una vez que la sesión de depuración haya finalizado. Los archivos de origen se almacenan localmente en el subdirectorio src del directorio de instalación de las herramientas de depuración para Windows.

## <a name="source-server-data-blocks"></a>Bloques de datos del servidor de origen

El servidor de origen se basa en dos bloques de datos dentro del archivo PDB.

-   Lista de archivos de origen. Al compilar un módulo, se crea automáticamente una lista de rutas de acceso completas a los archivos de código fuente que se usan para compilar el módulo.
-   Bloque de datos. La indización del origen tal y como se ha descrito anteriormente agrega una secuencia alternativa al archivo PDB denominado "srcsrv". El script que inserta estos datos depende del proceso de compilación específico y del sistema de control de código fuente en uso.

En la especificación de lenguaje versión 1, el bloque de datos se divide en tres secciones: ini, variables y archivos de código fuente. Tiene la siguiente sintaxis.

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

Todo el texto se interpreta literalmente, excepto en el caso de texto entre signos de porcentaje (%). El texto incluido entre signos de porcentaje se trata como un nombre de variable que se va a resolver de forma recursiva, a menos que sea una de las siguientes funciones:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

El texto del parámetro debe ir entre signos de porcentaje y tratarse como una variable que se va a expandir.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Todas las barras diagonales (/) del texto del parámetro deben reemplazarse por barras diagonales inversas ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Toda la información de ruta de acceso del texto del parámetro debe quitarse, lo que deja solo el nombre de archivo.

</dd> </dl>

La sección ini contiene variables que describen los requisitos. El script de indexación puede agregar cualquier número de variables a esta sección. A continuación, se muestran algunos ejemplos:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Versión
</dt> <dd>

Versión de la especificación de lenguaje. Esta variable es necesaria.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Cadena que describe el producto de control de código fuente. Esta variable es opcional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>DATETIME
</dt> <dd>

Cadena que indica la fecha y hora en que se procesó el archivo PDB. Esta variable es opcional.

</dd> </dl>

La sección variables contiene variables que describen cómo extraer un archivo desde el control de código fuente. También se puede usar para definir texto de uso frecuente como variables para reducir el tamaño del bloque de datos.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Describe cómo crear la ruta de acceso de destino para el archivo extraído. Esta es una variable obligatoria.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Describe cómo compilar el comando para extraer el archivo del control de código fuente. Esto incluye el nombre del archivo ejecutable y sus parámetros de la línea de comandos. Esta es una variable obligatoria.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Cadena que muestra las variables de entorno que se van a crear durante la extracción del archivo. Separe varias entradas con un carácter de retroceso ( \\ b). Esta es una variable opcional.

</dd> </dl>

La sección archivos de código fuente contiene una entrada para cada archivo de código fuente que se ha indexado. El contenido de cada línea se interpreta como variables con los nombres VAR1, VAR2, VAR3 y así sucesivamente hasta VAR10. Las variables se separan mediante asteriscos. VAR1 debe especificar la ruta de acceso completa al archivo de código fuente, tal y como se muestra en otro lugar del archivo PDB. Por ejemplo, la siguiente línea:

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

En este ejemplo, VAR4 es un número de versión. Sin embargo, la mayoría de los sistemas de control de código fuente admiten la etiqueta de archivos de forma que se pueda restaurar el estado de origen de una compilación determinada. Por lo tanto, podría usar la etiqueta para la compilación de forma alternativa. El bloque de datos de ejemplo se puede modificar para que contenga una variable como la siguiente:

``` syntax
LABEL=BUILD47
```

A continuación, suponiendo que el sistema de control de código fuente usa el signo de arroba (@) para indicar una etiqueta, puede modificar la variable SRCSRVCMD como se indica a continuación:

**sd.exe-p% fnvar%(% Var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% etiqueta%**

## <a name="how-source-server-works"></a>Cómo funciona el servidor de origen

El cliente del servidor de origen se implementa en Symsrv.dll. El cliente no extrae información directamente del archivo PDB; utiliza un controlador de símbolos como el que se implementa en Dbghelp.dll. Es esencialmente un motor de sustitución de variables recursivo que crea una línea de comandos que se puede usar para extraer el archivo de código fuente adecuado del sistema de control de código fuente. El código no debe llamar a Symsrv.dll directamente. Para integrar su funcionalidad en la aplicación, utilice la función [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .

La primera versión del servidor de origen funciona de la siguiente manera. Este comportamiento puede cambiar en versiones futuras.

-   El cliente llama a la función **SrcSrvInit** con la ruta de acceso de destino que se va a usar como base para todas las extracciones de archivo de origen. Almacena esta ruta de acceso en la variable ex.
-   El cliente extrae el flujo srcsrv del archivo PDB cuando se carga el archivo PDB del módulo y llama a la función **SrcSrvLoadModule** para pasar el bloque de datos al servidor de origen.
-   Cuando DbgHelp recupera un archivo de código fuente, el cliente llama a la función **SrcSrvGetFile** para recuperar los archivos de código fuente del control de código fuente.
-   El servidor de origen busca en las entradas del archivo de origen del bloque de datos una entrada que coincida con el archivo solicitado. Rellena *Var1 con el* contenido de la entrada del archivo de origen. A continuación, expande la variable SRCSRVTRG con VAR1 a VAR *n*. Si el archivo ya está en esta ubicación, devuelve la ubicación al autor de la llamada. De lo contrario, expande la variable SRCSRVCMD para compilar el comando necesario para recuperar el archivo del control de código fuente y copiarlo en la ubicación de destino. Por último, ejecuta este comando.

## <a name="creating-a-source-control-provider-module"></a>Crear un módulo de proveedor de control de código fuente

El servidor de origen incluye módulos de proveedor para Perforce (p4.pm) y visual Source Safe (vss.pm). Para crear su propio módulo de proveedor, debe implementar el siguiente conjunto de interfaces.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**
</dt> <dd>

Propósito: muestra información de uso del módulo simple en STDOUT.

Parámetros: None

Valor devuelto: ninguno

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**
</dt> <dd>

Propósito: muestra información detallada sobre el uso del módulo en STDOUT.

Parámetros: None

Valor devuelto: ninguno

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: New ( \@ CommandArguments)**
</dt> <dd>

Propósito: Inicializa una instancia del módulo de proveedor.

Parámetros: todos los @ARGV argumentos que SSIndex. cmd no reconoció como argumentos generales.

Valor devuelto: una referencia que se puede utilizar en operaciones posteriores.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref >GatherFileInformation ($SourcePath, $ServerHashReference)**
</dt> <dd>

Propósito: permite que el módulo recopile la información de indización de origen necesaria para el directorio especificado por el parámetro $SourcePath. El módulo no debe asumir que se llamará a esta entrada una sola vez para cada instancia de objeto, ya que SSIndex. cmd puede llamarla varias veces para diferentes rutas de acceso.

Parámetros: (1) el directorio local que contiene el origen que se va a indizar. (2) referencia a un hash que contiene todas las entradas del archivo de Srcsrv.ini especificado.

Valor devuelto: ninguno

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**
</dt> <dd>

Propósito: proporciona la información necesaria para extraer un solo archivo específico del sistema de control de código fuente.

Parámetros: un nombre de archivo completo

Valor devuelto: (1) referencia hash de las variables necesarias para interpretar el $FileEntry devuelto. SSIndex. cmd almacena en caché estas variables para cada archivo de código fuente utilizado por un solo archivo de depuración para reducir la cantidad de información que se escribe en el flujo de índice de origen. (2) la entrada de archivo que se va a escribir en el flujo de índice de origen para permitir que SrcSrv.dll Extraiga este archivo desde el control de código fuente. El formato exacto de esta línea es específico del sistema de control de código fuente.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**
</dt> <dd>

Propósito: proporciona una cadena descriptiva para identificar el proveedor de control de código fuente para el usuario final.

Parámetros: None

Valor devuelto: el nombre descriptivo del sistema de control de código fuente.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**
</dt> <dd>

Propósito: permite al proveedor de control de código fuente agregar variables específicas del control de código fuente a la secuencia de origen para cada archivo de depuración. Los módulos de ejemplo usan este método para escribir las variables de destino EXTRACT de extracción \_ y extracción \_ .

Parámetros: None

Valor devuelto: la lista de entradas de las variables de flujo de origen.

</dd> </dl>

 

 




