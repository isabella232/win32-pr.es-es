---
description: 'WsdCodeGen tiene dos funciones: generar archivos de configuración y generar código fuente para las aplicaciones de cliente y host de WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Sintaxis de la línea de comandos WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908541"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="b6ab1-103">Sintaxis de la línea de comandos WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="b6ab1-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="b6ab1-104">WsdCodeGen tiene dos funciones: generar archivos de configuración y generar código fuente para las aplicaciones de cliente y host de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="b6ab1-105">En este tema se proporciona la sintaxis de línea de comandos que se usa para realizar cada tarea.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="b6ab1-106">Generar un archivo de configuración</span><span class="sxs-lookup"><span data-stu-id="b6ab1-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="b6ab1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6ab1-107">Syntax</span></span>

<span data-ttu-id="b6ab1-108">**WSDCODEGEN.EXE** **/generateconfig:**{**cliente** \| **host** \| **All**} **\[ /OutputFile:**_nombrearchivoconfig_ *_\]_* *WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="b6ab1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6ab1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ab1-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {cliente \| host \| todos}**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-111">El tipo de código que generará el archivo de configuración de salida.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="b6ab1-112">**/generateconfig: el cliente** se usa para generar un archivo de configuración para generar el código de cliente, **/generateconfig: host** se usa para generar un archivo de configuración para generar el código de host y **/generateconfig: ALL** se usa para generar un archivo de configuración para generar el cliente y el código del host.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_nombrearchivoconfig_</span><span class="sxs-lookup"><span data-stu-id="b6ab1-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-114">Este parámetro opcional se usa para especificar el nombre de archivo del archivo de configuración de salida.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="b6ab1-115">Si se excluye este parámetro, se codegen.config el nombre del archivo de configuración de salida.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-117">Incluya una plantilla PnP-X en el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-119">Una lista delimitada por espacios de los archivos WSDL que va a procesar WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="b6ab1-120">Generar código fuente</span><span class="sxs-lookup"><span data-stu-id="b6ab1-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="b6ab1-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6ab1-121">Syntax</span></span>

<span data-ttu-id="b6ab1-122">**WSDCODEGEN.EXE** **/GenerateCode** **\[ /download \]** **\[ /GBC \]** **\[ outputroot:**_ruta de acceso_ *_\]_* **\[ /writeaccess:**_comando_ *_\]_* *nombrearchivoconfig*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="b6ab1-123">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6ab1-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ab1-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-125">Indica a WsdCodeGen que genere código fuente.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="b6ab1-126">Este es el modo predeterminado si no se especifica ningún modo.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-128">Descarga los documentos importados a los que hace referencia el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="b6ab1-129">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-131">Agrega comentarios al código fuente que indica que se ha generado el código.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="b6ab1-132">Estos comentarios llevan como prefijo la frase "generada por".</span><span class="sxs-lookup"><span data-stu-id="b6ab1-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="b6ab1-133">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="b6ab1-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-135">La ubicación de salida para los archivos generados.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-135">The output location for generated files.</span></span> <span data-ttu-id="b6ab1-136">la *ruta de acceso* puede ser una ruta de acceso absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="b6ab1-137">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_comando_</span><span class="sxs-lookup"><span data-stu-id="b6ab1-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-139">Indica a WsdCodeGen que ejecute el comando especificado antes de modificar los archivos existentes en el disco.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="b6ab1-140">Los archivos de salida que sean idénticos a los del disco no recibirán este comando ni se escribirán en él.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="b6ab1-141">Si el comando contiene la secuencia " {0} ", esta secuencia se reemplazará por el nombre del archivo que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="b6ab1-142">De lo contrario, el nombre de archivo se anexará al comando.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="b6ab1-143">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="b6ab1-143">Examples:</span></span>

<span data-ttu-id="b6ab1-144">**/writeaccess: "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="b6ab1-145">**/writeaccess: "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="b6ab1-146">**/writeaccess: "Copy {0} .. \\ copia de seguridad \\ "**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="b6ab1-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nombrearchivoconfig*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="b6ab1-148">Nombre del archivo de configuración que se va a procesar antes de generar el código.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="b6ab1-149">Leyenda de formato</span><span class="sxs-lookup"><span data-stu-id="b6ab1-149">Formatting Legend</span></span>



| <span data-ttu-id="b6ab1-150">Formato</span><span class="sxs-lookup"><span data-stu-id="b6ab1-150">Format</span></span>                                                                    | <span data-ttu-id="b6ab1-151">Significado</span><span class="sxs-lookup"><span data-stu-id="b6ab1-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b6ab1-152">*Cursiva*</span><span class="sxs-lookup"><span data-stu-id="b6ab1-152">*Italic*</span></span>                                                                  | <span data-ttu-id="b6ab1-153">Información que el usuario debe proporcionar</span><span class="sxs-lookup"><span data-stu-id="b6ab1-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="b6ab1-154">**Negrita**</span><span class="sxs-lookup"><span data-stu-id="b6ab1-154">**Bold**</span></span>                                                                  | <span data-ttu-id="b6ab1-155">Elementos que el usuario debe escribir exactamente como se indica</span><span class="sxs-lookup"><span data-stu-id="b6ab1-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="b6ab1-156">Entre corchetes ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="b6ab1-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="b6ab1-157">Elementos opcionales</span><span class="sxs-lookup"><span data-stu-id="b6ab1-157">Optional items</span></span>                                          |
| <span data-ttu-id="b6ab1-158">Entre llaves ( {} ); opciones separadas por canalización ( \| ).</span><span class="sxs-lookup"><span data-stu-id="b6ab1-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="b6ab1-159">Ejemplo: { \| impares}</span><span class="sxs-lookup"><span data-stu-id="b6ab1-159">Example: {even\|odd}</span></span> | <span data-ttu-id="b6ab1-160">Conjunto de opciones de las que el usuario debe elegir sólo una.</span><span class="sxs-lookup"><span data-stu-id="b6ab1-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b6ab1-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ab1-161">Requirements</span></span>



| <span data-ttu-id="b6ab1-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ab1-162">Requirement</span></span> | <span data-ttu-id="b6ab1-163">Value</span><span class="sxs-lookup"><span data-stu-id="b6ab1-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6ab1-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6ab1-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ab1-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6ab1-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6ab1-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6ab1-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ab1-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6ab1-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6ab1-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6ab1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ab1-169">Archivo de configuración WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="b6ab1-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="b6ab1-170">Usar WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="b6ab1-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




