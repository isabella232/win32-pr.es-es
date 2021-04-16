---
description: En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Crear diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696209"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="788bc-103">Crear diccionarios personalizados para el reconocimiento de escritura a mano en Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="788bc-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="788bc-104">En esta sección se explica cómo crear un diccionario personalizado para el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="788bc-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="788bc-105">En el sistema operativo Windows 7 y el sistema operativo Windows Server 2008 R2, la precisión del reconocimiento de escritura a mano se puede mejorar significativamente mediante el uso de diccionarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="788bc-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="788bc-106">Estos diccionarios complementan o reemplazan diccionarios del sistema usados para escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="788bc-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="788bc-107">La compatibilidad con el reconocimiento de escritura a mano se proporciona a través de la característica Servicios de Escritura con lápiz y Escritura a mano que debe habilitarse a través de Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="788bc-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="788bc-108">Los diccionarios personalizados solo se pueden instalar para un idioma si el reconocedor de escritura a mano para ese idioma está instalado.</span><span class="sxs-lookup"><span data-stu-id="788bc-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="788bc-109">Hay dos pasos básicos para configurar un diccionario personalizado para escritura a mano:</span><span class="sxs-lookup"><span data-stu-id="788bc-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="788bc-110">Compilar una lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="788bc-110">Compile a word list.</span></span> <span data-ttu-id="788bc-111">La compilación crea un archivo de diccionario personalizado (. hwrdict) compilado.</span><span class="sxs-lookup"><span data-stu-id="788bc-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="788bc-112">Instale el diccionario personalizado compilado.</span><span class="sxs-lookup"><span data-stu-id="788bc-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="788bc-113">Compilar una lista de palabras</span><span class="sxs-lookup"><span data-stu-id="788bc-113">Compiling a Word List</span></span>

<span data-ttu-id="788bc-114">La lista de palabras que se va a compilar debe estar en formato de texto sin formato y debe guardarse con una codificación Unicode.</span><span class="sxs-lookup"><span data-stu-id="788bc-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="788bc-115">Otras codificaciones no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="788bc-115">Other encodings will not work.</span></span> <span data-ttu-id="788bc-116">Cada línea del archivo de texto se toma como una sola entrada en el diccionario.</span><span class="sxs-lookup"><span data-stu-id="788bc-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="788bc-117">Se permiten las entradas de unidades multipalabra que contienen uno o varios espacios.</span><span class="sxs-lookup"><span data-stu-id="788bc-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="788bc-118">Se omiten los espacios al principio o al final de una línea.</span><span class="sxs-lookup"><span data-stu-id="788bc-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="788bc-119">Un diccionario personalizado se compila desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="788bc-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="788bc-120">Para compilar un diccionario, abra una ventana de comandos, navegue hasta la carpeta que contiene la lista de palabras y, a continuación, ejecute HwrComp.exe con las opciones de línea de comandos que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="788bc-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="788bc-121">En el ejemplo siguiente se muestra la sintaxis de uso de las opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="788bc-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="788bc-122">Explicación de las opciones</span><span class="sxs-lookup"><span data-stu-id="788bc-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="788bc-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="788bc-123">Parameter</span></span></th>
<th><span data-ttu-id="788bc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="788bc-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="788bc-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="788bc-125">-lang <localename></span></span></td>
<td><span data-ttu-id="788bc-126">Nombre de configuración regional especificado que se ha asignado al archivo de diccionario personalizado compilado.</span><span class="sxs-lookup"><span data-stu-id="788bc-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="788bc-127">El argumento <localename> tiene el formato Language-region.</span><span class="sxs-lookup"><span data-stu-id="788bc-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="788bc-128">Un ejemplo de esto es en-US, que indica el idioma Inglés de la región de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="788bc-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="788bc-129">Para obtener ejemplos de este formulario, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="788bc-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="788bc-130">Los siguientes idiomas son compatibles con Windows 7 y Windows Server 2008 R2 gracias a esta característica: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-is, pt-BR, pt-PT, da-DK, SV-SE, NB-NO, NN-NO, fi-FI, pl-PL, CS-CZ, ru-RU, RO-RO, Sr-Latn-CS, Sr-Cyrl-CS, CA-ES y hr-HR.</span><span class="sxs-lookup"><span data-stu-id="788bc-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="788bc-131">-Type <type></span><span class="sxs-lookup"><span data-stu-id="788bc-131">-type <type></span></span></td>
<td><span data-ttu-id="788bc-132">El argumento de opción <type> es una concatenación de cadena única del uso del recurso como la lista de palabras principales (principal) o como un complemento de la lista de palabras principales (secundaria) seguida del nombre de lista de palabras real al que se aplica el recurso (como diccionario o apellidos).</span><span class="sxs-lookup"><span data-stu-id="788bc-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="788bc-133">Estos son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="788bc-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="788bc-134">PRIMARY-CITYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-135">PRIMARY-COUNTRYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-136">PRIMARY-COUNTRYSHORTNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-137">DICCIONARIO PRINCIPAL</span><span class="sxs-lookup"><span data-stu-id="788bc-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="788bc-138">PRIMARY-GIVENNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-139">PRIMARY-STATEORPROVINCE-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="788bc-140">PRIMARY-STREETNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-141">LISTA DE PRINCIPALES APELLIDOS</span><span class="sxs-lookup"><span data-stu-id="788bc-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-142">SECUNDARIO-CITYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-143">SECUNDARIO-COUNTRYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-144">SECUNDARIO-COUNTRYSHORTNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-145">DICCIONARIO SECUNDARIO</span><span class="sxs-lookup"><span data-stu-id="788bc-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="788bc-146">SECUNDARIO-EMAILSMTP-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="788bc-147">SECUNDARIO-EMAILUSERNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-148">SECUNDARIA-GIVENNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-149">SECUNDARIO-STATEORPROVINCE-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="788bc-150">SECUNDARIO-STREETNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="788bc-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-151">LISTA DE APELLIDOS SECUNDARIOS</span><span class="sxs-lookup"><span data-stu-id="788bc-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="788bc-152">LISTA DE DIRECCIONES URL SECUNDARIAS</span><span class="sxs-lookup"><span data-stu-id="788bc-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="788bc-153">Si un valor de tipo comienza con el prefijo PRIMAry, el Diccionario compilado, una vez instalado, reemplazará el Diccionario del sistema para ese idioma.</span><span class="sxs-lookup"><span data-stu-id="788bc-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="788bc-154">El valor del diccionario PRIMAry-DICTIONARY representa el Diccionario del sistema principal para un idioma.</span><span class="sxs-lookup"><span data-stu-id="788bc-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="788bc-155">Reemplazar un diccionario del sistema no hace nada en el contenido del Diccionario del sistema original, ya que el reemplazo solo está en vigor hasta que se haya quitado el diccionario personalizado.</span><span class="sxs-lookup"><span data-stu-id="788bc-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="788bc-156">Si un valor de tipo comienza con el prefijo secundario, el Diccionario compilado complementará el Diccionario del sistema sin reemplazarlo.</span><span class="sxs-lookup"><span data-stu-id="788bc-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="788bc-157">-Comentario</span><span class="sxs-lookup"><span data-stu-id="788bc-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="788bc-158">El comentario especificado se compila en el archivo del diccionario.</span><span class="sxs-lookup"><span data-stu-id="788bc-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="788bc-159">El comentario debe ser una cadena única y no tener más de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="788bc-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="788bc-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="788bc-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="788bc-161">La salida se escribe en el nombre de archivo especificado por <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="788bc-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="788bc-162">Si falta esta opción, el nombre del archivo de salida se deriva del nombre del archivo de entrada original, con la extensión de archivo de entrada reemplazada por. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="788bc-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="788bc-163">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="788bc-163">Defaults</span></span>

<span data-ttu-id="788bc-164">Si no se especifican parámetros, los valores de opción predeterminados son</span><span class="sxs-lookup"><span data-stu-id="788bc-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="788bc-165">-lang <current input language> -tipo secundario-Diccionario</span><span class="sxs-lookup"><span data-stu-id="788bc-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="788bc-166">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="788bc-166">Examples</span></span>

<span data-ttu-id="788bc-167">El siguiente compila el archivo de entrada mylist1.txt, aplica los valores de opción predeterminados y crea el archivo de salida mylist1. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="788bc-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="788bc-168">En cambio, el siguiente compila mylist1.txt en myrsrc1. hwrdict, pero asigna "English (EE. UU.)" (en-US) como el idioma y el Diccionario secundario como tipo.</span><span class="sxs-lookup"><span data-stu-id="788bc-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="788bc-169">Instalación de un diccionario personalizado compilado</span><span class="sxs-lookup"><span data-stu-id="788bc-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="788bc-170">HwrComp.exe crea un archivo. hwrdict, que se encuentra en un formato binario que puede usar un reconocedor de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="788bc-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="788bc-171">Este archivo se puede instalar en cualquier equipo que ejecute Windows 7 o Windows Server 2008 R2 y que admita el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="788bc-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="788bc-172">Un diccionario se instala solo para el usuario actual o para todos los usuarios de un equipo.</span><span class="sxs-lookup"><span data-stu-id="788bc-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="788bc-173">Un archivo de diccionario personalizado compilado se puede instalar desde la línea de comandos mediante el HwrReg.exe de herramientas.</span><span class="sxs-lookup"><span data-stu-id="788bc-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="788bc-174">Esta herramienta es útil si desea invalidar algunos de los valores de configuración que se compilan en el archivo o son los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="788bc-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="788bc-175">Hay dos maneras de ejecutar HwrReg.exe: en modo de comprobación e instalación y en modo de lista/eliminación.</span><span class="sxs-lookup"><span data-stu-id="788bc-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="788bc-176">Ejecutar HwrReg.exe en modo de comprobación/instalación</span><span class="sxs-lookup"><span data-stu-id="788bc-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="788bc-177">Este modo es para los archivos de diccionario personalizados que todavía no se han instalado.</span><span class="sxs-lookup"><span data-stu-id="788bc-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="788bc-178">A continuación se muestra la sintaxis de uso de las opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="788bc-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="788bc-179">Explicación de las opciones</span><span class="sxs-lookup"><span data-stu-id="788bc-179">Explanation of Options</span></span>



| <span data-ttu-id="788bc-180">Parámetro</span><span class="sxs-lookup"><span data-stu-id="788bc-180">Parameter</span></span>                | <span data-ttu-id="788bc-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="788bc-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="788bc-182">-comprobar</span><span class="sxs-lookup"><span data-stu-id="788bc-182">-check</span></span>                   | <span data-ttu-id="788bc-183">El archivo de diccionario se comprueba sin instalarse.</span><span class="sxs-lookup"><span data-stu-id="788bc-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="788bc-184">La opción check muestra el comentario del archivo, además de la información de registro que se utilizaría para instalar el archivo.</span><span class="sxs-lookup"><span data-stu-id="788bc-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="788bc-185">Esta opción es útil para comprobar la información de registro antes de que se realice la instalación.</span><span class="sxs-lookup"><span data-stu-id="788bc-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="788bc-186">Si falta esta opción, HwrReg.exe instala el diccionario personalizado.</span><span class="sxs-lookup"><span data-stu-id="788bc-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="788bc-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="788bc-187">lang <localename></span></span> | <span data-ttu-id="788bc-188">El archivo de diccionario se comprueba sin instalarse.</span><span class="sxs-lookup"><span data-stu-id="788bc-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="788bc-189">La opción check muestra el comentario del archivo, además de la información de registro que se utilizaría para instalar el archivo.</span><span class="sxs-lookup"><span data-stu-id="788bc-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="788bc-190">Esta opción es útil para comprobar la información de registro antes de que se realice la instalación.</span><span class="sxs-lookup"><span data-stu-id="788bc-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="788bc-191">Si falta esta opción, HwrReg.exe instala el diccionario personalizado.</span><span class="sxs-lookup"><span data-stu-id="788bc-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="788bc-192">ámbito {todo \| me}</span><span class="sxs-lookup"><span data-stu-id="788bc-192">scope {all\|me}</span></span>         | <span data-ttu-id="788bc-193">El diccionario personalizado se instala para todos los usuarios (ámbito todos) o solo para el usuario actual (ámbito me).</span><span class="sxs-lookup"><span data-stu-id="788bc-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="788bc-194">La instalación de con el ámbito All requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. de lo contrario, se devolverá un código de error.</span><span class="sxs-lookup"><span data-stu-id="788bc-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="788bc-195">Si falta esta opción, el ámbito de la instalación es solo el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="788bc-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="788bc-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="788bc-196">noprompt</span></span>                | <span data-ttu-id="788bc-197">HwrReg.exe no solicita confirmación.</span><span class="sxs-lookup"><span data-stu-id="788bc-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="788bc-198">Esto puede ser útil cuando se ejecuta hwrReg.exe desde un script.</span><span class="sxs-lookup"><span data-stu-id="788bc-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="788bc-199">En el ejemplo siguiente se instala el diccionario personalizado myrsrc1. hwrdict para el idioma "danés (Dinamarca)" (da DK), con el ámbito predeterminado del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="788bc-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="788bc-200">Ejecutar HwrReg.exe en modo List/Remove</span><span class="sxs-lookup"><span data-stu-id="788bc-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="788bc-201">En este modo se enumeran o se quitan los diccionarios personalizados instalados.</span><span class="sxs-lookup"><span data-stu-id="788bc-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="788bc-202">A continuación se muestra la sintaxis de uso de las opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="788bc-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="788bc-203">Explicación de las opciones</span><span class="sxs-lookup"><span data-stu-id="788bc-203">Explanation of Options</span></span>



| <span data-ttu-id="788bc-204">Parámetro</span><span class="sxs-lookup"><span data-stu-id="788bc-204">Parameter</span></span>                | <span data-ttu-id="788bc-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="788bc-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="788bc-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="788bc-206">lang <localename></span></span> | <span data-ttu-id="788bc-207">Los diccionarios registrados solo para este nombre de configuración regional se muestran o se quitan.</span><span class="sxs-lookup"><span data-stu-id="788bc-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="788bc-208">El argumento <localename> tiene la región de idioma del formulario.</span><span class="sxs-lookup"><span data-stu-id="788bc-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="788bc-209">Para obtener ejemplos de este formulario, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="788bc-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="788bc-210">Si falta esta opción, los diccionarios de todos los idiomas se muestran o se quitan.</span><span class="sxs-lookup"><span data-stu-id="788bc-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="788bc-211">ámbito {todo \| me}</span><span class="sxs-lookup"><span data-stu-id="788bc-211">scope {all\|me}</span></span>         | <span data-ttu-id="788bc-212">El diccionario personalizado se instala para todos los usuarios (ámbito todos) o solo para el usuario actual (ámbito me).</span><span class="sxs-lookup"><span data-stu-id="788bc-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="788bc-213">La instalación de con el ámbito All requiere que el comando se ejecute en un símbolo del sistema con privilegios elevados. de lo contrario, se devolverá un código de error.</span><span class="sxs-lookup"><span data-stu-id="788bc-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="788bc-214">Si falta esta opción, el ámbito de la instalación es solo el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="788bc-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="788bc-215">automáticamente <type></span><span class="sxs-lookup"><span data-stu-id="788bc-215">type <type></span></span>       | <span data-ttu-id="788bc-216">Muestra o quita solo los diccionarios registrados con el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="788bc-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="788bc-217">Si falta esta opción, todos los tipos de diccionario se enumeran o se quitan.</span><span class="sxs-lookup"><span data-stu-id="788bc-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="788bc-218">La instalación o eliminación de un diccionario personalizado de otro tipo (como PRIMAry-COUNTRYNAME-LIST) puede afectar al reconocimiento de escritura a mano en otros contextos.</span><span class="sxs-lookup"><span data-stu-id="788bc-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="788bc-219">list</span><span class="sxs-lookup"><span data-stu-id="788bc-219">list</span></span>                    | <span data-ttu-id="788bc-220">Enumera todos los diccionarios instalados que coinciden con las demás opciones.</span><span class="sxs-lookup"><span data-stu-id="788bc-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="788bc-221">Si falta esta opción, se debe especificar la opción Remove.</span><span class="sxs-lookup"><span data-stu-id="788bc-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="788bc-222">remove</span><span class="sxs-lookup"><span data-stu-id="788bc-222">remove</span></span>                  | <span data-ttu-id="788bc-223">Solicita la eliminación de cualquier Diccionario que coincida con las demás opciones.</span><span class="sxs-lookup"><span data-stu-id="788bc-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="788bc-224">Si falta esta opción, se debe especificar la lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="788bc-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="788bc-225">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="788bc-225">Examples</span></span>

<span data-ttu-id="788bc-226">A continuación se enumeran los diccionarios que tienen el idioma "inglés (EE. UU.)" (en Estados Unidos) y el tipo Diccionario primario y que están instalados solo para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="788bc-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="788bc-227">Del mismo modo, el siguiente quita los diccionarios que coinciden con los mismos criterios.</span><span class="sxs-lookup"><span data-stu-id="788bc-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="788bc-228">Notas generales sobre diccionarios personalizados</span><span class="sxs-lookup"><span data-stu-id="788bc-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="788bc-229">Si instala dos diccionarios personalizados que tienen el mismo tipo, idioma y ámbito, la segunda instalación sobrescribirá el primero.</span><span class="sxs-lookup"><span data-stu-id="788bc-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="788bc-230">Si instala dos diccionarios personalizados con el mismo tipo y lenguaje, pero con ámbitos diferentes (uno para todos los usuarios y uno para el usuario actual), el Diccionario instalado para el usuario actual tiene prioridad y se omite el Diccionario instalado para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="788bc-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

