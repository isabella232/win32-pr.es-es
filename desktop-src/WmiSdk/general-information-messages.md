---
description: Los siguientes mensajes de información describen la operación del compilador.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Mensajes de información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360581"
---
# <a name="general-information-messages"></a><span data-ttu-id="e5a78-103">Mensajes de información general</span><span class="sxs-lookup"><span data-stu-id="e5a78-103">General Information Messages</span></span>

<span data-ttu-id="e5a78-104">Los siguientes mensajes de información describen la operación del compilador.</span><span class="sxs-lookup"><span data-stu-id="e5a78-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="e5a78-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versión <\#> definiciones MIB compiladas desde <file name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-106">Este mensaje aparece al principio de cada compilación de archivos.</span><span class="sxs-lookup"><span data-stu-id="e5a78-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="e5a78-107">Significa que es posible que el usuario haya especificado explícitamente en la línea de comandos o que el compilador lo haya extraído de los directorios de inclusión del registro o de los directorios de inclusión que se mencionan en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e5a78-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error de comprobación de sintaxis en <file name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-109">Los mensajes de error específicos que preceden a este mensaje proporcionan la naturaleza de los errores de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="e5a78-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error de comprobación semántica en <file name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-111">Los mensajes de error específicos que preceden a este mensaje proporcionan la naturaleza de los errores semánticos.</span><span class="sxs-lookup"><span data-stu-id="e5a78-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: no se pudo cargar <file name> en Smir**</span><span class="sxs-lookup"><span data-stu-id="e5a78-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-113">Error de comprobación de sintaxis o semántica en el módulo o no se completó la interacción con SMIR.</span><span class="sxs-lookup"><span data-stu-id="e5a78-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación de sintaxis correcta el <file name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e5a78-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación semántica correcta el <file name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e5a78-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: se cargó <file name> correctamente en Smir**</span><span class="sxs-lookup"><span data-stu-id="e5a78-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e5a78-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: no se pudieron resolver uno o más símbolos en <module name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-118">No se encontraron los módulos correspondientes a uno o varios símbolos importados en el módulo especificado o no se pudieron compilar.</span><span class="sxs-lookup"><span data-stu-id="e5a78-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: no se pudo conectar con SMIR**</span><span class="sxs-lookup"><span data-stu-id="e5a78-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-120">Asegúrese de que exista Smir.dll, se haya registrado con el comando regsvr32 y de que el servidor de Instrumental de administración de Windows (WMI) esté en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="e5a78-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: módulos en la lista SMIR: <de módulos, 1 en cada línea>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-122">Esta es la salida del modificador **/l** .</span><span class="sxs-lookup"><span data-stu-id="e5a78-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir no pudo enumerar los módulos de SMIR**</span><span class="sxs-lookup"><span data-stu-id="e5a78-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-124">Esto indica un error del modificador **/l** debido a que no hay conexión Smir.</span><span class="sxs-lookup"><span data-stu-id="e5a78-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: se eliminó el módulo <module name> correctamente**</span><span class="sxs-lookup"><span data-stu-id="e5a78-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-126">El modificador **/d** se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5a78-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: no se pudo eliminar el módulo <module name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-128">Esto indica un error del modificador **/d** debido a que no hay conexión Smir.</span><span class="sxs-lookup"><span data-stu-id="e5a78-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: se eliminaron todos los módulos del SMIR**</span><span class="sxs-lookup"><span data-stu-id="e5a78-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-130">El modificador **/p** se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5a78-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: no se pudieron eliminar todos los módulos de SMIR**</span><span class="sxs-lookup"><span data-stu-id="e5a78-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-132">Error del modificador **/p** porque no hay conexión Smir.</span><span class="sxs-lookup"><span data-stu-id="e5a78-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: el módulo no <module name> existe en Smir**</span><span class="sxs-lookup"><span data-stu-id="e5a78-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-134">Error del modificador **/d** porque el módulo especificado no está en Smir.</span><span class="sxs-lookup"><span data-stu-id="e5a78-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: se generó el MOF correctamente**</span><span class="sxs-lookup"><span data-stu-id="e5a78-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-136">El modificador **/g** o **/GC** funcionó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5a78-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: no se pudo generar MOF**</span><span class="sxs-lookup"><span data-stu-id="e5a78-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-138">El modificador **/g** o **/GC** no funcionaba correctamente debido a que no hay ninguna conexión Smir.</span><span class="sxs-lookup"><span data-stu-id="e5a78-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nombre del módulo: <module name>**</span><span class="sxs-lookup"><span data-stu-id="e5a78-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-140">Este es el resultado correcto del modificador **/n** .</span><span class="sxs-lookup"><span data-stu-id="e5a78-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: no se pudo analizar <file name> correctamente**</span><span class="sxs-lookup"><span data-stu-id="e5a78-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-142">Esto indica un error del modificador **/n** o **/ni** porque el archivo especificado no es un archivo MIB válido.</span><span class="sxs-lookup"><span data-stu-id="e5a78-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: archivos procesados <number> correctamente**</span><span class="sxs-lookup"><span data-stu-id="e5a78-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-144">Especifica el número de archivos que se analizaron correctamente cuando se usaron el modificador **/r** o **/auto** .</span><span class="sxs-lookup"><span data-stu-id="e5a78-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: archivos repetidos en la entrada para el módulo <module name> . Solo <file name> se compilará el archivo**</span><span class="sxs-lookup"><span data-stu-id="e5a78-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-146">El usuario ha especificado explícitamente más de un archivo en la línea de comandos y dos o más de estos archivos tienen el mismo módulo MIB.</span><span class="sxs-lookup"><span data-stu-id="e5a78-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: se ha agregado <directory name> el directorio al registro**</span><span class="sxs-lookup"><span data-stu-id="e5a78-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-148">El modificador **/PA** se ha ejecutado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5a78-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: no se pudo agregar <directory name> el directorio al registro**</span><span class="sxs-lookup"><span data-stu-id="e5a78-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-150">Error del modificador **/PA** , que solo sucede si se produce un error en la API del registro.</span><span class="sxs-lookup"><span data-stu-id="e5a78-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: directorio eliminado <directory name> del registro**</span><span class="sxs-lookup"><span data-stu-id="e5a78-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-152">Éxito del modificador **/PD** .</span><span class="sxs-lookup"><span data-stu-id="e5a78-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: no se pudo eliminar <directory name> del registro**</span><span class="sxs-lookup"><span data-stu-id="e5a78-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-154">Error del modificador **/PD** .</span><span class="sxs-lookup"><span data-stu-id="e5a78-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="e5a78-155">El directorio especificado no existe en la lista de directorios del registro.</span><span class="sxs-lookup"><span data-stu-id="e5a78-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="e5a78-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> no es un archivo MIB válido**</span><span class="sxs-lookup"><span data-stu-id="e5a78-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="e5a78-157">Se ha especificado más de un archivo en la línea de comandos, uno de los cuales no es un archivo MIB válido.</span><span class="sxs-lookup"><span data-stu-id="e5a78-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e5a78-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5a78-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a78-159">Configuración del entorno SNMP de WMI</span><span class="sxs-lookup"><span data-stu-id="e5a78-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



