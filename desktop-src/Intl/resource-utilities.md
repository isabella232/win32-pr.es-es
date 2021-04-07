---
description: En este tema se describen dos utilidades que se usan para crear aplicaciones de MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilidades de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002568"
---
# <a name="resource-utilities"></a><span data-ttu-id="e0972-103">Utilidades de recursos</span><span class="sxs-lookup"><span data-stu-id="e0972-103">Resource Utilities</span></span>

<span data-ttu-id="e0972-104">En este tema se describen dos utilidades que se usan para crear aplicaciones de MUI.</span><span class="sxs-lookup"><span data-stu-id="e0972-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="e0972-105">Aunque MUIRCT es una herramienta específica de MUI, MUI también usa la utilidad del compilador estándar de Windows RC.</span><span class="sxs-lookup"><span data-stu-id="e0972-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="e0972-106">Se proporcionan instrucciones para el uso de estas utilidades en [localizar recursos y compilar la aplicación](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="e0972-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="e0972-107">Utilidad MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-107">MUIRCT Utility</span></span>

<span data-ttu-id="e0972-108">MUIRCT (Muirct.exe) es una utilidad de línea de comandos para dividir un archivo ejecutable estándar en un archivo LN y archivos de recursos específicos del lenguaje (es decir, localizables).</span><span class="sxs-lookup"><span data-stu-id="e0972-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="e0972-109">Cada uno de los archivos resultantes contiene datos de configuración de recursos para la Asociación de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0972-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="e0972-110">MUIRCT se incluye en el Microsoft Windows SDK para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0972-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="e0972-111">A partir de Windows Vista, el cargador de recursos de Win32 se actualiza para cargar recursos desde archivos específicos del idioma, así como desde archivos LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="e0972-112">Usos de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="e0972-113">Divida el binario en el archivo binario principal y mui basado en el \_ archivo de configuración RC.</span><span class="sxs-lookup"><span data-stu-id="e0972-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="e0972-114">Extrae la suma de comprobación del archivo de suma de comprobación \_ e insértela en el archivo de salida \_ .</span><span class="sxs-lookup"><span data-stu-id="e0972-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="e0972-115">Calcula la suma de comprobación basada en el archivo de suma de comprobación \_ e insértela en el archivo de salida \_ .</span><span class="sxs-lookup"><span data-stu-id="e0972-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="e0972-116">Vuelca el contenido de datos de configuración de recursos del archivo de entrada \_ .</span><span class="sxs-lookup"><span data-stu-id="e0972-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="e0972-117">Sintaxis de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-117">MUIRCT Syntax</span></span>

<span data-ttu-id="e0972-118">MUIRCT puede tomar la dirección de los modificadores de línea de comandos y/o de un archivo de configuración de recursos, especificado mediante el modificador-q.</span><span class="sxs-lookup"><span data-stu-id="e0972-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="e0972-119">**Modificadores y argumentos**</span><span class="sxs-lookup"><span data-stu-id="e0972-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0972-120">-h |-?</span><span class="sxs-lookup"><span data-stu-id="e0972-120">-h|-?</span></span></td>
<td><span data-ttu-id="e0972-121">Muestra la pantalla de ayuda.</span><span class="sxs-lookup"><span data-stu-id="e0972-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-122">-c</span><span class="sxs-lookup"><span data-stu-id="e0972-122">-c</span></span></td>
<td><span data-ttu-id="e0972-123">Especifica la checksum_file de entrada de la que se va a extraer o calcular la suma de comprobación de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="e0972-124">Checksum_file debe ser un archivo binario de Win32 que contenga recursos localizables.</span><span class="sxs-lookup"><span data-stu-id="e0972-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="e0972-125">Si checksum_file contiene recursos para más de un idioma, se debe usar el modificador-b para especificar cuáles de ellos se deben usar; de lo contrario, se producirá un error MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="e0972-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-126">-b</span><span class="sxs-lookup"><span data-stu-id="e0972-126">-b</span></span></td>
<td><span data-ttu-id="e0972-127">Especifica el idioma que se usará cuando el checksum_file especificado con-c contenga recursos en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="e0972-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="e0972-128">Este modificador solo se puede usar junto con el modificador-c.</span><span class="sxs-lookup"><span data-stu-id="e0972-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="e0972-129">El identificador de idioma puede estar en formato decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e0972-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="e0972-130">MUIRCT produce un error si el checksum_file contiene recursos en varios idiomas y no se especifica-b o si no se encuentra el idioma especificado por el modificador-b en el checksum_file.</span><span class="sxs-lookup"><span data-stu-id="e0972-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-131">-g</span><span class="sxs-lookup"><span data-stu-id="e0972-131">-g</span></span></td>
<td><span data-ttu-id="e0972-132">Especifica el identificador de idioma que se va a incluir como idioma de reserva final en la sección de datos de configuración de recursos del archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="e0972-133">Si el cargador de recursos no puede cargar un archivo. mui solicitado de los idiomas de interfaz de usuario preferidos del subproceso, utiliza el idioma de reserva final como último intento.</span><span class="sxs-lookup"><span data-stu-id="e0972-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="e0972-134">El valor LangID se puede especificar en formato decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e0972-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="e0972-135">Por ejemplo, el inglés (Estados Unidos) puede especificarse mediante-g 0xC0A o-g 1033.</span><span class="sxs-lookup"><span data-stu-id="e0972-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-136">-q</span><span class="sxs-lookup"><span data-stu-id="e0972-136">-q</span></span></td>
<td><span data-ttu-id="e0972-137">Especifica que el source_file se va a dividir en el output_LN_file y el output_MUI_file según el diseño del archivo de rc_config.</span><span class="sxs-lookup"><span data-stu-id="e0972-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="e0972-138">El archivo rc_config es un archivo con formato XML que especifica los recursos que se extraerán en el archivo. mui y que se dejarán en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="e0972-139">El rc_config puede especificar la distribución de tipos de recursos y elementos individuales con nombre entre el output_LN_file y el output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="e0972-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="e0972-140">El source_file debe ser un archivo binario de Win32 que contenga recursos en un solo lenguaje; de lo contrario, MUIRCT producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e0972-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="e0972-141">MUIRCT no divide el archivo si es independiente del idioma, lo que se indica con el valor 0 de identificador de idioma en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e0972-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="e0972-142">Los output_LN_file y output_mui_file son los nombres del archivo neutro y. MUI en el que se divide el source_file.</span><span class="sxs-lookup"><span data-stu-id="e0972-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="e0972-143">Estos nombres de archivo son opcionales.</span><span class="sxs-lookup"><span data-stu-id="e0972-143">These file names are optional.</span></span> <span data-ttu-id="e0972-144">Si no se especifican, MUIRCT anexa las extensiones. LN y. mui a source_file.</span><span class="sxs-lookup"><span data-stu-id="e0972-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="e0972-145">Normalmente, debe quitar la &quot; extensión. LN &quot; antes de implementar el archivo.</span><span class="sxs-lookup"><span data-stu-id="e0972-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="e0972-146">MUIRCT asocia el output_LN_file y output_MUI_file calculando una suma de comprobación basada en el nombre de la source_file y la versión del archivo e insertando el resultado en la sección de configuración de recursos de cada archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="e0972-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="e0972-147">Cuando se usa junto con el modificador-c, el modificador-q tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="e0972-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="e0972-148">Si el archivo de rc_config proporcionado con el modificador-q contiene una suma de comprobación MUIRCT omite el modificador-c e inserta el valor de la suma de comprobación del valor, rc_config archivo en los archivos LN y. MUI.</span><span class="sxs-lookup"><span data-stu-id="e0972-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="e0972-149">Si no se encuentra ningún valor de suma de comprobación en el rc_config, MUIRCT calcula la suma de comprobación de recursos según el comportamiento del modificador-c.</span><span class="sxs-lookup"><span data-stu-id="e0972-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-150">-v</span><span class="sxs-lookup"><span data-stu-id="e0972-150">-v</span></span></td>
<td><span data-ttu-id="e0972-151">Especifica el nivel de detallados para el registro.</span><span class="sxs-lookup"><span data-stu-id="e0972-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="e0972-152">Especifique 1 para imprimir todos los mensajes de error básicos y los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="e0972-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="e0972-153">Especifique 2 para incluir también la información de recursos (tipo, nombre, identificador de idioma) incluida en el archivo. mui y en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="e0972-154">El valor predeterminado es-v 1</span><span class="sxs-lookup"><span data-stu-id="e0972-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-155">-X</span><span class="sxs-lookup"><span data-stu-id="e0972-155">-x</span></span></td>
<td><span data-ttu-id="e0972-156">Especifica el identificador de idioma con el que MUIRCT marca todos los tipos de recursos agregados a la sección de recursos del archivo. MUI.</span><span class="sxs-lookup"><span data-stu-id="e0972-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="e0972-157">El valor LangID se puede especificar en formato decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e0972-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="e0972-158">Por ejemplo, el inglés (Estados Unidos) se puede especificar mediante-x 0xC0A o-x 1033.</span><span class="sxs-lookup"><span data-stu-id="e0972-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-159">-E</span><span class="sxs-lookup"><span data-stu-id="e0972-159">-e</span></span></td>
<td><span data-ttu-id="e0972-160">Extrae la suma de comprobación de recursos contenida en el checksum_file proporcionado con el modificador-c y lo inserta en el output_file especificado.</span><span class="sxs-lookup"><span data-stu-id="e0972-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="e0972-161">Cuando se especifica-e, MUIRCT omite todos los modificadores distintos del modificador-c.</span><span class="sxs-lookup"><span data-stu-id="e0972-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="e0972-162">En este caso, el checksum_file debe ser un archivo binario de Win32 que contenga una sección de datos de configuración de recursos con un valor de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="e0972-163">El output_file debe ser un archivo LN o. mui existente.</span><span class="sxs-lookup"><span data-stu-id="e0972-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-164">-Z</span><span class="sxs-lookup"><span data-stu-id="e0972-164">-z</span></span></td>
<td><span data-ttu-id="e0972-165">Calcula e inserta los datos de la suma de comprobación de recursos en el archivo de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="e0972-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="e0972-166">MUIRCT basa el cálculo de suma de comprobación en la entrada proporcionada con el modificador-c y el modificador opcional-b.</span><span class="sxs-lookup"><span data-stu-id="e0972-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="e0972-167">Si especifica un archivo de salida para el modificador-z que no existe, MUIRCT se cierra con un error.</span><span class="sxs-lookup"><span data-stu-id="e0972-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="e0972-168">Ejemplo: calcula la suma de comprobación basada en recursos localizables de Notepad.exe e inserta la suma de comprobación en el archivo de salida Notepad2.exe.</span><span class="sxs-lookup"><span data-stu-id="e0972-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-169">-f</span><span class="sxs-lookup"><span data-stu-id="e0972-169">-f</span></span></td>
<td><span data-ttu-id="e0972-170">Permite crear un archivo. mui con el recurso de versión que es el único recurso traducible.</span><span class="sxs-lookup"><span data-stu-id="e0972-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="e0972-171">De forma predeterminada, MUIRCT no lo permite.</span><span class="sxs-lookup"><span data-stu-id="e0972-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-172">-d</span><span class="sxs-lookup"><span data-stu-id="e0972-172">-d</span></span></td>
<td><span data-ttu-id="e0972-173">Busca y muestra los datos de configuración de recursos incrustados en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="e0972-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="e0972-174">Cuando se especifica este modificador, MUIRCT omite todas las demás opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e0972-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-175">-M</span><span class="sxs-lookup"><span data-stu-id="e0972-175">-m</span></span></td>
<td><span data-ttu-id="e0972-176">Especifica el número de versión que se va a utilizar al calcular la suma de comprobación para asociar el output_LN_file y output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="e0972-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="e0972-177">source_filename</span></span></td>
<td><span data-ttu-id="e0972-178">Nombre del archivo de origen binario localizado; no se pueden usar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="e0972-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="e0972-179">Este archivo solo puede contener recursos en un idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="e0972-180">Si hay recursos en varios idiomas en el archivo, MUIRCT produce un error, a menos que se use el modificador-b.</span><span class="sxs-lookup"><span data-stu-id="e0972-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="e0972-181">Si el archivo contiene recursos con identificadores de idioma que solo tienen el valor 0, MUIRCT no divide el archivo porque un identificador de idioma de 0 indica un idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="e0972-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="e0972-182">En el caso del modificador-d, source_filename es un archivo LN o un archivo de recursos específico del lenguaje para el que MUIRCT va a mostrar los datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="e0972-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="e0972-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e0972-184">Optional.</span></span> <span data-ttu-id="e0972-185">Nombre del archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-185">Name of LN file.</span></span> <span data-ttu-id="e0972-186">Si no especifica el nombre de este archivo, MUIRCT anexa una segunda extensión &quot; . LN &quot; al nombre del archivo de código fuente que se va a usar como nombre de archivo independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="e0972-187">Normalmente, debe quitar la &quot; extensión. LN &quot; antes de implementar el archivo.</span><span class="sxs-lookup"><span data-stu-id="e0972-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0972-188">El archivo LN no debe contener cadenas ni menús.</span><span class="sxs-lookup"><span data-stu-id="e0972-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="e0972-189">Debe quitarlas manualmente.</span><span class="sxs-lookup"><span data-stu-id="e0972-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="e0972-190">mui_filename</span></span></td>
<td><span data-ttu-id="e0972-191">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e0972-191">Optional.</span></span> <span data-ttu-id="e0972-192">Nombre del archivo de recursos específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-192">Name of language-specific resource file.</span></span> <span data-ttu-id="e0972-193">Si no especifica un nombre, MUIRCT anexa una segunda extensión &quot; . mui &quot; al nombre del archivo de código fuente que se va a usar como nombre de archivo. Normalmente, MUIRCT crea un archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e0972-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="e0972-194">Sin embargo, no crea un archivo de recursos si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0972-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="e0972-195">No hay recursos localizables en el archivo binario original.</span><span class="sxs-lookup"><span data-stu-id="e0972-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="e0972-196">El único lenguaje de recursos que se encuentra en el archivo binario original es el idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="e0972-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="e0972-197">El archivo binario original tiene recursos para más de un idioma, sin contar el idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="e0972-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="e0972-198">Si el archivo binario contiene recursos para dos idiomas y uno de ellos es el idioma neutro, la utilidad considera que el archivo es Monolingual y crea un archivo de recursos específico del idioma si hay recursos localizables.</span><span class="sxs-lookup"><span data-stu-id="e0972-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="e0972-199">Salida del lenguaje MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-199">MUIRCT Language Output</span></span>

<span data-ttu-id="e0972-200">MUIRCT elige el valor de atributo "UltimateFallbackLanguage" para insertar en los datos de configuración de recursos de archivo LN según el siguiente orden, de la prioridad más alta a la más baja:</span><span class="sxs-lookup"><span data-stu-id="e0972-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="e0972-201">Atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.</span><span class="sxs-lookup"><span data-stu-id="e0972-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="e0972-202">El idioma especificado con el modificador-g.</span><span class="sxs-lookup"><span data-stu-id="e0972-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="e0972-203">Idioma del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0972-203">Input file language.</span></span>

<span data-ttu-id="e0972-204">MUIRCT elige el valor de atributo "Language" que se va a insertar en los datos de configuración de recursos de archivos. mui según el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="e0972-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="e0972-205">atributo "Language" en el archivo de configuración de recursos de origen, si se pasa uno como entrada.</span><span class="sxs-lookup"><span data-stu-id="e0972-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="e0972-206">El idioma especificado por el modificador-x (Force Language).</span><span class="sxs-lookup"><span data-stu-id="e0972-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="e0972-207">Idioma del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0972-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="e0972-208">Control de suma de comprobación MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="e0972-209">Normalmente, el sistema operativo calcula la suma de comprobación de los recursos específicos del idioma de un archivo, a menos que se especifique la suma de comprobación a través de un archivo de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="e0972-210">Siempre que la suma de comprobación sea la misma para el archivo LN y todos los archivos de recursos específicos del idioma asociados, y el atributo de idioma en la configuración de recursos en la coincidencia con el lenguaje LN y el idioma, el cargador de recursos puede cargar los recursos correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0972-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="e0972-211">MUIRCT admite varios métodos para colocar las sumas de comprobación adecuadas en los datos de configuración de recursos:</span><span class="sxs-lookup"><span data-stu-id="e0972-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="e0972-212">Cree un archivo ejecutable para cada lenguaje que contenga código y recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="e0972-213">Después de esto, use MUIRCT para dividir cada uno de estos archivos en un archivo LN y un archivo de recursos específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="e0972-214">MUIRCT se ejecuta varias veces, una vez para generar un archivo de recursos para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="e0972-215">Puede realizar la compilación de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="e0972-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="e0972-216">Use el modificador-q para especificar un valor de suma de comprobación en el archivo de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="e0972-217">MUIRCT coloca este valor en todos los archivos LN y en los archivos de recursos específicos del idioma producidos.</span><span class="sxs-lookup"><span data-stu-id="e0972-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="e0972-218">Debe adoptar una estrategia para elegir este valor, tal y como se describe más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="e0972-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="e0972-219">Use el modificador-c (y, opcionalmente, el conmutador-b) para elegir un solo idioma con recursos a partir del cual MUIRCT extrae la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="e0972-220">Use el modificador-z para elegir un solo idioma con recursos a partir del cual MUIRCT siempre extrae la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="e0972-221">Aplique esta suma de comprobación después de que los archivos se hayan creado con otros métodos.</span><span class="sxs-lookup"><span data-stu-id="e0972-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="e0972-222">Cree un archivo ejecutable que contenga código y recursos para un solo lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e0972-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="e0972-223">Después de esto, use MUIRCT para dividir los recursos entre el archivo LN y el archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e0972-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="e0972-224">Por último, use una herramienta de localización binaria para modificar el archivo de recursos resultante para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="e0972-225">La Convención más común para el tratamiento de sumas de comprobación consiste en basar la suma de comprobación en los recursos de inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e0972-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="e0972-226">Puede adoptar una Convención diferente, siempre que sea coherente para cada archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="e0972-227">Por ejemplo, es absolutamente aceptable que una empresa de desarrollo de software base sus sumas de comprobación en el software que se basa en los recursos de francés (Francia) en lugar de los recursos en inglés (Estados Unidos), siempre que todas las aplicaciones tengan recursos en francés (Francia) en los que basar las sumas de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="e0972-228">También es aceptable usar el archivo de configuración de recursos para asignar un valor hexadecimal arbitrario de hasta 16 dígitos hexadecimales como una suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="e0972-229">Esta última estrategia impide el uso eficaz de los conmutadores-z,-c y-b de MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="e0972-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="e0972-230">Requiere la adopción de un método mediante [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) u otra herramienta para generar valores de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="e0972-231">Esta estrategia también requiere la configuración de una directiva para determinar cuándo se debe modificar el valor al agregar nuevos recursos localizables.</span><span class="sxs-lookup"><span data-stu-id="e0972-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="e0972-232">Para aplicar la suma de comprobación inglés (Estados Unidos) a todos los archivos, puede usar cualquiera de los métodos de control de suma de comprobación descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e0972-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="e0972-233">Por ejemplo, puede generar el archivo LN y el archivo de recursos específico del lenguaje para inglés (Estados Unidos) y, a continuación, usar el modificador MUIRCT-d para obtener la suma de comprobación resultante.</span><span class="sxs-lookup"><span data-stu-id="e0972-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="e0972-234">Puede copiar esta suma de comprobación en el archivo de configuración de recursos y usar el modificador-q con MUIRCT para aplicar la suma de comprobación a todos los demás archivos.</span><span class="sxs-lookup"><span data-stu-id="e0972-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="e0972-235">Uso de un archivo de configuración de recursos con MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="e0972-236">Puede especificar los datos de configuración de recursos cuando se usa MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="e0972-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="e0972-237">Tanto si proporciona explícitamente un archivo de configuración de recursos como si no, cada archivo de recursos específico del lenguaje tiene datos de configuración de recursos, al igual que cualquier archivo LN con un archivo de recursos asociado.</span><span class="sxs-lookup"><span data-stu-id="e0972-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="e0972-238">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0972-238">For example:</span></span>

-   <span data-ttu-id="e0972-239">Si usa el modificador-q para especificar un archivo de configuración de recursos, pero no hay recursos localizables en el archivo de origen de entrada, no se genera ningún archivo de recursos específico del idioma y el archivo LN resultante no contiene datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="e0972-240">Además, si el archivo de origen de entrada tiene recursos multilingües, MUIRCT no dividirá el archivo.</span><span class="sxs-lookup"><span data-stu-id="e0972-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="e0972-241">Actualmente, el comportamiento de MUIRCT es incoherente cuando el elemento neutralResources del archivo de configuración de recursos no contiene elementos resourceType y el elemento localizedResources contiene cadenas y menús, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0972-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="e0972-242">En tal caso, MUIRCT divide los recursos como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e0972-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="e0972-243">Todos los recursos del binario original (incluidas las cadenas y los menús), además de los recursos de MUI, se colocan en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="e0972-244">Las cadenas, los menús y los recursos de MUI se colocan en el archivo de recursos específico del idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="e0972-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="e0972-245">Ejemplos de uso de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="e0972-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="e0972-246">**Ejemplos de uso estándar**</span><span class="sxs-lookup"><span data-stu-id="e0972-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="e0972-247">**Ejemplo de salida de archivo LN con el modificador-d**</span><span class="sxs-lookup"><span data-stu-id="e0972-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="e0972-248">Este es un ejemplo de la salida de los datos de configuración de recursos de un archivo LN, Shell32.dll, mediante el modificador-d con MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="e0972-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="e0972-249">**Ejemplo de Language-Specific salida de archivo de recursos con el modificador-d**</span><span class="sxs-lookup"><span data-stu-id="e0972-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="e0972-250">Este es un ejemplo de la salida de datos de configuración de recursos de un archivo. MUI, Shell32.dll. MUI, con el modificador-d para MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="e0972-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="e0972-251">RC (utilidad del compilador)</span><span class="sxs-lookup"><span data-stu-id="e0972-251">RC Compiler Utility</span></span>

<span data-ttu-id="e0972-252">RC Compiler (Rc.exe) es una utilidad de línea de comandos para compilar un archivo de script de definición de recursos (extensión. RC) en archivos de recursos (extensión. res).</span><span class="sxs-lookup"><span data-stu-id="e0972-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="e0972-253">El compilador RC se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e0972-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="e0972-254">En este documento solo se explica el uso del compilador RC con capacidades relacionadas con la MUI del cargador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="e0972-255">Para obtener información completa sobre el compilador, vea [acerca de los archivos de recursos](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="e0972-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="e0972-256">El compilador RC permite crear, desde un único conjunto de orígenes, un archivo LN y un archivo de recursos independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="e0972-257">En el caso de MUIRCT, los archivos están asociados a los datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="e0972-258">RC sintaxis del compilador tal como se usa para recursos de MUI</span><span class="sxs-lookup"><span data-stu-id="e0972-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="e0972-259">Los modificadores del compilador RC se definen en detalle en [uso de RC](../menurc/using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="e0972-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="e0972-260">En esta sección solo se definen los modificadores que se usan para crear recursos de MUI.</span><span class="sxs-lookup"><span data-stu-id="e0972-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="e0972-261">Recuerde que cada modificador distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e0972-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="e0972-262">Se supone que los tipos de recursos son independientes del idioma, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e0972-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="e0972-263">**Modificadores y argumentos**</span><span class="sxs-lookup"><span data-stu-id="e0972-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0972-264">-h |-?</span><span class="sxs-lookup"><span data-stu-id="e0972-264">-h|-?</span></span></td>
<td><span data-ttu-id="e0972-265">Muestra la pantalla de ayuda.</span><span class="sxs-lookup"><span data-stu-id="e0972-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-266">-FM</span><span class="sxs-lookup"><span data-stu-id="e0972-266">-fm</span></span></td>
<td><span data-ttu-id="e0972-267">Utiliza el archivo de recursos especificado para los recursos específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="e0972-268">Normalmente, el compilador de recursos crea un archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e0972-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="e0972-269">Sin embargo, no crea el archivo si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0972-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="e0972-270">No hay recursos localizables en el archivo. rc.</span><span class="sxs-lookup"><span data-stu-id="e0972-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="e0972-271">El único idioma de los recursos que se encuentra en el archivo. RC es el idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="e0972-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="e0972-272">El archivo. rc tiene recursos para más de un idioma, sin contar el idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="e0972-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="e0972-273">Si el archivo. RC contiene recursos para dos idiomas y uno de ellos es el idioma neutro, el compilador considera que el archivo es Monolingual.</span><span class="sxs-lookup"><span data-stu-id="e0972-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="e0972-274">Si hay recursos localizables, el compilador crea un archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e0972-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-275">-q</span><span class="sxs-lookup"><span data-stu-id="e0972-275">-q</span></span></td>
<td><span data-ttu-id="e0972-276">Usa el archivo de configuración de recursos especificado para obtener los tipos de recursos que se colocarán en el archivo de recursos específico del lenguaje y en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="e0972-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="e0972-277">Para obtener más información, vea <a href="preparing-a-resource-configuration-file.md">preparar un archivo de configuración de recursos</a>.</span><span class="sxs-lookup"><span data-stu-id="e0972-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="e0972-278">Como alternativa a este modificador, puede usar los modificadores-j y-k, pero es preferible usar un archivo de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="e0972-279">Mediante el uso del modificador-q con un archivo de configuración de recursos, puede implementar una división basada en elementos y proporcionar atributos que terminarán con la configuración de recursos binarios en el archivo de recursos LN y el idioma específico.</span><span class="sxs-lookup"><span data-stu-id="e0972-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="e0972-280">Esta división no es posible mediante los modificadores-j y-k.</span><span class="sxs-lookup"><span data-stu-id="e0972-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0972-281">El proceso de división del compilador RC no funciona correctamente si se almacenan los recursos y la información de versión en distintos archivos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="e0972-282">En este caso, el compilador RC no divide la información de versión.</span><span class="sxs-lookup"><span data-stu-id="e0972-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="e0972-283">Por lo tanto, se produce un error del vinculador durante la vinculación del archivo de recursos específico del lenguaje porque el archivo no tiene recursos de versión.</span><span class="sxs-lookup"><span data-stu-id="e0972-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-284">-g</span><span class="sxs-lookup"><span data-stu-id="e0972-284">-g</span></span></td>
<td><span data-ttu-id="e0972-285">Especifica el identificador de <a href="language-identifiers.md">idioma de reserva</a> final en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e0972-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-286">-G1</span><span class="sxs-lookup"><span data-stu-id="e0972-286">-g1</span></span></td>
<td><span data-ttu-id="e0972-287">Crea un archivo MUI. res aunque el recurso de versión sea el único contenido traducible.</span><span class="sxs-lookup"><span data-stu-id="e0972-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="e0972-288">De forma predeterminada, el compilador RC no genera un archivo. res si la versión es el único recurso traducible.</span><span class="sxs-lookup"><span data-stu-id="e0972-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-289">-g2</span><span class="sxs-lookup"><span data-stu-id="e0972-289">-g2</span></span></td>
<td><span data-ttu-id="e0972-290">Especifica el número de versión personalizado que se va a utilizar al calcular la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0972-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="e0972-291">mui_res_name</span></span></td>
<td><span data-ttu-id="e0972-292">Archivo de recursos para recursos específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="e0972-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="e0972-294">Archivo de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0972-295">langid</span><span class="sxs-lookup"><span data-stu-id="e0972-295">langid</span></span></td>
<td><span data-ttu-id="e0972-296">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0972-297">version</span><span class="sxs-lookup"><span data-stu-id="e0972-297">version</span></span></td>
<td><span data-ttu-id="e0972-298">Número de versión personalizado, en un formato como &quot; 6.2.0.0 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e0972-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="e0972-299">Ejemplo del uso del compilador RC para compilar recursos MUI</span><span class="sxs-lookup"><span data-stu-id="e0972-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="e0972-300">Para ilustrar la operación del compilador RC con recursos de MUI, vamos a examinar la siguiente línea de comandos para el archivo de recursos. RC:</span><span class="sxs-lookup"><span data-stu-id="e0972-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="e0972-301">Esta línea de comandos hace que el compilador de RC haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e0972-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="e0972-302">Cree el archivo de recursos específico del idioma file \_ res. res y un archivo de recursos independiente del idioma que se toma como valor predeterminado de archivo. res, según el nombre del archivo. rc.</span><span class="sxs-lookup"><span data-stu-id="e0972-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="e0972-303">Agregue los tipos de recursos 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY \_ Type al archivo. res específico del idioma si están en el archivo. rc.</span><span class="sxs-lookup"><span data-stu-id="e0972-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="e0972-304">Agregue el tipo de recurso 16, junto con cualquier otro tipo de recurso que se describe en el archivo de recursos al archivo. res independiente del idioma y al archivo. res específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="e0972-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="e0972-305">Tenga en cuenta que, en este ejemplo, el tipo de recurso 16 se agrega en dos lugares.</span><span class="sxs-lookup"><span data-stu-id="e0972-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="e0972-306">Elija el valor del atributo "UltimateFallbackLanguage" para insertar en los datos de configuración de recursos de archivo LN según los criterios siguientes, ordenados de prioridad más alta a más bajo:</span><span class="sxs-lookup"><span data-stu-id="e0972-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="e0972-307">El atributo "UltimateFallbackLanguage" en el archivo de configuración de recursos si se pasa uno como entrada.</span><span class="sxs-lookup"><span data-stu-id="e0972-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="e0972-308">Valor del atributo Language que se va a insertar en los datos de configuración de recursos según el orden del lenguaje del compilador RC (idioma del archivo de recursos independiente del idioma y del idioma).</span><span class="sxs-lookup"><span data-stu-id="e0972-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="e0972-309">Las consideraciones incluyen el idioma en el archivo. rc, el valor de idioma del modificador-GL y el identificador 0x0409 para inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e0972-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0972-310">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0972-310">Remarks</span></span>

<span data-ttu-id="e0972-311">Si incluye cualquier tipo de recurso ICON (3), DIALOG (5), STRING (6) o VERSION (16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources del archivo de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0972-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0972-312">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0972-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0972-313">Referencia de la interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="e0972-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="e0972-314">Administración de recursos de MUI</span><span class="sxs-lookup"><span data-stu-id="e0972-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="e0972-315">Localizar recursos y compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="e0972-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
