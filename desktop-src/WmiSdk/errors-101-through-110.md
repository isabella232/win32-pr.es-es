---
description: Describe los errores del proveedor SNMP de WMI de 101 a 110.
ms.assetid: baa64233-eb19-4f52-836b-5bdf4a23ae4f
ms.tgt_platform: multiple
title: Errores de 101 a 110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21874ada13d15920e755e5061ec638ad51fa0f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666878"
---
# <a name="errors-101-through-110"></a>Errores de 101 a 110

Describe los errores del proveedor SNMP de WMI de 101 a 110.

[Error irrecuperable 101](#fatal-error-101)

[Error irrecuperable 102](#fatal-error-102)

[Error irrecuperable 103](#fatal-error-103)

[Error irrecuperable 104](#fatal-error-104)

[Error irrecuperable 105](#fatal-error-105)

[Error irrecuperable 106](#fatal-error-106)

[Error irrecuperable 107](#fatal-error-107)

[Error irrecuperable 108](#fatal-error-108)

[Error irrecuperable 109](#fatal-error-109)

[ADVERTENCIA 110](#warning-110)

## <a name="fatal-error-101"></a>Error irrecuperable 101

<dl> <dt>

<span id="_101__Fatal____Usage_"></span><span id="_101__fatal____usage_"></span><span id="_101__FATAL____USAGE_"></span>**<101,> irrecuperable: "uso:**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___VersionArgs___CommandArgs_"></span><span id="smi2smir__diagnosticargs___versionargs___commandargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___VERSIONARGS___COMMANDARGS_"></span>**smi2smir <DiagnosticArgs> <VersionArgs><CommandArgs>**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___RegistryArgs_"></span><span id="smi2smir__diagnosticargs___registryargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___REGISTRYARGS_"></span>**smi2smir <DiagnosticArgs><RegistryArgs>**
</dt> <dd></dd> <dt>

<span id="smi2smir__HelpArgs__"></span><span id="smi2smir__helpargs__"></span><span id="SMI2SMIR__HELPARGS__"></span>**smi2smir <HelpArgs> "**
</dt> <dd>

Error de sintaxis de línea de comandos. A continuación se explican los modificadores.

</dd> </dl>

## <a name="fatal-error-102"></a>Error irrecuperable 102

<dl> <dt>

<span id="_102__Fatal___Invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__fatal___invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__FATAL___INVALID_ARGUMENT_ON_COMMAND_LINE_AFTER__LAST_CORRECT_ARGUMENT__"></span>**<102,> grave: "argumento no válido en la línea de comandos después de <last correct argument> "**
</dt> <dd>

Error de sintaxis de línea de comandos. Hay algunos argumentos adicionales o un modificador no es válido en la línea de comandos. El <last correct argument> parámetro hace referencia al último argumento que se leyó correctamente en la línea de comandos y, posiblemente, puede ser smi2smir, que es el nombre del archivo ejecutable del compilador de información del módulo SNMP.

</dd> </dl>

## <a name="fatal-error-103"></a>Error irrecuperable 103

<dl> <dt>

<span id="_103__Fatal____Diagnostic_Level_not_specified_for_the__m_switch_"></span><span id="_103__fatal____diagnostic_level_not_specified_for_the__m_switch_"></span><span id="_103__FATAL____DIAGNOSTIC_LEVEL_NOT_SPECIFIED_FOR_THE__M_SWITCH_"></span>**<103,> grave: "no se ha especificado el nivel de diagnóstico para el modificador/m"**
</dt> <dd>

Error de sintaxis de línea de comandos. Si especifica el modificador **/m** , también debe especificar un nivel de diagnóstico de 0, 1 o 2.

</dd> </dl>

## <a name="fatal-error-104"></a>Error irrecuperable 104

<dl> <dt>

<span id="_104__Fatal____Diagnostic_Level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__fatal____diagnostic_level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__FATAL____DIAGNOSTIC_LEVEL_MUST_BE_0__1_OR_2_FOR_THE__M_SWITCH_"></span>**<104,> grave: "el nivel de diagnóstico debe ser 0, 1 o 2 para el modificador/m"**
</dt> <dd>

Error de sintaxis de línea de comandos. Si especifica el modificador **/m** , también debe especificar un nivel de diagnóstico de 0, 1 o 2.

</dd> </dl>

## <a name="fatal-error-105"></a>Error irrecuperable 105

<dl> <dt>

<span id="_105__Fatal____Maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__fatal____maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__FATAL____MAXIMUM_DIAGNOSTIC_COUNT_MISSING_AFTER_THE__C_SWITCH_"></span>**<105,> irrecuperable: "número máximo de diagnósticos que faltan después del modificador/c"**
</dt> <dd>

Error de sintaxis de línea de comandos. Si especifica el modificador **/c** , también debe especificar un entero no negativo como el recuento máximo.

</dd> </dl>

## <a name="fatal-error-106"></a>Error irrecuperable 106

<dl> <dt>

<span id="_106__Fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__FATAL_____ARGUMENT__IS_NOT_A_VALID_DIAGNOSTIC_COUNT_"></span>**<106,> irrecuperable: " <argument> no es un número de diagnósticos válido"**
</dt> <dd>

Error de sintaxis de línea de comandos. Si especifica el modificador **/c** , también debe especificar un entero no negativo como el recuento máximo.

</dd> </dl>

## <a name="fatal-error-107"></a>Error irrecuperable 107

<dl> <dt>

<span id="_107__Fatal____File_Name_s__missing_"></span><span id="_107__fatal____file_name_s__missing_"></span><span id="_107__FATAL____FILE_NAME_S__MISSING_"></span>**<107,> irrecuperable: "faltan nombres de archivo"**
</dt> <dd>

Error semántico de la línea de comandos. Se deben especificar uno o más nombres de archivo en la línea de comandos para la combinación de modificadores indicada.

</dd> </dl>

## <a name="fatal-error-108"></a>Error irrecuperable 108

<dl> <dt>

<span id="_108__Fatal____No_command_argument_specified_"></span><span id="_108__fatal____no_command_argument_specified_"></span><span id="_108__FATAL____NO_COMMAND_ARGUMENT_SPECIFIED_"></span>**<108,> grave: "no se ha especificado ningún argumento de comando"**
</dt> <dd>

Error de sintaxis de línea de comandos. Se debe especificar alguna acción en la línea de comandos.

</dd> </dl>

## <a name="fatal-error-109"></a>Error irrecuperable 109

<dl> <dt>

<span id="_109__Fatal____Module_name_missing_"></span><span id="_109__fatal____module_name_missing_"></span><span id="_109__FATAL____MODULE_NAME_MISSING_"></span>**<109,> irrecuperable: "falta el nombre del módulo"**
</dt> <dd>

Error de sintaxis de línea de comandos.

</dd> </dl>

## <a name="warning-110"></a>ADVERTENCIA 110

<dl> <dt>

<span id="_110__Warning____No_include_path_specified_after_the__i_switch_"></span><span id="_110__warning____no_include_path_specified_after_the__i_switch_"></span><span id="_110__WARNING____NO_INCLUDE_PATH_SPECIFIED_AFTER_THE__I_SWITCH_"></span>**<110, ADVERTENCIA>: "no se ha especificado ninguna ruta de acceso de inclusión después del modificador/i"**
</dt> <dd>

ADVERTENCIA de sintaxis de la línea de comandos. Si especifica el modificador **/i** , también debe especificar la ruta de acceso a los archivos incluidos.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno SNMP de WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



