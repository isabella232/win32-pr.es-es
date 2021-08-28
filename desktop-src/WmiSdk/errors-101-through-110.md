---
description: Describe los errores del proveedor SNMP de WMI del 101 al 110.
ms.assetid: baa64233-eb19-4f52-836b-5bdf4a23ae4f
ms.tgt_platform: multiple
title: Errores del 101 al 110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a33a4bc1aee7d9357c0dd46c7bae2e70390f892
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884407"
---
# <a name="errors-101-through-110"></a>Errores del 101 al 110

Describe los errores del proveedor SNMP de WMI del 101 al 110.

[Error irreales 101](#fatal-error-101)

[Error irreales 102](#fatal-error-102)

[Error irreales 103](#fatal-error-103)

[Error irreales 104](#fatal-error-104)

[Error irreales 105](#fatal-error-105)

[Error irreales 106](#fatal-error-106)

[Error irreales 107](#fatal-error-107)

[Error irreales 108](#fatal-error-108)

[Error irreales 109](#fatal-error-109)

[Advertencia 110](#warning-110)

## <a name="fatal-error-101"></a>Error irreales 101

<dl> <dt>

<span id="_101__Fatal____Usage_"></span><span id="_101__fatal____usage_"></span><span id="_101__FATAL____USAGE_"></span>**<101, Error>: "Uso:**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___VersionArgs___CommandArgs_"></span><span id="smi2smir__diagnosticargs___versionargs___commandargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___VERSIONARGS___COMMANDARGS_"></span>**smi2smira &lt; DiagnosticArgs &gt; &lt; VersionArgs &gt; &lt; CommandArgs&gt;**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___RegistryArgs_"></span><span id="smi2smir__diagnosticargs___registryargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___REGISTRYARGS_"></span>**smi2smira &lt; DiagnosticArgs &gt; &lt; RegistryArgs&gt;**
</dt> <dd></dd> <dt>

<span id="smi2smir__HelpArgs__"></span><span id="smi2smir__helpargs__"></span><span id="SMI2SMIR__HELPARGS__"></span>**smi2smira &lt; HelpArgs &gt; "**
</dt> <dd>

Error de sintaxis de la línea de comandos. Esto va seguido de una explicación de los modificadores.

</dd> </dl>

## <a name="fatal-error-102"></a>Error irreales 102

<dl> <dt>

<span id="_102__Fatal___Invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__fatal___invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__FATAL___INVALID_ARGUMENT_ON_COMMAND_LINE_AFTER__LAST_CORRECT_ARGUMENT__"></span>**<102, Error>:"Argumento no válido en la línea de comandos después de <last correct argument> "**
</dt> <dd>

Error de sintaxis de la línea de comandos. Hay algunos argumentos adicionales o un modificador no es válido en la línea de comandos. El parámetro hace referencia al último argumento que se leyó correctamente en la línea de comandos y posiblemente puede ser smi2smira, que es el nombre del archivo ejecutable para el compilador de información del <last correct argument> módulo SNMP.

</dd> </dl>

## <a name="fatal-error-103"></a>Error irreales 103

<dl> <dt>

<span id="_103__Fatal____Diagnostic_Level_not_specified_for_the__m_switch_"></span><span id="_103__fatal____diagnostic_level_not_specified_for_the__m_switch_"></span><span id="_103__FATAL____DIAGNOSTIC_LEVEL_NOT_SPECIFIED_FOR_THE__M_SWITCH_"></span>**<103, Error>: "Nivel de diagnóstico no especificado para el modificador /m"**
</dt> <dd>

Error de sintaxis de la línea de comandos. Si especifica el **modificador /m,** también debe especificar un nivel de diagnóstico de 0, 1 o 2.

</dd> </dl>

## <a name="fatal-error-104"></a>Error irreales 104

<dl> <dt>

<span id="_104__Fatal____Diagnostic_Level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__fatal____diagnostic_level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__FATAL____DIAGNOSTIC_LEVEL_MUST_BE_0__1_OR_2_FOR_THE__M_SWITCH_"></span>**<104, Error>: "El nivel de diagnóstico debe ser 0, 1 o 2 para el modificador /m"**
</dt> <dd>

Error de sintaxis de la línea de comandos. Si especifica el **modificador /m,** también debe especificar un nivel de diagnóstico de 0, 1 o 2.

</dd> </dl>

## <a name="fatal-error-105"></a>Error irreales 105

<dl> <dt>

<span id="_105__Fatal____Maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__fatal____maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__FATAL____MAXIMUM_DIAGNOSTIC_COUNT_MISSING_AFTER_THE__C_SWITCH_"></span>**<105, Error>: "Falta el número máximo de diagnósticos después del modificador /c"**
</dt> <dd>

Error de sintaxis de la línea de comandos. Si especifica el modificador **/c,** también debe especificar un entero no negativo como recuento máximo.

</dd> </dl>

## <a name="fatal-error-106"></a>Error irreales 106

<dl> <dt>

<span id="_106__Fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__FATAL_____ARGUMENT__IS_NOT_A_VALID_DIAGNOSTIC_COUNT_"></span>**<106, Error>: " &lt; el argumento no es un recuento de diagnóstico &gt; válido"**
</dt> <dd>

Error de sintaxis de la línea de comandos. Si especifica el modificador **/c,** también debe especificar un entero no negativo como recuento máximo.

</dd> </dl>

## <a name="fatal-error-107"></a>Error irreales 107

<dl> <dt>

<span id="_107__Fatal____File_Name_s__missing_"></span><span id="_107__fatal____file_name_s__missing_"></span><span id="_107__FATAL____FILE_NAME_S__MISSING_"></span>**<107, Error>: "Faltan nombres de archivo"**
</dt> <dd>

Error semántico de la línea de comandos. Se deben especificar uno o varios nombres de archivo en la línea de comandos para la combinación de modificadores especificada.

</dd> </dl>

## <a name="fatal-error-108"></a>Error irreales 108

<dl> <dt>

<span id="_108__Fatal____No_command_argument_specified_"></span><span id="_108__fatal____no_command_argument_specified_"></span><span id="_108__FATAL____NO_COMMAND_ARGUMENT_SPECIFIED_"></span>**<108, Error>: "No se especificó ningún argumento de comando"**
</dt> <dd>

Error de sintaxis de la línea de comandos. Se debe especificar alguna acción en la línea de comandos.

</dd> </dl>

## <a name="fatal-error-109"></a>Error irreales 109

<dl> <dt>

<span id="_109__Fatal____Module_name_missing_"></span><span id="_109__fatal____module_name_missing_"></span><span id="_109__FATAL____MODULE_NAME_MISSING_"></span>**<109, Error>: "Falta el nombre del módulo"**
</dt> <dd>

Error de sintaxis de la línea de comandos.

</dd> </dl>

## <a name="warning-110"></a>Advertencia 110

<dl> <dt>

<span id="_110__Warning____No_include_path_specified_after_the__i_switch_"></span><span id="_110__warning____no_include_path_specified_after_the__i_switch_"></span><span id="_110__WARNING____NO_INCLUDE_PATH_SPECIFIED_AFTER_THE__I_SWITCH_"></span>**<110, Advertencia>: "No se especificó ninguna ruta de acceso de include después del modificador /i"**
</dt> <dd>

Advertencia de sintaxis de la línea de comandos. Si especifica el modificador **/i,** también debe especificar la ruta de acceso a los archivos incluidos.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno SNMP de WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



