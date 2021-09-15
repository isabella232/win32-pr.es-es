---
description: Describe los errores del proveedor SNMP de WMI de 1081 a 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Errores del 1081 al 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ce7b1a8c575067fe2231108e0d314af2f8dc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476113"
---
# <a name="errors-1081-through-1090"></a>Errores del 1081 al 1090

Describe los errores del proveedor SNMP de WMI de 1081 a 1090.

[Error irresal 1081](#fatal-error-1081)

[Error irrecuperable 1082](#fatal-error-1082)

[Error irresal 1084](#fatal-error-1084)

[Advertencia 1085](#warning-1085)

[Advertencia 1086](#warning-1086)

[Error irresal 1087](#fatal-error-1087)

[Error irresal 1089](#fatal-error-1089)

[Error irreales 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Error irresal 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Error>: " &lt; fileName &gt; line>: Identificador de símbolo no presente en \# el identificador de módulo importado &lt; &gt; &lt; &gt; "**
</dt> <dd>

Error semántico del módulo en la referencia cruzada, específico de SNMPv1 ni SNMPv2C. Un símbolo importado de un módulo no se resuelve como nada en ese módulo. Si realmente se hace referencia a ese símbolo en el MIB, se produce este error.

</dd> </dl>

## <a name="fatal-error-1082"></a>Error irrecuperable 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Cláusula>: " &lt; fileName &gt; :<line \#>: Cláusula STATUS &lt; no válida &gt; "**
</dt> <dd>

**Invocación de macro OBJECT-IDENTITY,** error semántico de módulo específico de SNMPv2C. La cláusula STATUS de una invocación **OBJECT-IDENTITY** debe ser "actual", "en desuso" u "obsoleta".

</dd> </dl>

## <a name="fatal-error-1084"></a>Error irresal 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Error>: "fileName><line \#>: MODULE-IDENTITY required after the IMPORTS section for all SNMPv2 modules"**
</dt> <dd>

**Invocación de macro MODULE-IDENTITY,** error semántico de módulo específico de SNMPv2C. Debe haber una única invocación **MODULE-IDENTITY** en una MIB SNMPv2C, inmediatamente después de la sección IMPORTS.

</dd> </dl>

## <a name="warning-1085"></a>Advertencia 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Advertencia>: " &lt; fileName &gt;<línea \#>: No se &lt; encontraron grupos en el nombre del módulo &gt; . No se pudo inventar MODULE-IDENTITY. Se producirá un error al intentar cargar el módulo en SMIR"**
</dt> <dd>

Advertencia específica de SNMPv1 semántica del módulo. Este error se genera si no se encuentra ningún grupo de objetos en un módulo.

</dd> </dl>

## <a name="warning-1086"></a>Advertencia 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Advertencia>: " &lt; fileName &gt;<línea \#>: No &lt; se encontraron grupos en el nombre del módulo &gt; "**
</dt> <dd>

Advertencia específica de SNMPv1 semántica del módulo. Este error se genera si no se encuentra ningún grupo de objetos en un módulo.

</dd> </dl>

## <a name="fatal-error-1087"></a>Error irresal 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Error>: " fileName<line>: Cláusula STATUS no válida &lt; &gt; para una macro \# &lt; &gt; TEXTUAL-CONVENTION"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. La cláusula status de una invocación de macro **TEXTUAL-CONVENTION** debe ser "actual", "en desuso" o "obsoleta".

</dd> </dl>

## <a name="fatal-error-1089"></a>Error irresal 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Error>: " fileName :<line>: El identificador de símbolo de la cláusula AUGMENTS no se resuelve en una fila &lt; &gt; \# &lt; &gt; OBJECT-TYPE"**
</dt> <dd>

**Error semántico de** módulo específico de SNMPv2C de invocación de macro OBJECT-TYPE. Si hay una cláusula AUGMENTS, el identificador de la cláusula AUGMENTS debe resolverse en una tabla OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1090"></a>Error irresal 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Error>: " fileName :<line> la cláusula IMPLIED solo es útil para el último &lt; &gt; objeto \# INDEX"**
</dt> <dd>

**Error semántico de** módulo específico de SNMPv2C de invocación de macro OBJECT-TYPE. La cláusula IMPLIED solo se puede asociar al último objeto de la cláusula INDEX.

</dd> </dl>

 

 



