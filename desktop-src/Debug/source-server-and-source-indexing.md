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
# <a name="source-server"></a><span data-ttu-id="9a8b9-103">Servidor de origen</span><span class="sxs-lookup"><span data-stu-id="9a8b9-103">Source Server</span></span>

<span data-ttu-id="9a8b9-104">El servidor de origen permite a un cliente recuperar la versión exacta de los archivos de origen que se usaron para compilar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="9a8b9-105">Dado que el código fuente de un módulo puede cambiar entre versiones y a lo largo de un año, es importante examinar el código fuente tal como existía cuando se compiló la versión del módulo en cuestión.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="9a8b9-106">El servidor de origen recupera los archivos correspondientes del control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="9a8b9-107">Para usar el servidor de origen, la aplicación debe haber sido indizada por el origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="9a8b9-108">Indexación de origen</span><span class="sxs-lookup"><span data-stu-id="9a8b9-108">Source Indexing</span></span>

<span data-ttu-id="9a8b9-109">El sistema de indexación de origen es una colección de archivos ejecutables y scripts Perl.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="9a8b9-110">Los scripts Perl requieren Perl 5,6 o superior.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="9a8b9-111">Por lo general, los archivos binarios se indizan en el origen durante el proceso de compilación una vez que se ha compilado la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="9a8b9-112">La información que necesita el servidor de origen se almacena en los archivos PDB.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="9a8b9-113">El servidor de origen se distribuye actualmente con scripts que deben funcionar con los siguientes sistemas de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="9a8b9-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="9a8b9-114">Team Foundation Server</span></span>
-   <span data-ttu-id="9a8b9-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="9a8b9-115">Perforce</span></span>
-   <span data-ttu-id="9a8b9-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="9a8b9-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="9a8b9-117">CSV</span><span class="sxs-lookup"><span data-stu-id="9a8b9-117">CVS</span></span>
-   <span data-ttu-id="9a8b9-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="9a8b9-118">Subversion</span></span>

<span data-ttu-id="9a8b9-119">También puede crear un script personalizado para indizar el código para un sistema de control de código fuente diferente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="9a8b9-120">En la tabla siguiente se enumeran las herramientas de servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="9a8b9-121">Herramienta</span><span class="sxs-lookup"><span data-stu-id="9a8b9-121">Tool</span></span>        | <span data-ttu-id="9a8b9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a8b9-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8b9-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="9a8b9-123">Srcsrv.ini</span></span>  | <span data-ttu-id="9a8b9-124">Este archivo es la lista maestra de todos los servidores de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="9a8b9-125">Cada entrada tiene el siguiente *formato:* = *ServerInfo*</span><span class="sxs-lookup"><span data-stu-id="9a8b9-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="9a8b9-126">Al usar Perforce, la información del servidor se compone de la ruta de acceso de red completa al servidor, seguida de dos puntos, seguido del número de puerto que usa.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="9a8b9-127">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-127">For example:</span></span><br/> <span data-ttu-id="9a8b9-128">MiEquipo = Machine. Corp. Company. com: 1666</span><span class="sxs-lookup"><span data-stu-id="9a8b9-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="9a8b9-129">Este archivo se puede instalar en el equipo que ejecuta el depurador.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="9a8b9-130">Cuando se inicia el servidor de origen, examina Srcsrv.ini para los valores; Estos valores reemplazarán la información contenida en el archivo PDB.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="9a8b9-131">Esto permite a los usuarios configurar un depurador para utilizar un servidor de control de código fuente alternativo en tiempo de depuración.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="9a8b9-132">Para obtener más información, vea el ejemplo Srcsrv.ini instalado con las herramientas del servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="9a8b9-133">Ssindex. cmd</span><span class="sxs-lookup"><span data-stu-id="9a8b9-133">Ssindex.cmd</span></span> | <span data-ttu-id="9a8b9-134">Este script crea la lista de archivos protegidos en el control de código fuente junto con la información de versión de cada archivo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="9a8b9-135">Almacena un subconjunto de esta información en los archivos. pdb generados al compilar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="9a8b9-136">El script usa uno de los siguientes módulos Perl para interactuar con el control de código fuente: P4.pm (Perforce) o Vss.pm (visual Source Safe). Para obtener más información, ejecute el script con el comando-?</span><span class="sxs-lookup"><span data-stu-id="9a8b9-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="9a8b9-137">o-??</span><span class="sxs-lookup"><span data-stu-id="9a8b9-137">or -??</span></span> <span data-ttu-id="9a8b9-138">opción (ayuda detallada) o examine el script.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9a8b9-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="9a8b9-139">Srctool.exe</span></span> | <span data-ttu-id="9a8b9-140">Esta utilidad enumera todos los archivos indizados dentro de un archivo. pdb.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="9a8b9-141">Para cada archivo, se muestra la ruta de acceso completa, el servidor de control de código fuente y el número de versión del archivo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="9a8b9-142">Puede usar esta información para recuperar archivos sin usar el servidor de origen. Para obtener más información, ejecute la utilidad con el</span><span class="sxs-lookup"><span data-stu-id="9a8b9-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="9a8b9-143">.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9a8b9-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="9a8b9-144">Pdbstr.exe</span></span>  | <span data-ttu-id="9a8b9-145">Esta utilidad la usan los scripts de indización para insertar la información de control de versiones en la secuencia alternativa "srcsrv" del archivo. pdb de destino.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="9a8b9-146">También puede leer cualquier flujo de un archivo. pdb.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="9a8b9-147">Puede usar esta información para comprobar que los scripts de indización funcionan correctamente. Para obtener más información, ejecute la utilidad con el</span><span class="sxs-lookup"><span data-stu-id="9a8b9-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="9a8b9-148">.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="9a8b9-149">Recuperando el archivo de código fuente</span><span class="sxs-lookup"><span data-stu-id="9a8b9-149">Retrieving the Source File</span></span>

<span data-ttu-id="9a8b9-150">La API de DbgHelp proporciona acceso a la funcionalidad del servidor de origen a través de la función [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="9a8b9-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="9a8b9-151">Para recuperar el nombre del archivo de código fuente que se va a recuperar, llame a la función [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) o [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .</span><span class="sxs-lookup"><span data-stu-id="9a8b9-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="9a8b9-152">Usar el servidor de origen con un depurador</span><span class="sxs-lookup"><span data-stu-id="9a8b9-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="9a8b9-153">Para usar el servidor de origen con WinDbg, KD, NTSD o CDB, asegúrese de que ha instalado una versión reciente del paquete de herramientas de depuración para Windows (versión 6,3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="9a8b9-154">A continuación, incluya SRV \* en el comando. SRCPATH de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="9a8b9-155">**\. SRCPATH SRV \* ;** _c: \\ origen_</span><span class="sxs-lookup"><span data-stu-id="9a8b9-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="9a8b9-156">Tenga en cuenta que en este ejemplo también se incluye una ruta de acceso de origen tradicional.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="9a8b9-157">Si el depurador no puede recuperar el archivo del servidor de origen, buscará en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="9a8b9-158">Si el servidor de origen recupera un archivo de origen, permanecerá en el disco duro una vez que la sesión de depuración haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="9a8b9-159">Los archivos de origen se almacenan localmente en el subdirectorio src del directorio de instalación de las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="9a8b9-160">Bloques de datos del servidor de origen</span><span class="sxs-lookup"><span data-stu-id="9a8b9-160">Source Server Data Blocks</span></span>

<span data-ttu-id="9a8b9-161">El servidor de origen se basa en dos bloques de datos dentro del archivo PDB.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="9a8b9-162">Lista de archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-162">Source file list.</span></span> <span data-ttu-id="9a8b9-163">Al compilar un módulo, se crea automáticamente una lista de rutas de acceso completas a los archivos de código fuente que se usan para compilar el módulo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="9a8b9-164">Bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-164">Data block.</span></span> <span data-ttu-id="9a8b9-165">La indización del origen tal y como se ha descrito anteriormente agrega una secuencia alternativa al archivo PDB denominado "srcsrv".</span><span class="sxs-lookup"><span data-stu-id="9a8b9-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="9a8b9-166">El script que inserta estos datos depende del proceso de compilación específico y del sistema de control de código fuente en uso.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="9a8b9-167">En la especificación de lenguaje versión 1, el bloque de datos se divide en tres secciones: ini, variables y archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="9a8b9-168">Tiene la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-168">It has the following syntax.</span></span>

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

<span data-ttu-id="9a8b9-169">Todo el texto se interpreta literalmente, excepto en el caso de texto entre signos de porcentaje (%).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="9a8b9-170">El texto incluido entre signos de porcentaje se trata como un nombre de variable que se va a resolver de forma recursiva, a menos que sea una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="9a8b9-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span><span class="sxs-lookup"><span data-stu-id="9a8b9-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-172">El texto del parámetro debe ir entre signos de porcentaje y tratarse como una variable que se va a expandir.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span><span class="sxs-lookup"><span data-stu-id="9a8b9-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-174">Todas las barras diagonales (/) del texto del parámetro deben reemplazarse por barras diagonales inversas ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span><span class="sxs-lookup"><span data-stu-id="9a8b9-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-176">Toda la información de ruta de acceso del texto del parámetro debe quitarse, lo que deja solo el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="9a8b9-177">La sección ini contiene variables que describen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="9a8b9-178">El script de indexación puede agregar cualquier número de variables a esta sección.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="9a8b9-179">A continuación, se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="9a8b9-180"><span id="VERSION"></span><span id="version"></span>Versión</span><span class="sxs-lookup"><span data-stu-id="9a8b9-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-181">Versión de la especificación de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-181">The language specification version.</span></span> <span data-ttu-id="9a8b9-182">Esta variable es necesaria.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span><span class="sxs-lookup"><span data-stu-id="9a8b9-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-184">Cadena que describe el producto de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-184">A string that describes the source control product.</span></span> <span data-ttu-id="9a8b9-185">Esta variable es opcional.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span><span class="sxs-lookup"><span data-stu-id="9a8b9-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-187">Cadena que indica la fecha y hora en que se procesó el archivo PDB.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="9a8b9-188">Esta variable es opcional.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="9a8b9-189">La sección variables contiene variables que describen cómo extraer un archivo desde el control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="9a8b9-190">También se puede usar para definir texto de uso frecuente como variables para reducir el tamaño del bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="9a8b9-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span><span class="sxs-lookup"><span data-stu-id="9a8b9-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-192">Describe cómo crear la ruta de acceso de destino para el archivo extraído.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="9a8b9-193">Esta es una variable obligatoria.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span><span class="sxs-lookup"><span data-stu-id="9a8b9-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-195">Describe cómo compilar el comando para extraer el archivo del control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="9a8b9-196">Esto incluye el nombre del archivo ejecutable y sus parámetros de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="9a8b9-197">Esta es una variable obligatoria.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span><span class="sxs-lookup"><span data-stu-id="9a8b9-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-199">Cadena que muestra las variables de entorno que se van a crear durante la extracción del archivo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="9a8b9-200">Separe varias entradas con un carácter de retroceso ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="9a8b9-201">Esta es una variable opcional.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="9a8b9-202">La sección archivos de código fuente contiene una entrada para cada archivo de código fuente que se ha indexado.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="9a8b9-203">El contenido de cada línea se interpreta como variables con los nombres VAR1, VAR2, VAR3 y así sucesivamente hasta VAR10.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="9a8b9-204">Las variables se separan mediante asteriscos.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="9a8b9-205">VAR1 debe especificar la ruta de acceso completa al archivo de código fuente, tal y como se muestra en otro lugar del archivo PDB.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="9a8b9-206">Por ejemplo, la siguiente línea:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="9a8b9-207">se interpreta de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="9a8b9-208">En este ejemplo, VAR4 es un número de versión.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="9a8b9-209">Sin embargo, la mayoría de los sistemas de control de código fuente admiten la etiqueta de archivos de forma que se pueda restaurar el estado de origen de una compilación determinada.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="9a8b9-210">Por lo tanto, podría usar la etiqueta para la compilación de forma alternativa.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="9a8b9-211">El bloque de datos de ejemplo se puede modificar para que contenga una variable como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="9a8b9-212">A continuación, suponiendo que el sistema de control de código fuente usa el signo de arroba (@) para indicar una etiqueta, puede modificar la variable SRCSRVCMD como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="9a8b9-213">**sd.exe-p% fnvar%(% Var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% etiqueta%**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="9a8b9-214">Cómo funciona el servidor de origen</span><span class="sxs-lookup"><span data-stu-id="9a8b9-214">How Source Server Works</span></span>

<span data-ttu-id="9a8b9-215">El cliente del servidor de origen se implementa en Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="9a8b9-216">El cliente no extrae información directamente del archivo PDB; utiliza un controlador de símbolos como el que se implementa en Dbghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="9a8b9-217">Es esencialmente un motor de sustitución de variables recursivo que crea una línea de comandos que se puede usar para extraer el archivo de código fuente adecuado del sistema de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="9a8b9-218">El código no debe llamar a Symsrv.dll directamente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="9a8b9-219">Para integrar su funcionalidad en la aplicación, utilice la función [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="9a8b9-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="9a8b9-220">La primera versión del servidor de origen funciona de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-220">The first version of source server works as follows.</span></span> <span data-ttu-id="9a8b9-221">Este comportamiento puede cambiar en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="9a8b9-222">El cliente llama a la función **SrcSrvInit** con la ruta de acceso de destino que se va a usar como base para todas las extracciones de archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="9a8b9-223">Almacena esta ruta de acceso en la variable ex.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="9a8b9-224">El cliente extrae el flujo srcsrv del archivo PDB cuando se carga el archivo PDB del módulo y llama a la función **SrcSrvLoadModule** para pasar el bloque de datos al servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="9a8b9-225">Cuando DbgHelp recupera un archivo de código fuente, el cliente llama a la función **SrcSrvGetFile** para recuperar los archivos de código fuente del control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="9a8b9-226">El servidor de origen busca en las entradas del archivo de origen del bloque de datos una entrada que coincida con el archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="9a8b9-227">Rellena *Var1 con el* contenido de la entrada del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="9a8b9-228">A continuación, expande la variable SRCSRVTRG con VAR1 a VAR *n*.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="9a8b9-229">Si el archivo ya está en esta ubicación, devuelve la ubicación al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="9a8b9-230">De lo contrario, expande la variable SRCSRVCMD para compilar el comando necesario para recuperar el archivo del control de código fuente y copiarlo en la ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="9a8b9-231">Por último, ejecuta este comando.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="9a8b9-232">Crear un módulo de proveedor de control de código fuente</span><span class="sxs-lookup"><span data-stu-id="9a8b9-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="9a8b9-233">El servidor de origen incluye módulos de proveedor para Perforce (p4.pm) y visual Source Safe (vss.pm).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="9a8b9-234">Para crear su propio módulo de proveedor, debe implementar el siguiente conjunto de interfaces.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="9a8b9-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-236">Propósito: muestra información de uso del módulo simple en STDOUT.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="9a8b9-237">Parámetros: None</span><span class="sxs-lookup"><span data-stu-id="9a8b9-237">Parameters: None</span></span>

<span data-ttu-id="9a8b9-238">Valor devuelto: ninguno</span><span class="sxs-lookup"><span data-stu-id="9a8b9-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-240">Propósito: muestra información detallada sobre el uso del módulo en STDOUT.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="9a8b9-241">Parámetros: None</span><span class="sxs-lookup"><span data-stu-id="9a8b9-241">Parameters: None</span></span>

<span data-ttu-id="9a8b9-242">Valor devuelto: ninguno</span><span class="sxs-lookup"><span data-stu-id="9a8b9-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: New ( \@ CommandArguments)**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-244">Propósito: Inicializa una instancia del módulo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="9a8b9-245">Parámetros: todos los @ARGV argumentos que SSIndex. cmd no reconoció como argumentos generales.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="9a8b9-246">Valor devuelto: una referencia que se puede utilizar en operaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref >GatherFileInformation ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-248">Propósito: permite que el módulo recopile la información de indización de origen necesaria para el directorio especificado por el parámetro $SourcePath.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="9a8b9-249">El módulo no debe asumir que se llamará a esta entrada una sola vez para cada instancia de objeto, ya que SSIndex. cmd puede llamarla varias veces para diferentes rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="9a8b9-250">Parámetros: (1) el directorio local que contiene el origen que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="9a8b9-251">(2) referencia a un hash que contiene todas las entradas del archivo de Srcsrv.ini especificado.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="9a8b9-252">Valor devuelto: ninguno</span><span class="sxs-lookup"><span data-stu-id="9a8b9-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-254">Propósito: proporciona la información necesaria para extraer un solo archivo específico del sistema de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="9a8b9-255">Parámetros: un nombre de archivo completo</span><span class="sxs-lookup"><span data-stu-id="9a8b9-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="9a8b9-256">Valor devuelto: (1) referencia hash de las variables necesarias para interpretar el $FileEntry devuelto.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="9a8b9-257">SSIndex. cmd almacena en caché estas variables para cada archivo de código fuente utilizado por un solo archivo de depuración para reducir la cantidad de información que se escribe en el flujo de índice de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="9a8b9-258">(2) la entrada de archivo que se va a escribir en el flujo de índice de origen para permitir que SrcSrv.dll Extraiga este archivo desde el control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="9a8b9-259">El formato exacto de esta línea es específico del sistema de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-261">Propósito: proporciona una cadena descriptiva para identificar el proveedor de control de código fuente para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="9a8b9-262">Parámetros: None</span><span class="sxs-lookup"><span data-stu-id="9a8b9-262">Parameters: None</span></span>

<span data-ttu-id="9a8b9-263">Valor devuelto: el nombre descriptivo del sistema de control de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="9a8b9-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="9a8b9-265">Propósito: permite al proveedor de control de código fuente agregar variables específicas del control de código fuente a la secuencia de origen para cada archivo de depuración.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="9a8b9-266">Los módulos de ejemplo usan este método para escribir las variables de destino EXTRACT de extracción \_ y extracción \_ .</span><span class="sxs-lookup"><span data-stu-id="9a8b9-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="9a8b9-267">Parámetros: None</span><span class="sxs-lookup"><span data-stu-id="9a8b9-267">Parameters: None</span></span>

<span data-ttu-id="9a8b9-268">Valor devuelto: la lista de entradas de las variables de flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




