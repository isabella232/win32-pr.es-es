---
description: Describe los errores del proveedor SNMP de WMI de 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errores de 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697472"
---
# <a name="errors-1051-through-1060"></a>Errores de 1051 a 1060

Describe los errores del proveedor SNMP de WMI de 1051 a 1060.

[Error irrecuperable 1051](#fatal-error-1051)

[Error irrecuperable 1054](#fatal-error-1054)

[Error irrecuperable 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Error irrecuperable 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> irrecuperable: " <fileName> : <línea \#>: referencia ambigua al símbolo <identifier> "**
</dt> <dd>

Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C. Cada descriptor de objeto que corresponde a un objeto en una MIB estándar de Internet debe ser único. Dado que las MIB empresariales pueden tener descriptores de objeto comunes, estos descriptores importados de dos módulos deben usarse sin ambigüedades en el módulo MIB mediante el uso de la notación "module. descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Error irrecuperable 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> grave: " <fileName> : <línea \#>: <identifier> en la cláusula index no se resuelve como uno de los tipos permitidos"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, una secuencia sin secuencia o no de tipo. Cualquier tipo especificado en la cláusula INDEX también debe resolverse en uno de ellos.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Error irrecuperable 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> irrecuperable: " <fileName> : <línea \#>: la sintaxis de tipo de objeto de índice <identifier> no se resuelve como uno de los tipos permitidos"**
</dt> <dd>

Error semántico del módulo de invocación de macros **de tipo de objeto** . El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, una secuencia sin secuencia o no de tipo.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



