---
description: Describe los errores del proveedor SNMP de WMI de 1041 a 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Errores de 1041 a 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082446"
---
# <a name="errors-1041-through-1050"></a>Errores de 1041 a 1050

Describe los errores del proveedor SNMP de WMI de 1041 a 1050.

[Error irrecuperable 1041](#fatal-error-1041)

[Error irrecuperable 1042](#fatal-error-1042)

[ADVERTENCIA 1043](#warning-1043)

[Error irrecuperable 1044](#fatal-error-1044)

[ADVERTENCIA 1045](#warning-1045)

[ADVERTENCIA 1046](#warning-1046)

[ADVERTENCIA 1047](#warning-1047)

[ADVERTENCIA 1048](#warning-1048)

[Error irrecuperable 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Error irrecuperable 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041,> grave: " <fileName><\#> de línea: el identificador <identifier> de la especificación de intervalo no se resuelve como un valor entero"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 o SNMPv2C. El símbolo que se usa en una especificación de tamaño debe resolverse como una cadena de octeto o opaca. Cualquier valor usado en la especificación de un intervalo debe ser un entero.

</dd> </dl>

## <a name="fatal-error-1042"></a>Error irrecuperable 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042,> grave: " <fileName><línea \#>: el límite superior de la especificación del intervalo es menor que el límite inferior"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 o SNMPv2C. El símbolo que se usa en una especificación de tamaño debe resolverse como una cadena de octeto o opaca. El límite inferior de una especificación de intervalo o de tamaño no debe ser mayor que el límite superior.

</dd> </dl>

## <a name="warning-1043"></a>ADVERTENCIA 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, ADVERTENCIA>: " <fileName> : <línea \#>: el tipo de objeto con la sintaxis" Sequence "debe tener una cláusula de acceso" no accesible "**
</dt> <dd>

ADVERTENCIA semántica del módulo de invocación de macros **de tipo de objeto** . Una tabla o fila conceptual (secuencia de tipos de objeto de secuencia o, respectivamente) debe ser "no accesible".

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Error irrecuperable 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044,> grave: " <fileName><línea \#>: redefinición del símbolo <identifier> "**
</dt> <dd>

Error semántico del módulo, específico no es SNMPv1 ni SNMPv2C. La nueva definición de los descriptores de objeto, las invocaciones de macros y los tipos ASN. 1 producen un error.

</dd> </dl>

## <a name="warning-1045"></a>ADVERTENCIA 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, ADVERTENCIA>: " <fileName><lineReference al símbolo estándar <symbolName> se supone que es para la definición como en <moduleName> . Use las notaciones "module. Symbol" Si desea hacer referencia a la definición del módulo actual "**
</dt> <dd>

ADVERTENCIA semántica del módulo, específica de no SNMPv1 ni SNMPv2C. Se ha redefinido un símbolo conocido por el compilador y se hace referencia a él. El compilador asume la definición estándar del símbolo. Por lo tanto, para usar una nueva definición del símbolo estándar, debe usar la notación "module. Symbol".

</dd> </dl>

## <a name="warning-1046"></a>ADVERTENCIA 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, ADVERTENCIA>: " <fileName><> de línea \# : <symbol> sin definir. Suponiendo la definición estándar "**
</dt> <dd>

ADVERTENCIA semántica del módulo, específica de no SNMPv1 ni SNMPv2C. Un símbolo conocido por el compilador no debe volver a definirse ni usarse sin importarse.

</dd> </dl>

## <a name="warning-1047"></a>ADVERTENCIA 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, ADVERTENCIA>: " <fileName><> de línea \# : definición de tipo <symbol> definida pero sin referencia"**
</dt> <dd>

ADVERTENCIA semántica del módulo, específica de no SNMPv1 ni SNMPv2C. Se debe hacer referencia a todas las asignaciones de valores y definiciones de tipo en alguna parte.

</dd> </dl>

## <a name="warning-1048"></a>ADVERTENCIA 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, ADVERTENCIA>: " <fileName><de línea \#>: definición de valor <symbol> definida pero no se hace referencia a ella"**
</dt> <dd>

ADVERTENCIA semántica del módulo, específica de no SNMPv1 ni SNMPv2C. Se debe hacer referencia a todas las asignaciones de valores y definiciones de tipo en alguna parte.

</dd> </dl>

## <a name="fatal-error-1049"></a>Error irrecuperable 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049,> irrecuperable: " <fileName> : <\# de línea>: no se permite la cláusula DEFVAL para el tipo de objeto con la sintaxis NetworkAddress"**
</dt> <dd>

Error semántico del módulo específico de **la llamada a la macro de tipo de objeto** SNMPv1. No se permite la cláusula DEFVAL para un tipo de objeto cuya cláusula de sintaxis se resuelve en NetworkAddress.

</dd> </dl>

 

 



