---
description: Describe los errores del proveedor SNMP de WMI de 1081 a 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Errores de 1081 a 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687314"
---
# <a name="errors-1081-through-1090"></a>Errores de 1081 a 1090

Describe los errores del proveedor SNMP de WMI de 1081 a 1090.

[Error irrecuperable 1081](#fatal-error-1081)

[Error irrecuperable 1082](#fatal-error-1082)

[Error irrecuperable 1084](#fatal-error-1084)

[ADVERTENCIA 1085](#warning-1085)

[ADVERTENCIA 1086](#warning-1086)

[Error irrecuperable 1087](#fatal-error-1087)

[Error irrecuperable 1089](#fatal-error-1089)

[Error irrecuperable 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Error irrecuperable 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081,> irrecuperable: " <fileName> línea \#>: símbolo <identifier> no presente en el módulo importado <identifier> "**
</dt> <dd>

Error semántico del módulo en referencias cruzadas, específicas de SNMPv1 o SNMPv2C. Un símbolo importado de un módulo no se resuelve en ningún elemento de ese módulo. Si se hace referencia realmente a ese símbolo en la MIB, se produce este error.

</dd> </dl>

## <a name="fatal-error-1082"></a>Error irrecuperable 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082,> irrecuperable: " <fileName> : <línea \#>: cláusula de estado no válida <clause> "**
</dt> <dd>

Invocación de macro **de objeto-identidad** , error semántico del módulo específico de SNMPv2c. La cláusula de estado de una invocación de **objeto-identidad** debe ser "actual", "en desuso" o "obsoleto".

</dd> </dl>

## <a name="fatal-error-1084"></a>Error irrecuperable 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084,> grave: "fileName><line \#>: module-Identity required After the IMports for All SNMPv2 modules"**
</dt> <dd>

Error de la invocación de macros **de la identidad de módulo** y de SNMPv2c. Solo debe haber una invocación de **identidad de módulo** en una MIB de SNMPv2c, inmediatamente después de la sección Imports.

</dd> </dl>

## <a name="warning-1085"></a>ADVERTENCIA 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, ADVERTENCIA>: " <fileName><\#> de línea: no se encontraron grupos en el módulo <name> . No se pudo fabricar MODULE-IDENTITY. Se producirá un error al intentar cargar el módulo en el SMIR**
</dt> <dd>

ADVERTENCIA relativa a la semántica de un módulo de SNMPv1. Este error se genera si no se encuentra ningún grupo de objetos en un módulo.

</dd> </dl>

## <a name="warning-1086"></a>ADVERTENCIA 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, ADVERTENCIA>: " <fileName><\#> de línea: no se encontraron grupos en el módulo <name> "**
</dt> <dd>

ADVERTENCIA relativa a la semántica de un módulo de SNMPv1. Este error se genera si no se encuentra ningún grupo de objetos en un módulo.

</dd> </dl>

## <a name="fatal-error-1087"></a>Error irrecuperable 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087.> irrecuperable: " <fileName><\# de línea>: cláusula de estado no válida <clause> para una macro de Convención de texto"**
</dt> <dd>

Asignación de tipos, error semántico del módulo específico de SNMPv2C. La cláusula de estado de una invocación de macro de **Convención de texto** debe ser "actual", "en desuso" o "obsoleta".

</dd> </dl>

## <a name="fatal-error-1089"></a>Error irrecuperable 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, fatal>: " <fileName> : <línea \#>: el símbolo <identifier> en la cláusula increments no se resuelve como un tipo de objeto de fila"**
</dt> <dd>

Error semántico del módulo específico de la invocación de macro de **tipo de objeto** SNMPv2c. Si hay una cláusula de AUMENTOs, el identificador de la cláusula de AUMENTOs debe resolverse en un tipo de objeto de tabla.

</dd> </dl>

## <a name="fatal-error-1090"></a>Error irrecuperable 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090,> grave: " <fileName> : <línea \#> cláusula implícita solo es útil para el último objeto de índice"**
</dt> <dd>

Error semántico del módulo específico de la invocación de macro de **tipo de objeto** SNMPv2c. La cláusula implícita solo se puede asociar con el último objeto de la cláusula INDEX.

</dd> </dl>

 

 



