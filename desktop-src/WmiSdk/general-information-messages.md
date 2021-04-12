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
# <a name="general-information-messages"></a>Mensajes de información general

Los siguientes mensajes de información describen la operación del compilador.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versión <\#> definiciones MIB compiladas desde <file name>**
</dt> <dd>

Este mensaje aparece al principio de cada compilación de archivos. Significa que es posible que el usuario haya especificado explícitamente en la línea de comandos o que el compilador lo haya extraído de los directorios de inclusión del registro o de los directorios de inclusión que se mencionan en la línea de comandos.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error de comprobación de sintaxis en <file name>**
</dt> <dd>

Los mensajes de error específicos que preceden a este mensaje proporcionan la naturaleza de los errores de sintaxis.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error de comprobación semántica en <file name>**
</dt> <dd>

Los mensajes de error específicos que preceden a este mensaje proporcionan la naturaleza de los errores semánticos.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: no se pudo cargar <file name> en Smir**
</dt> <dd>

Error de comprobación de sintaxis o semántica en el módulo o no se completó la interacción con SMIR.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación de sintaxis correcta el <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación semántica correcta el <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: se cargó <file name> correctamente en Smir**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: no se pudieron resolver uno o más símbolos en <module name>**
</dt> <dd>

No se encontraron los módulos correspondientes a uno o varios símbolos importados en el módulo especificado o no se pudieron compilar.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: no se pudo conectar con SMIR**
</dt> <dd>

Asegúrese de que exista Smir.dll, se haya registrado con el comando regsvr32 y de que el servidor de Instrumental de administración de Windows (WMI) esté en funcionamiento.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: módulos en la lista SMIR: <de módulos, 1 en cada línea>**
</dt> <dd>

Esta es la salida del modificador **/l** .

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir no pudo enumerar los módulos de SMIR**
</dt> <dd>

Esto indica un error del modificador **/l** debido a que no hay conexión Smir.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: se eliminó el módulo <module name> correctamente**
</dt> <dd>

El modificador **/d** se ejecutó correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: no se pudo eliminar el módulo <module name>**
</dt> <dd>

Esto indica un error del modificador **/d** debido a que no hay conexión Smir.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: se eliminaron todos los módulos del SMIR**
</dt> <dd>

El modificador **/p** se ejecutó correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: no se pudieron eliminar todos los módulos de SMIR**
</dt> <dd>

Error del modificador **/p** porque no hay conexión Smir.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: el módulo no <module name> existe en Smir**
</dt> <dd>

Error del modificador **/d** porque el módulo especificado no está en Smir.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: se generó el MOF correctamente**
</dt> <dd>

El modificador **/g** o **/GC** funcionó correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: no se pudo generar MOF**
</dt> <dd>

El modificador **/g** o **/GC** no funcionaba correctamente debido a que no hay ninguna conexión Smir.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nombre del módulo: <module name>**
</dt> <dd>

Este es el resultado correcto del modificador **/n** .

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: no se pudo analizar <file name> correctamente**
</dt> <dd>

Esto indica un error del modificador **/n** o **/ni** porque el archivo especificado no es un archivo MIB válido.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: archivos procesados <number> correctamente**
</dt> <dd>

Especifica el número de archivos que se analizaron correctamente cuando se usaron el modificador **/r** o **/auto** .

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: archivos repetidos en la entrada para el módulo <module name> . Solo <file name> se compilará el archivo**
</dt> <dd>

El usuario ha especificado explícitamente más de un archivo en la línea de comandos y dos o más de estos archivos tienen el mismo módulo MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: se ha agregado <directory name> el directorio al registro**
</dt> <dd>

El modificador **/PA** se ha ejecutado correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: no se pudo agregar <directory name> el directorio al registro**
</dt> <dd>

Error del modificador **/PA** , que solo sucede si se produce un error en la API del registro.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: directorio eliminado <directory name> del registro**
</dt> <dd>

Éxito del modificador **/PD** .

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: no se pudo eliminar <directory name> del registro**
</dt> <dd>

Error del modificador **/PD** . El directorio especificado no existe en la lista de directorios del registro.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> no es un archivo MIB válido**
</dt> <dd>

Se ha especificado más de un archivo en la línea de comandos, uno de los cuales no es un archivo MIB válido.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno SNMP de WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



