---
description: Describe los errores del proveedor WMI SNMP de 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errores de 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3405a799d71b33fa1dabd7c84964b8d1726d2e27
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882584"
---
# <a name="errors-1051-through-1060"></a>Errores de 1051 a 1060

Describe los errores del proveedor WMI SNMP de 1051 a 1060.

[Error irresal 1051](#fatal-error-1051)

[Error irresal 1054](#fatal-error-1054)

[Error irresal 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Error irreales 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Error irresperante>: " &lt; fileName &gt; :<line \#>: Referencia &lt; ambigua al identificador de símbolos &gt; "**
</dt> <dd>

Error semántico del módulo de sección IMPORTS, específico de SNMPv1 ni SNMPv2C. Cada descriptor de objeto correspondiente a un objeto en una MIB estándar de Internet debe ser único. Dado que las MIB empresariales pueden tener descriptores de objetos comunes, estos descriptores importados desde dos módulos deben usarse de forma inequívoca en el módulo MIB mediante la notación "module.descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Error irresal 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: " &lt; fileName &gt; :<line \#>: identifier in INDEX clause does &lt; not resolve to one of the allowed &gt; types"**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, un tipo que no sea SEQUENCE o que no sea SEQUENCE OF. Cualquier tipo especificado en la cláusula INDEX también debe resolverse en uno de estos.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Error irresal 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:" &lt; fileName &gt; :<line \#>: SYNTAX of INDEX OBJECT-TYPE &lt; identifier , does not resolve to one of the allowed &gt; types"**
</dt> <dd>

**Error semántico del** módulo de invocación de macro OBJECT-TYPE. El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, un tipo que no sea SEQUENCE o que no sea SEQUENCE OF.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



