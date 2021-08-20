---
description: Los siguientes mensajes de información describen la operación del compilador.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Mensajes de información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a0889d165e16b5ba5d7d4948f20b9aec60030755984e2a4af7c4fc118c2c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819333"
---
# <a name="general-information-messages"></a>Mensajes de información general

Los siguientes mensajes de información describen la operación del compilador.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versión <de> \# definiciones de MIB compiladas a partir de <file name>**
</dt> <dd>

Este mensaje aparece al principio de cada compilación de archivos. Esto significa que el usuario puede haber especificado explícitamente el archivo en la línea de comandos o que el compilador lo haya extraido de los directorios include del Registro o de los directorios include mencionados en la línea de comandos.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error en la comprobación de sintaxis <file name>**
</dt> <dd>

Los mensajes de error específicos que preceden a este mensaje dan la naturaleza de los errores de sintaxis.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: error de comprobación semántica en <file name>**
</dt> <dd>

Los mensajes de error específicos que preceden a este mensaje dan la naturaleza de los errores semánticos.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: no se pudo cargar <file name> en el smir**
</dt> <dd>

Error de sintaxis o comprobación semántica en el módulo, o la interacción de SMIR no se ha completado.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación de sintaxis correcta en <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: comprobación semántica correcta en <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: se <file name> ha cargado correctamente en el smir.**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: no se pudo resolver uno o varios símbolos en <module name>**
</dt> <dd>

Los módulos correspondientes a uno o varios de los símbolos importados en el módulo especificado no se encontraron o no se pudieron compilar.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: no se pudo conectar a SMIR**
</dt> <dd>

Asegúrese de Smir.dll existente, se haya registrado mediante el comando regsvr32 y de que el servidor de Windows Management Instrumentation (WMI) esté en funcionamiento.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: módulos en SAMI: <lista de módulos, 1 en cada línea>**
</dt> <dd>

Esta es la salida del **modificador /l.**

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir No se pudieron enumerar los módulos en SMIR**
</dt> <dd>

Esto indica un error del conmutador **/l** debido a que no hay conexión SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: módulo eliminado <module name> correctamente**
</dt> <dd>

El **modificador /d** se ha cambiado correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: No se pudo eliminar el módulo <module name>**
</dt> <dd>

Esto indica un error del conmutador **/d** debido a que no hay conexión SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: se han eliminado todos los módulos de SMIR.**
</dt> <dd>

El **modificador /p** se ha cambiado correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: no se pudieron eliminar todos los módulos de SMIR**
</dt> <dd>

Error en el modificador **/p** porque no hay ninguna conexión SMIR.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: el <module name> módulo no existe en SMIR**
</dt> <dd>

Error en el modificador **/d** porque el módulo especificado no está en el SMIR.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MOF generado correctamente**
</dt> <dd>

El **modificador /g** **o /gc** ha funcionado correctamente.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: No se pudo generar MOF**
</dt> <dd>

El **modificador /g** **o /gc** no funcionaba correctamente debido a que no había conexión SMIR.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nombre del módulo: <module name>**
</dt> <dd>

Esta es la salida correcta del **modificador /n.**

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: No se pudo analizar <file name> correctamente**
</dt> <dd>

Esto indica un error del modificador **/n** o **/ni** porque el archivo especificado no es un archivo MIB válido.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: archivos procesados <number> correctamente**
</dt> <dd>

Esto especifica el número de archivos que se analizaron correctamente cuando se usaron el modificador **/r** o **/auto.**

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: archivos repetidos en la entrada del módulo <module name> . Solo se <file name> compilará el archivo**
</dt> <dd>

El usuario ha especificado explícitamente más de un archivo en la línea de comandos y dos o más de estos archivos tienen el mismo módulo MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: se ha agregado el <directory name> directorio al registro.**
</dt> <dd>

Correcto del **modificador /pa.**

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: no se pudo agregar el <directory name> directorio al registro**
</dt> <dd>

Error del modificador **/pa,** que solo se produce si se produce un error en la API del Registro.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: directorio eliminado <directory name> del registro**
</dt> <dd>

Correcto del **modificador /pd.**

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: no se pudo eliminar <directory name> del registro**
</dt> <dd>

Error del **modificador /pd.** El directorio especificado no existe en la lista de directorios del Registro.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> no es un archivo mib válido**
</dt> <dd>

Se ha especificado más de un archivo en la línea de comandos, uno de los cuales no es un archivo MIB válido.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno SNMP de WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



