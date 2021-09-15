---
description: Describe los errores del proveedor SNMP de WMI del 1001 al 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Errores del 1001 al 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c754936d8900a16b89be1f1137984ee6e7d40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575337"
---
# <a name="errors-1001-through-1010"></a>Errores del 1001 al 1010

Describe los errores del proveedor SNMP de WMI del 1001 al 1010.

[Error irreales 1001](#fatal-error-1001)

[Error irreales 1002](#fatal-error-1002)

[Error irreales 1003](#fatal-error-1003)

[Advertencia 1004](#warning-1004)

[Advertencia 1005](#warning-1005)

[Error irreales 1006](#fatal-error-1006)

[Error irreales 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Error irreales 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Error>: " fileName :<line>: la cláusula SYNTAX de OBJECT-TYPE no se resuelve en tipos &lt; &gt; \# permitidos"
</dt> <dd>

Error semántico del módulo de invocación de macro OBJECT-TYPE. La cláusula SYNTAX de la macro OBJECT-TYPE debe resolverse en un tipo o subtipo, formado mediante la especificación SIZE o range que permite SNMPv1 o SNMPv2C SMI. Si este no es el caso, se notifica el error grave 1001.

Este error puede producirse al compilar una MIB SNMPv1 o SNMPv2C.

Los tipos permitidos por SMI SNMPv1 son:

-   INTEGER
-   NULL
-   OCTET STRING
-   IDENTIFICADOR DE OBJETO
-   NetworkAddress
-   IpAddress
-   Contador
-   Medidor
-   TimeTicks
-   Opaca
-   DisplayString
-   PhysAddress

Los tipos permitidos por SMI de SNMPv2C son:

-   INTEGER
-   OCTET STRING
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

## <a name="fatal-error-1002"></a>Error irreales 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, cláusula>: " &lt; fileName &gt; :<line \#>: Cláusula ACCESS &lt; no válida &gt; "
</dt> <dd>

Error semántico del módulo de invocación de macro OBJECT-TYPE. Para SNMPv1, la cláusula ACCESS de la macro OBJECT-TYPE debe ser de "solo lectura", "solo escritura", "lectura/escritura" o "no accesible".

Para SNMPv2C, la cláusula MAX-ACCESS debe ser de "solo lectura", "read-create", "read/write" o "not-accessible".

</dd> </dl>

## <a name="fatal-error-1003"></a>Error irreales 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, cláusula>: " &lt; fileName &gt; :<line \#>: Cláusula STATUS &lt; no válida &gt; "
</dt> <dd>

Error semántico del módulo de invocación de macro OBJECT-TYPE. Para SNMPv1, la cláusula STATUS de una invocación de macro OBJECT-TYPE debe ser "obligatoria", "opcional", "obsoleta" o "en desuso".

Para SNMPv2C, la cláusula STATUS de una invocación de macro OBJECT-TYPE debe ser "actual", "en desuso" u "obsoleta".

</dd> </dl>

## <a name="warning-1004"></a>Advertencia 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Advertencia>: " &lt; fileName &gt; :<line>: identificador OBJECT-TYPE , cuya sintaxis se resuelve en uno de los tipos Counter no termina con la \# &lt; letra &gt; 's' "
</dt> <dd>

Advertencia semántica del módulo de invocación de macro OBJECT-TYPE. El identificador de un objeto de SYNTAX Counter (SNMPv1) o Counter32 y Counter64 (SNMPv2C) debe ser plural.

Esta advertencia puede producirse al compilar una MIB SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Advertencia 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Advertencia>: " &lt; fileName &gt; :<line>: OBJECT-TYPE con SYNTAX "SEQUENCE OF", debe tener una cláusula \# ACCESS "no accesible"
</dt> <dd>

Advertencia semántica del módulo de invocación de macro OBJECT-TYPE. Una tabla o fila conceptual (tipos de objeto SEQUENCE OF o SEQUENCE, respectivamente) debe ser "no accesible".

Esta advertencia puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Error irreales 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, fatal>: " &lt; fileName :<line> OBJECT-TYPE identifier , que es de SYNTAX SEQUENCE, no tiene una cláusula INDEX o &gt; \# &lt; &gt; AUGMENTS"
</dt> <dd>

Error semántico del módulo de invocación de macro OBJECT-TYPE. Para SNMPv1, la cláusula INDEX debe estar presente para una definición OBJECT-TYPE cuya SYNTAX se resuelve en un tipo SEQUENCE.

Para SNMPv2C, la cláusula INDEX o AUGMENTS debe estar presente para una declaración de fila conceptual.

</dd> </dl>

## <a name="fatal-error-1008"></a>Error irreales 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, error irresal>: " &lt; fileName &gt; :<line>: object-TYPE identifier , que es de \# &lt; SYNTAX &gt; "SEQUENCE" no se ha hecho referencia"
</dt> <dd>

Error semántico del módulo de invocación de macro OBJECT-TYPE. Un OBJECT-TYPE con la cláusula SYNTAX como un tipo SEQUENCE debe figurar en la cláusula SYNTAX de exactamente una invocación OBJECT-TYPE que representa una declaración de tabla, es decir, un objeto con la cláusula SYNTAX como un tipo SEQUENCE OF. El <de \#> hace referencia al segundo punto de referencia.

Este error puede producirse en SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



