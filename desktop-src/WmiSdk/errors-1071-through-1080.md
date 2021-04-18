---
description: Describe los errores del proveedor SNMP de WMI de 1071 a 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Errores de 1071 a 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707407"
---
# <a name="errors-1071-through-1080"></a>Errores de 1071 a 1080

Describe los errores del proveedor SNMP de WMI de 1071 a 1080.

[ADVERTENCIA 1071](#warning-1071)

[ADVERTENCIA 1072](#warning-1072)

[Error irrecuperable 1074](#fatal-error-1074)

[Error irrecuperable 1075](#fatal-error-1075)

[Error irrecuperable 1077](#fatal-error-1077)

[Error irrecuperable 1079](#fatal-error-1079)

[ADVERTENCIA 1080](#warning-1080)

## <a name="warning-1071"></a>ADVERTENCIA 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, ADVERTENCIA>: " <fileName><\#> de línea: el símbolo <identifier> no está presente en el módulo importado <identifier> "**
</dt> <dd>

ADVERTENCIA semántica del módulo sobre la referencia cruzada, específica no es SNMPv1 ni SNMPv2C. Un símbolo importado de un módulo no se resuelve en ningún elemento de ese módulo. Aunque ese módulo se especifica en la entrada, aparece esta advertencia.

</dd> </dl>

## <a name="warning-1072"></a>ADVERTENCIA 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, ADVERTENCIA>: " <fileName> : <línea \#> objeto-tipo <name> es un descendiente del tipo de objeto <name> del módulo <name> "**
</dt> <dd>

ADVERTENCIA semántica del módulo de invocación de macros **de tipo de objeto** . Un objeto escalar no puede tener objetos descendientes.

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Error irrecuperable 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074,> grave: " <fileName> : <\# secuencia de> de línea (fila conceptual): el tipo de objeto <name> no tiene una secuencia de tipo de objeto (tabla conceptual) como su elemento primario"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Cada objeto de fila debe tener un objeto de tabla como su elemento primario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1075"></a>Error irrecuperable 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075,> irrecuperable: " <fileName> : <\# de línea>: el tipo de objeto <name> no puede ser un elemento secundario del tipo <name> de objeto de tabla del módulo <name> a menos que esté en la secuencia de la última"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Cada objeto de secuencia debe tener exactamente los mismos objetos que se mencionan en la definición del tipo de secuencia como sus elementos secundarios. DE igual forma, cada secuencia de objeto debe tener exactamente un elemento secundario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1077"></a>Error irrecuperable 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077,> irrecuperable: " <fileName> : <línea \#>: la sintaxis de Table Object-Type <name> no es la secuencia de la sintaxis del objeto secundario-Type <name> del módulo <name> "**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . La cláusula de sintaxis de un objeto Table debe ser la "secuencia de" de la sintaxis del objeto Row.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1079"></a>Error irrecuperable 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079,> grave: "fileName>: <line \#>: Object-Type <name> es un elemento secundario adicional de Object-Type <name> de Module <name> "**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . Cada secuencia de objeto debe tener exactamente un elemento secundario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1080"></a>ADVERTENCIA 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, ADVERTENCIA>: " <fileName><línea \#>: módulo MIB <moduleName> , desde el que <symbolName> se importa el símbolo, no está presente en la entrada"**
</dt> <dd>

ADVERTENCIA semántica del módulo sobre la referencia cruzada, específica no es SNMPv1 ni SNMPv2C. Si uno de los módulos de la sección IMPORTAciones del módulo principal o de un módulo subsidiario no existe, pero no se hace referencia a los símbolos de este módulo, se muestra esta advertencia.

</dd> </dl>

 

 



