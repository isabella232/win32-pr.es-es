---
description: Describe los errores del proveedor SNMP de WMI de 1071 a 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Errores de 1071 a 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c92cfd1c79b5bedd070229adcbc4c663d209903428073fc976cd575022e9ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679625"
---
# <a name="errors-1071-through-1080"></a>Errores de 1071 a 1080

Describe los errores del proveedor SNMP de WMI de 1071 a 1080.

[Advertencia 1071](#warning-1071)

[Advertencia 1072](#warning-1072)

[Error irresal 1074](#fatal-error-1074)

[Error irreales 1075](#fatal-error-1075)

[Error irresal 1077](#fatal-error-1077)

[Error irreales 1079](#fatal-error-1079)

[Advertencia 1080](#warning-1080)

## <a name="warning-1071"></a>Advertencia 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Advertencia>: "<línea>: Símbolo no <fileName> presente en el módulo importado \# <identifier> <identifier> "**
</dt> <dd>

Advertencia semántica de módulo sobre la referencia cruzada, específica de SNMPv1 ni SNMPv2C. Un símbolo importado de un módulo no se resuelve como nada en ese módulo. Aunque ese módulo se especifica en la entrada, aparece esta advertencia.

</dd> </dl>

## <a name="warning-1072"></a>Advertencia 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Advertencia>: " <fileName> :<línea \#> OBJECT-TYPE es un descendiente <name> de OBJECT-TYPE <name> del módulo <name> "**
</dt> <dd>

Advertencia semántica del módulo de invocación de macro **OBJECT-TYPE.** Un objeto escalar no puede tener ningún objeto descendiente.

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Error irresal 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Error>: " <fileName> :<\# line> SEQUENCE (fila conceptual) OBJECT-TYPE no tiene sequence of <name> (tabla conceptual) OBJECT-TYPE como su elemento primario"**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. Cada objeto de fila debe tener un objeto de tabla como su elemento primario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1075"></a>Error irreales 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:" <fileName> :<line>: OBJECT-TYPE no puede ser un elemento secundario de la tabla OBJECT-TYPE del módulo a menos que esté en la secuencia del \# <name> <name> <name> último"**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. Cada objeto SEQUENCE debe tener exactamente los mismos objetos que se mencionan en la definición de tipo SEQUENCE que sus secundarios. De forma similar, cada objeto SEQUENCE OF debe tener exactamente un elemento secundario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1077"></a>Error irresal 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: " :<line>: La sintaxis de table OBJECT-TYPE no es la secuencia de la sintaxis del <fileName> \# elemento secundario <name> OBJECT-TYPE <name> del módulo <name> "**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. La cláusula de sintaxis de un objeto de tabla debe ser la "SEQUENCE OF" de la sintaxis del objeto de fila.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1079"></a>Error irreales 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line>: OBJECT-TYPE es un elemento secundario adicional de \# <name> OBJECT-TYPE del módulo <name> <name> "**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. Cada objeto SEQUENCE OF debe tener exactamente un elemento secundario.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1080"></a>Advertencia 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Advertencia>: "<línea>: Módulo MIB , desde el que se importa el símbolo, no está presente en la <fileName> \# <moduleName> <symbolName> entrada"**
</dt> <dd>

Advertencia semántica de módulo sobre la referencia cruzada, específica de SNMPv1 ni SNMPv2C. Si uno de los módulos de la sección IMPORTS del módulo principal o un módulo de subsidiaria no existe, pero no se hace referencia a los símbolos de este módulo, aparece esta advertencia.

</dd> </dl>

 

 



