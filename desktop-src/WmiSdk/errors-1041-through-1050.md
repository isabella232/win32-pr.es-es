---
description: Describe los errores del proveedor WMI SNMP de 1041 a 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Errores del 1041 al 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09540249abfed0c8bbf5113ca16f6c1ccbb5d4a913673f628d47ca269f63134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924556"
---
# <a name="errors-1041-through-1050"></a>Errores del 1041 al 1050

Describe los errores del proveedor WMI SNMP de 1041 a 1050.

[Error irreales 1041](#fatal-error-1041)

[Error irreales 1042](#fatal-error-1042)

[Advertencia 1043](#warning-1043)

[Error irreales 1044](#fatal-error-1044)

[Advertencia 1045](#warning-1045)

[Advertencia 1046](#warning-1046)

[Advertencia 1047](#warning-1047)

[Advertencia 1048](#warning-1048)

[Error irreales 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Error irreales 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, error irresal>: "<línea>: el identificador en la especificación del intervalo no se resuelve como <fileName> \# un valor <identifier> entero"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 ni SNMPv2C. El símbolo usado en una especificación SIZE debe resolverse en OCTET STRING o Opaque. Cualquier valor utilizado para especificar un intervalo debe ser un entero.

</dd> </dl>

## <a name="fatal-error-1042"></a>Error irreales 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, error grave>: "<línea>: el límite superior de la especificación del intervalo es menor que el <fileName> \# límite inferior"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 ni SNMPv2C. El símbolo usado en una especificación SIZE debe resolverse en OCTET STRING o Opaque. El límite inferior de un intervalo o especificación SIZE no debe ser mayor que el límite superior.

</dd> </dl>

## <a name="warning-1043"></a>Advertencia 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Advertencia>: " <fileName> :<line \#>: OBJECT-TYPE con SYNTAX "SEQUENCE" debe tener una cláusula ACCESS "no accesible"**
</dt> <dd>

Advertencia semántica del módulo de invocación de macro **OBJECT-TYPE.** Una tabla o fila conceptual (tipos de objeto SEQUENCE OF o SEQUENCE, respectivamente) debe ser "no accesible".

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Error irreales 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, error irresal>: "<<fileName> línea \#>: redefinición del símbolo <identifier> "**
</dt> <dd>

Error semántico del módulo, específico de SNMPv1 ni SNMPv2C. La redefinición de descriptores de objetos, invocaciones de macro y tipos ASN.1 produce un error.

</dd> </dl>

## <a name="warning-1045"></a>Advertencia 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, advertencia>: " <fileName><lineReference to standard symbol <symbolName> assumed to be for the definition as in <moduleName> . Use las notaciones "module.symbol", si desea hacer referencia a la definición en el módulo actual"**
</dt> <dd>

Advertencia semántica del módulo, específica de SNMPv1 ni SNMPv2C. Se ha redefinido un símbolo conocido por el compilador y al que se hace referencia. El compilador asume la definición estándar del símbolo. Por lo tanto, para usar una redefinición del símbolo estándar, debe usar la notación "Module.Symbol".

</dd> </dl>

## <a name="warning-1046"></a>Advertencia 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Advertencia>: "<<fileName> línea \#>: sin <symbol> definir. Suponiendo la definición estándar"**
</dt> <dd>

Advertencia semántica del módulo, específica de SNMPv1 ni SNMPv2C. Un símbolo conocido por el compilador no debe volver a definirse ni usarse sin importarse.

</dd> </dl>

## <a name="warning-1047"></a>Advertencia 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Advertencia>: "<línea>: definición de tipo definida pero no <fileName> \# <symbol> referenciada"**
</dt> <dd>

Advertencia semántica del módulo, específica de SNMPv1 ni SNMPv2C. Se debe hacer referencia a todas las asignaciones de valores y definiciones de tipos en algún lugar.

</dd> </dl>

## <a name="warning-1048"></a>Advertencia 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Advertencia>: "<línea>: Definición de valor definida pero no <fileName> \# <symbol> referenciada"**
</dt> <dd>

Advertencia semántica del módulo, específica de SNMPv1 ni SNMPv2C. Se debe hacer referencia a todas las asignaciones de valores y definiciones de tipos en algún lugar.

</dd> </dl>

## <a name="fatal-error-1049"></a>Error irreales 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Error>: " <fileName> :<line>: Cláusula DEFVAL no permitida para \# OBJECT-TYPE con SYNTAX NetworkAddress"**
</dt> <dd>

**Error semántico** de módulo específico de SNMPv1 de invocación de macro OBJECT-TYPE. No se permite la cláusula DEFVAL para object-type cuya cláusula SYNTAX se resuelve en NetworkAddress.

</dd> </dl>

 

 



