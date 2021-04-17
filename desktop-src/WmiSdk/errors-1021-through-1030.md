---
description: Describe los errores del proveedor SNMP de WMI de 1021 a 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Errores de 1021 a 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666877"
---
# <a name="errors-1021-through-1030"></a>Errores de 1021 a 1030

Describe los errores del proveedor SNMP de WMI de 1021 a 1033.

[Error irrecuperable 1021](#fatal-error-1021)

[Error irrecuperable 1022](#fatal-error-1022)

[Error irrecuperable 1023](#fatal-error-1023)

[Error irrecuperable 1024](#fatal-error-1024)

[Error irrecuperable 1025](#fatal-error-1025)

[Error irrecuperable 1026](#fatal-error-1026)

[ADVERTENCIA 1027](#warning-1027)

[Error irrecuperable 1028](#fatal-error-1028)

[Error irrecuperable 1029](#fatal-error-1029)

[Error irrecuperable 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Error irrecuperable 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> grave: " <fileName><> de línea \# : <identifier> el identificador de la cláusula variables de Trap-Type no se resuelve como un tipo de objeto escalar"**
</dt> <dd>

Invocación de macros **de tipo de captura** , error semántico del módulo específico de SNMPv1. Cada elemento de la lista de variables utilizada en la cláusula VARIABLES de una invocación de macro de **tipo Trap** debe resolverse en el nombre de una instancia de tipo de objeto escalar.

</dd> </dl>

## <a name="fatal-error-1022"></a>Error irrecuperable 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> grave: " <fileName><\#> de línea: el valor no se resuelve en el tipo <type> "**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C. El valor de la RHS de un entero, un valor **null**, una cadena de octeto o una asignación de valores de identificador de objeto es de un tipo incorrecto.

</dd> </dl>

## <a name="fatal-error-1023"></a>Error irrecuperable 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> grave: " <fileName><\#> de línea: <identifier> el identificador no se resuelve como el tipo <identifier> "**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C. Un símbolo (referencia de valor) en el RHS de un entero, un valor **null**, una cadena de octeto o una asignación de valores de identificador de objeto no se resuelve en el tipo correcto.

</dd> </dl>

## <a name="fatal-error-1024"></a>Error irrecuperable 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> grave: " <fileName><\#> de línea: entero negativo en la definición del valor de OID"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C. Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).

</dd> </dl>

## <a name="fatal-error-1025"></a>Error irrecuperable 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> grave: "el identificador <identifier> del valor de OID no se resuelve como un entero positivo"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C. Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).

</dd> </dl>

## <a name="fatal-error-1026"></a>Error irrecuperable 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> grave: " <fileName><\#> de línea: <identifier> el identificador en el valor OID no se resuelve como un valor OID ni un entero positivo"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C. El primer componente que se usa en un valor de OID debe resolverse en un valor de OID o un entero.

</dd> </dl>

## <a name="warning-1027"></a>ADVERTENCIA 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, ADVERTENCIA>: " <fileName><> de línea \# : símbolo importado <identifier> sin usar"**
</dt> <dd>

La sección de IMPORTAciones de la advertencia semántica del módulo, específica no es SNMPv1 ni SNMPv2C. Se emite una advertencia por cada símbolo importado sin usar.

</dd> </dl>

## <a name="fatal-error-1028"></a>Error irrecuperable 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> irrecuperable: "módulo <identifier> no importado en la sección de importaciones"**
</dt> <dd>

Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C. Un nombre de módulo que se usa para hacer referencia a un símbolo debe estar presente en la cláusula Imports o ser el nombre del módulo actual.

</dd> </dl>

## <a name="fatal-error-1029"></a>Error irrecuperable 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> grave: " <fileName><> de línea \# : el módulo actual <identifier> no se puede importar"**
</dt> <dd>

Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C. El nombre del módulo actual también se muestra en la lista de IMPORTAciones.

</dd> </dl>

## <a name="fatal-error-1030"></a>Error irrecuperable 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> grave: " <fileName><\#> de línea: símbolo <identifier> no importado desde el módulo <identifier> "**
</dt> <dd>

Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C. Ha usado la notación "module. Symbol", pero el símbolo no se ha importado desde el módulo especificado en la sección Imports.

</dd> </dl>

 

 



