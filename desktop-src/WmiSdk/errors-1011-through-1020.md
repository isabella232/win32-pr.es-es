---
description: Describe los errores del proveedor SNMP de WMI de 1011 a 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Errores de 1011 a 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083135"
---
# <a name="errors-1011-through-1020"></a>Errores de 1011 a 1020

Describe los errores del proveedor SNMP de WMI de 1011 a 1020.

[Error irrecuperable 1011](#fatal-error-1011)

[Error irrecuperable 1012](#fatal-error-1012)

[Error irrecuperable 1013](#fatal-error-1013)

[ADVERTENCIA 1014](#warning-1014)

[Error irrecuperable 1015](#fatal-error-1015)

[Error irrecuperable 1016](#fatal-error-1016)

[Error irrecuperable 1018](#fatal-error-1018)

[Error irrecuperable 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Error irrecuperable 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011,> grave: " <fileName> : <línea \#> la sintaxis del miembro <identifier> de Sequence, <identifier> , difiere de la cláusula de sintaxis del tipo de objeto"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Un elemento de una secuencia debe ser el mismo que el tipo de la cláusula de sintaxis de la definición de tipo de objeto. La línea \# de <> parámetro es la línea de la cláusula de sintaxis de la definición de tipo de objeto.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1012"></a>Error irrecuperable 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012,> grave: " <fileName> : <línea \#> solo se requiere una cláusula index o increments para los tipos de objeto de secuencia"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Una cláusula INDEX solo debe estar presente en una definición de tipo de objeto cuya sintaxis se resuelva como un tipo de secuencia.

Este error puede producirse al compilar una MIB de SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1013"></a>Error irrecuperable 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013,> grave: " <fileName><> de línea \# : <identifier> debe resolverse en un tipo de secuencia"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Un tipo que se usa en la construcción "SEQUENCE OF" debe resolverse en un tipo de secuencia.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1014"></a>ADVERTENCIA 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, ADVERTENCIA>: " <fileName> : <línea \#>: no se recomienda el subidentificador del valor 0 en OID"**
</dt> <dd>

ADVERTENCIA semántica del módulo de invocación de macros **de tipo de objeto** . Se recomienda que ningún objeto de una MIB estándar de Internet use un subidentificador de cero en su identificador de objeto.

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1015"></a>Error irrecuperable 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015,> grave: " <fileName> : <línea \#>: OBJECT-TYPEs <identifier> del módulo <identifier> y <identifier> del módulo <identifier> se les asignan los mismos valores de OID"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Dos invocaciones de **tipo de objeto** (en el mismo módulo o en módulos diferentes) no deben tener asignado el mismo valor de identificador de objeto.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1016"></a>Error irrecuperable 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016,> irrecuperable: " <fileName> : <línea \#>: el valor de la cláusula DEFVAL no coincide con el tipo de la cláusula de sintaxis"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Un valor de una cláusula DEFVAL debe ser un valor del tipo mencionado en la cláusula SYNTAX.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1018"></a>Error irrecuperable 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018,> grave: " <fileName><\#> de línea: <symbol> en la cláusula Enterprise de Trap-Type no se resuelve como un valor OID"**
</dt> <dd>

Invocación de macros **de tipo de captura** , error semántico del módulo específico de SNMPv1. El símbolo que se usa en la cláusula ENTERPRISE de una invocación de macro de **tipo Trap** debe resolverse en un valor de identificador de objeto.

</dd> </dl>

## <a name="fatal-error-1020"></a>Error irrecuperable 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020,> grave: " <fileName><> de línea \# : el valor asignado a Trap-Type no <identifier> se resuelve como un entero positivo"**
</dt> <dd>

Invocación de macros **de tipo de captura** , error semántico del módulo específico de SNMPv1. Un símbolo que se usa para especificar el valor de la captura no se resuelve como un entero positivo.

</dd> </dl>

 

 



