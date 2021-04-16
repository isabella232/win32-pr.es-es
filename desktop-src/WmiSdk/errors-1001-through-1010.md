---
description: Describe los errores del proveedor SNMP de WMI de 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Errores de 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716205"
---
# <a name="errors-1001-through-1010"></a>Errores de 1001 a 1010

Describe los errores del proveedor SNMP de WMI de 1001 a 1010.

[Error irrecuperable 1001](#fatal-error-1001)

[Error irrecuperable 1002](#fatal-error-1002)

[Error irrecuperable 1003](#fatal-error-1003)

[ADVERTENCIA 1004](#warning-1004)

[ADVERTENCIA 1005](#warning-1005)

[Error irrecuperable 1006](#fatal-error-1006)

[Error irrecuperable 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Error irrecuperable 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> irrecuperable: " <fileName> : <línea \#>: la cláusula Syntax de tipo Object no se resuelve como tipos permitidos"
</dt> <dd>

Error semántico del módulo de invocación de macros de tipo de objeto. La cláusula de sintaxis de la macro OBJECT-TYPE debe resolverse en un tipo o subtipo, formado mediante la especificación de tamaño o intervalo que permite la SMI de SNMPv1 o SNMPv2C. Si no es así, se muestra el error irrecuperable 1001.

Este error puede producirse al compilar una MIB de SNMPv1 o SNMPv2C.

Los tipos permitidos por la SMI de SNMPv1 son:

-   INTEGER
-   NULL
-   CADENA DE OCTETO
-   IDENTIFICADOR DE OBJETO
-   NetworkAddress
-   IpAddress
-   Contador
-   Indicador
-   TimeTicks
-   Opaca
-   DisplayString
-   PhysAddress

Los tipos permitidos por la SMI de SNMPv2C son:

-   INTEGER
-   CADENA DE OCTETO
-   IDENTIFICADOR DE OBJETO
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Opaca
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   TruthValue
-   TestAndIncr
-   AutonomousType
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>Error irrecuperable 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> irrecuperable: " <fileName> : <de línea \#>: cláusula de acceso no válida <clause> "
</dt> <dd>

Error semántico del módulo de invocación de macros de tipo de objeto. Para SNMPv1, la cláusula de acceso de la macro del tipo de objeto debe ser "de solo lectura", "solo escritura", "lectura/escritura" o "no accesible".

Para SNMPv2C, la cláusula MAX-ACCESS debe ser "de solo lectura", "lectura y creación", "lectura/escritura" o "no accesible".

</dd> </dl>

## <a name="fatal-error-1003"></a>Error irrecuperable 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> irrecuperable: " <fileName> : <línea \#>: cláusula de estado no válida <clause> "
</dt> <dd>

Error semántico del módulo de invocación de macros de tipo de objeto. Para SNMPv1, la cláusula de estado de una invocación de macro de tipo de objeto debe ser "obligatoria", "opcional", "obsoleto" o "desusado".

Para SNMPv2C, la cláusula de estado de una invocación de macro de tipo de objeto debe ser "actual", "en desuso" o "obsoleto".

</dd> </dl>

## <a name="warning-1004"></a>ADVERTENCIA 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, ADVERTENCIA>: " <fileName> : <línea \#>: Object-Type <identifier> , cuya sintaxis se resuelve como uno de los tipos de contador no termina con la ' ' de la letra
</dt> <dd>

ADVERTENCIA semántica del módulo de invocación de macros de tipo de objeto. El identificador de un objeto de contador de sintaxis (SNMPv1) o Counter32 y Counter64 (SNMPv2C) debe ser plural.

Esta advertencia puede producirse al compilar una MIB de SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>ADVERTENCIA 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, ADVERTENCIA>: " <fileName> : <línea \#>: tipo de objeto con la sintaxis" secuencia de ", debe tener una cláusula de acceso" no accesible ".
</dt> <dd>

ADVERTENCIA semántica del módulo de invocación de macros de tipo de objeto. Una tabla o fila conceptual (secuencia de tipos de objeto de secuencia o, respectivamente) debe ser "no accesible".

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Error irrecuperable 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> irrecuperable: " <fileName> : <de línea \#> tipo de objeto <identifier> , que es la secuencia de sintaxis, no tiene una cláusula index o aumenta"
</dt> <dd>

Error semántico del módulo de invocación de macros de tipo de objeto. Para SNMPv1, la cláusula INDEX debe estar presente para una definición de tipo de objeto cuya sintaxis se resuelva como un tipo de secuencia.

Para SNMPv2C, el índice o la cláusula de AUMENTOs deben estar presentes para una declaración de fila conceptual.

</dd> </dl>

## <a name="fatal-error-1008"></a>Error irrecuperable 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> irrecuperable: " <fileName> : <línea \#>: <identifier> no se ha hecho referencia a un tipo de objeto, que es de sintaxis" Sequence ".
</dt> <dd>

Error semántico del módulo de invocación de macros de tipo de objeto. Un tipo de objeto con la cláusula de sintaxis como un tipo de secuencia debe figurar en la cláusula de sintaxis de exactamente una invocación de tipo de objeto que representa una declaración de tabla, es decir, un objeto con la cláusula de sintaxis como una secuencia de tipo. El \# parámetro> de línea de <hace referencia al segundo punto de referencia.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



