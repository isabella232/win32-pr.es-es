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
# <a name="errors-1001-through-1010"></a><span data-ttu-id="5e052-103">Errores de 1001 a 1010</span><span class="sxs-lookup"><span data-stu-id="5e052-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="5e052-104">Describe los errores del proveedor SNMP de WMI de 1001 a 1010.</span><span class="sxs-lookup"><span data-stu-id="5e052-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="5e052-105">Error irrecuperable 1001</span><span class="sxs-lookup"><span data-stu-id="5e052-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="5e052-106">Error irrecuperable 1002</span><span class="sxs-lookup"><span data-stu-id="5e052-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="5e052-107">Error irrecuperable 1003</span><span class="sxs-lookup"><span data-stu-id="5e052-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="5e052-108">ADVERTENCIA 1004</span><span class="sxs-lookup"><span data-stu-id="5e052-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="5e052-109">ADVERTENCIA 1005</span><span class="sxs-lookup"><span data-stu-id="5e052-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="5e052-110">Error irrecuperable 1006</span><span class="sxs-lookup"><span data-stu-id="5e052-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="5e052-111">Error irrecuperable 1008</span><span class="sxs-lookup"><span data-stu-id="5e052-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="5e052-112">Error irrecuperable 1001</span><span class="sxs-lookup"><span data-stu-id="5e052-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="5e052-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> irrecuperable: " <fileName> : <línea \#>: la cláusula Syntax de tipo Object no se resuelve como tipos permitidos"</span><span class="sxs-lookup"><span data-stu-id="5e052-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-114">Error semántico del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="5e052-115">La cláusula de sintaxis de la macro OBJECT-TYPE debe resolverse en un tipo o subtipo, formado mediante la especificación de tamaño o intervalo que permite la SMI de SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5e052-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="5e052-116">Si no es así, se muestra el error irrecuperable 1001.</span><span class="sxs-lookup"><span data-stu-id="5e052-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="5e052-117">Este error puede producirse al compilar una MIB de SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5e052-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="5e052-118">Los tipos permitidos por la SMI de SNMPv1 son:</span><span class="sxs-lookup"><span data-stu-id="5e052-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="5e052-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5e052-119">INTEGER</span></span>
-   <span data-ttu-id="5e052-120">NULL</span><span class="sxs-lookup"><span data-stu-id="5e052-120">NULL</span></span>
-   <span data-ttu-id="5e052-121">CADENA DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="5e052-121">OCTET STRING</span></span>
-   <span data-ttu-id="5e052-122">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="5e052-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="5e052-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-123">NetworkAddress</span></span>
-   <span data-ttu-id="5e052-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-124">IpAddress</span></span>
-   <span data-ttu-id="5e052-125">Contador</span><span class="sxs-lookup"><span data-stu-id="5e052-125">Counter</span></span>
-   <span data-ttu-id="5e052-126">Indicador</span><span class="sxs-lookup"><span data-stu-id="5e052-126">Gauge</span></span>
-   <span data-ttu-id="5e052-127">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="5e052-127">TimeTicks</span></span>
-   <span data-ttu-id="5e052-128">Opaca</span><span class="sxs-lookup"><span data-stu-id="5e052-128">Opaque</span></span>
-   <span data-ttu-id="5e052-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="5e052-129">DisplayString</span></span>
-   <span data-ttu-id="5e052-130">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-130">PhysAddress</span></span>

<span data-ttu-id="5e052-131">Los tipos permitidos por la SMI de SNMPv2C son:</span><span class="sxs-lookup"><span data-stu-id="5e052-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="5e052-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5e052-132">INTEGER</span></span>
-   <span data-ttu-id="5e052-133">CADENA DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="5e052-133">OCTET STRING</span></span>
-   <span data-ttu-id="5e052-134">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="5e052-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="5e052-135">BITS</span><span class="sxs-lookup"><span data-stu-id="5e052-135">BITS</span></span>
-   <span data-ttu-id="5e052-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="5e052-136">Integer32</span></span>
-   <span data-ttu-id="5e052-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-137">IpAddress</span></span>
-   <span data-ttu-id="5e052-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="5e052-138">Counter32</span></span>
-   <span data-ttu-id="5e052-139">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="5e052-139">TimeTicks</span></span>
-   <span data-ttu-id="5e052-140">Opaca</span><span class="sxs-lookup"><span data-stu-id="5e052-140">Opaque</span></span>
-   <span data-ttu-id="5e052-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="5e052-141">Counter64</span></span>
-   <span data-ttu-id="5e052-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="5e052-142">Unsigned32</span></span>
-   <span data-ttu-id="5e052-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="5e052-143">DisplayString</span></span>
-   <span data-ttu-id="5e052-144">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-144">PhysAddress</span></span>
-   <span data-ttu-id="5e052-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="5e052-145">MacAddress</span></span>
-   <span data-ttu-id="5e052-146">TruthValue</span><span class="sxs-lookup"><span data-stu-id="5e052-146">TruthValue</span></span>
-   <span data-ttu-id="5e052-147">TestAndIncr</span><span class="sxs-lookup"><span data-stu-id="5e052-147">TestAndIncr</span></span>
-   <span data-ttu-id="5e052-148">AutonomousType</span><span class="sxs-lookup"><span data-stu-id="5e052-148">AutonomousType</span></span>
-   <span data-ttu-id="5e052-149">InstancePointer</span><span class="sxs-lookup"><span data-stu-id="5e052-149">InstancePointer</span></span>
-   <span data-ttu-id="5e052-150">VariablePointer</span><span class="sxs-lookup"><span data-stu-id="5e052-150">VariablePointer</span></span>
-   <span data-ttu-id="5e052-151">RowPointer</span><span class="sxs-lookup"><span data-stu-id="5e052-151">RowPointer</span></span>
-   <span data-ttu-id="5e052-152">RowStatus</span><span class="sxs-lookup"><span data-stu-id="5e052-152">RowStatus</span></span>
-   <span data-ttu-id="5e052-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="5e052-153">TimeStamp</span></span>
-   <span data-ttu-id="5e052-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="5e052-154">TimeInterval</span></span>
-   <span data-ttu-id="5e052-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="5e052-155">DateAndTime</span></span>
-   <span data-ttu-id="5e052-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="5e052-156">StorageType</span></span>
-   <span data-ttu-id="5e052-157">Tdomain</span><span class="sxs-lookup"><span data-stu-id="5e052-157">Tdomain</span></span>
-   <span data-ttu-id="5e052-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="5e052-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="5e052-159">Error irrecuperable 1002</span><span class="sxs-lookup"><span data-stu-id="5e052-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="5e052-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> irrecuperable: " <fileName> : <de línea \#>: cláusula de acceso no válida <clause> "</span><span class="sxs-lookup"><span data-stu-id="5e052-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-161">Error semántico del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="5e052-162">Para SNMPv1, la cláusula de acceso de la macro del tipo de objeto debe ser "de solo lectura", "solo escritura", "lectura/escritura" o "no accesible".</span><span class="sxs-lookup"><span data-stu-id="5e052-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="5e052-163">Para SNMPv2C, la cláusula MAX-ACCESS debe ser "de solo lectura", "lectura y creación", "lectura/escritura" o "no accesible".</span><span class="sxs-lookup"><span data-stu-id="5e052-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="5e052-164">Error irrecuperable 1003</span><span class="sxs-lookup"><span data-stu-id="5e052-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="5e052-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> irrecuperable: " <fileName> : <línea \#>: cláusula de estado no válida <clause> "</span><span class="sxs-lookup"><span data-stu-id="5e052-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-166">Error semántico del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="5e052-167">Para SNMPv1, la cláusula de estado de una invocación de macro de tipo de objeto debe ser "obligatoria", "opcional", "obsoleto" o "desusado".</span><span class="sxs-lookup"><span data-stu-id="5e052-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="5e052-168">Para SNMPv2C, la cláusula de estado de una invocación de macro de tipo de objeto debe ser "actual", "en desuso" o "obsoleto".</span><span class="sxs-lookup"><span data-stu-id="5e052-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="5e052-169">ADVERTENCIA 1004</span><span class="sxs-lookup"><span data-stu-id="5e052-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="5e052-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, ADVERTENCIA>: " <fileName> : <línea \#>: Object-Type <identifier> , cuya sintaxis se resuelve como uno de los tipos de contador no termina con la ' ' de la letra</span><span class="sxs-lookup"><span data-stu-id="5e052-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="5e052-171">ADVERTENCIA semántica del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="5e052-172">El identificador de un objeto de contador de sintaxis (SNMPv1) o Counter32 y Counter64 (SNMPv2C) debe ser plural.</span><span class="sxs-lookup"><span data-stu-id="5e052-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="5e052-173">Esta advertencia puede producirse al compilar una MIB de SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5e052-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="5e052-174">ADVERTENCIA 1005</span><span class="sxs-lookup"><span data-stu-id="5e052-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="5e052-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, ADVERTENCIA>: " <fileName> : <línea \#>: tipo de objeto con la sintaxis" secuencia de ", debe tener una cláusula de acceso" no accesible ".</span><span class="sxs-lookup"><span data-stu-id="5e052-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-176">ADVERTENCIA semántica del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="5e052-177">Una tabla o fila conceptual (secuencia de tipos de objeto de secuencia o, respectivamente) debe ser "no accesible".</span><span class="sxs-lookup"><span data-stu-id="5e052-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="5e052-178">Esta advertencia puede producirse en SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5e052-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="5e052-179">Error irrecuperable 1006</span><span class="sxs-lookup"><span data-stu-id="5e052-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="5e052-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> irrecuperable: " <fileName> : <de línea \#> tipo de objeto <identifier> , que es la secuencia de sintaxis, no tiene una cláusula index o aumenta"</span><span class="sxs-lookup"><span data-stu-id="5e052-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-181">Error semántico del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="5e052-182">Para SNMPv1, la cláusula INDEX debe estar presente para una definición de tipo de objeto cuya sintaxis se resuelva como un tipo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e052-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="5e052-183">Para SNMPv2C, el índice o la cláusula de AUMENTOs deben estar presentes para una declaración de fila conceptual.</span><span class="sxs-lookup"><span data-stu-id="5e052-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="5e052-184">Error irrecuperable 1008</span><span class="sxs-lookup"><span data-stu-id="5e052-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="5e052-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> irrecuperable: " <fileName> : <línea \#>: <identifier> no se ha hecho referencia a un tipo de objeto, que es de sintaxis" Sequence ".</span><span class="sxs-lookup"><span data-stu-id="5e052-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="5e052-186">Error semántico del módulo de invocación de macros de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e052-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="5e052-187">Un tipo de objeto con la cláusula de sintaxis como un tipo de secuencia debe figurar en la cláusula de sintaxis de exactamente una invocación de tipo de objeto que representa una declaración de tabla, es decir, un objeto con la cláusula de sintaxis como una secuencia de tipo.</span><span class="sxs-lookup"><span data-stu-id="5e052-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="5e052-188">El \# parámetro> de línea de <hace referencia al segundo punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="5e052-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="5e052-189">Este error puede producirse en SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5e052-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



