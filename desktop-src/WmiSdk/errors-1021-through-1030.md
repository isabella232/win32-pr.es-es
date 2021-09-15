---
description: Describe los errores del proveedor SNMP de WMI de 1021 a 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Errores de 1021 a 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b7b7c914354e1865d8f3da47f076ddd785a7ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270324"
---
# <a name="errors-1021-through-1030"></a>Errores de 1021 a 1030

Describe los errores del proveedor SNMP de WMI de 1021 a 1033.

[Error irreales 1021](#fatal-error-1021)

[Error irresal 1022](#fatal-error-1022)

[Error irreales 1023](#fatal-error-1023)

[Error irresal 1024](#fatal-error-1024)

[Error irresal 1025](#fatal-error-1025)

[Error irreales 1026](#fatal-error-1026)

[Advertencia 1027](#warning-1027)

[Error irresal 1028](#fatal-error-1028)

[Error irresal 1029](#fatal-error-1029)

[Error irresal 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Error irreales 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Error>: " &lt; fileName &gt;<line \#>: Identifier &lt; identifier &gt; in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**
</dt> <dd>

**Invocación de macro TRAP-TYPE,** error semántico de módulo específico de SNMPv1. Cada elemento de la lista de variables usadas en la cláusula VARIABLES de una invocación de macro **TRAP-TYPE** debe resolverse como el nombre de una instancia de OBJECT-TYPE escalar.

</dd> </dl>

## <a name="fatal-error-1022"></a>Error irresal 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Error>: " &lt; fileName &gt;<línea \#>: El &lt; valor no se resuelve en el tipo &gt; "**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico de SNMPv1 ni SNMPv2C. El valor de RHS de una asignación de valores INTEGER, **NULL,** OCTET STRING o OBJECT IDENTIFIER es del tipo incorrecto.

</dd> </dl>

## <a name="fatal-error-1023"></a>Error irresal 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Error>: " &lt; fileName &gt;<línea \#>: El &lt; &gt; &lt; identificador &gt; de identificador no se resuelve en el identificador de tipo "**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico de SNMPv1 ni SNMPv2C. Un símbolo (referencia de valor) en el RHS de una asignación de valores INTEGER, **NULL,** OCTET STRING o OBJECT IDENTIFIER no se resuelve en el tipo correcto.

</dd> </dl>

## <a name="fatal-error-1024"></a>Error irreales 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Error>: " fileName<línea>: Entero negativo en la definición de valor &lt; &gt; de \# OID"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico de SNMPv1 ni SNMPv2C. Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).

</dd> </dl>

## <a name="fatal-error-1025"></a>Error irresal 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Error>: "Identificador de identificador en el valor de OID no se resuelve &lt; &gt; como un entero positivo"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico de SNMPv1 ni SNMPv2C. Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).

</dd> </dl>

## <a name="fatal-error-1026"></a>Error irreales 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Error>: &lt; "fileName &gt;<line \#>: Identifier identifier &lt; &gt; in OID value neither resolves to an OID value nor a positive integer"**
</dt> <dd>

Error semántico del módulo de asignación de valores, específico de SNMPv1 ni SNMPv2C. El primer componente utilizado en un valor de OID debe resolverse como un valor OID o integer.

</dd> </dl>

## <a name="warning-1027"></a>Advertencia 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Advertencia>: " fileName<línea>: Identificador de símbolo importado &lt; &gt; sin \# &lt; &gt; usar"**
</dt> <dd>

Advertencia semántica del módulo de sección IMPORTS, específica de SNMPv1 ni SNMPv2C. Se emite una advertencia para cada símbolo importado sin usar.

</dd> </dl>

## <a name="fatal-error-1028"></a>Error irresal 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Error>: "Identificador de módulo &lt; no importado en la sección &gt; IMPORTS"**
</dt> <dd>

Error semántico del módulo de sección IMPORTS, específico de SNMPv1 ni SNMPv2C. Un nombre de módulo utilizado para hacer referencia a un símbolo debe estar presente en la cláusula IMPORTS o ser el nombre del módulo actual.

</dd> </dl>

## <a name="fatal-error-1029"></a>Error irresal 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Error>: " &lt; fileName<línea>: No se puede importar el identificador &gt; \# del módulo &lt; &gt; actual"**
</dt> <dd>

Error semántico del módulo de sección IMPORTS, específico de SNMPv1 ni SNMPv2C. El nombre del módulo actual también figura en la lista IMPORTS.

</dd> </dl>

## <a name="fatal-error-1030"></a>Error irreales 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Nombre de archivo>:"<línea>: Identificador de símbolo no importado desde el identificador &lt; &gt; de módulo \# &lt; &gt; &lt; &gt; "**
</dt> <dd>

Error semántico del módulo de sección IMPORTS, específico de SNMPv1 ni SNMPv2C. Ha usado la notación "Module.Symbol", pero el símbolo no se ha importado desde el módulo especificado en la sección IMPORTS.

</dd> </dl>

 

 



