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
# <a name="errors-1021-through-1030"></a><span data-ttu-id="005cd-103">Errores de 1021 a 1030</span><span class="sxs-lookup"><span data-stu-id="005cd-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="005cd-104">Describe los errores del proveedor SNMP de WMI de 1021 a 1033.</span><span class="sxs-lookup"><span data-stu-id="005cd-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="005cd-105">Error irrecuperable 1021</span><span class="sxs-lookup"><span data-stu-id="005cd-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="005cd-106">Error irrecuperable 1022</span><span class="sxs-lookup"><span data-stu-id="005cd-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="005cd-107">Error irrecuperable 1023</span><span class="sxs-lookup"><span data-stu-id="005cd-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="005cd-108">Error irrecuperable 1024</span><span class="sxs-lookup"><span data-stu-id="005cd-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="005cd-109">Error irrecuperable 1025</span><span class="sxs-lookup"><span data-stu-id="005cd-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="005cd-110">Error irrecuperable 1026</span><span class="sxs-lookup"><span data-stu-id="005cd-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="005cd-111">ADVERTENCIA 1027</span><span class="sxs-lookup"><span data-stu-id="005cd-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="005cd-112">Error irrecuperable 1028</span><span class="sxs-lookup"><span data-stu-id="005cd-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="005cd-113">Error irrecuperable 1029</span><span class="sxs-lookup"><span data-stu-id="005cd-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="005cd-114">Error irrecuperable 1030</span><span class="sxs-lookup"><span data-stu-id="005cd-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="005cd-115">Error irrecuperable 1021</span><span class="sxs-lookup"><span data-stu-id="005cd-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="005cd-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> grave: " <fileName><> de línea \# : <identifier> el identificador de la cláusula variables de Trap-Type no se resuelve como un tipo de objeto escalar"**</span><span class="sxs-lookup"><span data-stu-id="005cd-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-117">Invocación de macros **de tipo de captura** , error semántico del módulo específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="005cd-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="005cd-118">Cada elemento de la lista de variables utilizada en la cláusula VARIABLES de una invocación de macro de **tipo Trap** debe resolverse en el nombre de una instancia de tipo de objeto escalar.</span><span class="sxs-lookup"><span data-stu-id="005cd-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="005cd-119">Error irrecuperable 1022</span><span class="sxs-lookup"><span data-stu-id="005cd-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="005cd-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> grave: " <fileName><\#> de línea: el valor no se resuelve en el tipo <type> "**</span><span class="sxs-lookup"><span data-stu-id="005cd-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-121">Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-122">El valor de la RHS de un entero, un valor **null**, una cadena de octeto o una asignación de valores de identificador de objeto es de un tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="005cd-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="005cd-123">Error irrecuperable 1023</span><span class="sxs-lookup"><span data-stu-id="005cd-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="005cd-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> grave: " <fileName><\#> de línea: <identifier> el identificador no se resuelve como el tipo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="005cd-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-125">Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-126">Un símbolo (referencia de valor) en el RHS de un entero, un valor **null**, una cadena de octeto o una asignación de valores de identificador de objeto no se resuelve en el tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="005cd-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="005cd-127">Error irrecuperable 1024</span><span class="sxs-lookup"><span data-stu-id="005cd-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="005cd-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> grave: " <fileName><\#> de línea: entero negativo en la definición del valor de OID"**</span><span class="sxs-lookup"><span data-stu-id="005cd-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-129">Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-130">Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).</span><span class="sxs-lookup"><span data-stu-id="005cd-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="005cd-131">Error irrecuperable 1025</span><span class="sxs-lookup"><span data-stu-id="005cd-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="005cd-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> grave: "el identificador <identifier> del valor de OID no se resuelve como un entero positivo"**</span><span class="sxs-lookup"><span data-stu-id="005cd-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-133">Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-134">Todos los valores de una lista de componentes OID deben ser enteros no negativos (preferiblemente positivos).</span><span class="sxs-lookup"><span data-stu-id="005cd-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="005cd-135">Error irrecuperable 1026</span><span class="sxs-lookup"><span data-stu-id="005cd-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="005cd-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> grave: " <fileName><\#> de línea: <identifier> el identificador en el valor OID no se resuelve como un valor OID ni un entero positivo"**</span><span class="sxs-lookup"><span data-stu-id="005cd-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-137">Error semántico del módulo de asignación de valores, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-138">El primer componente que se usa en un valor de OID debe resolverse en un valor de OID o un entero.</span><span class="sxs-lookup"><span data-stu-id="005cd-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="005cd-139">ADVERTENCIA 1027</span><span class="sxs-lookup"><span data-stu-id="005cd-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="005cd-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, ADVERTENCIA>: " <fileName><> de línea \# : símbolo importado <identifier> sin usar"**</span><span class="sxs-lookup"><span data-stu-id="005cd-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-141">La sección de IMPORTAciones de la advertencia semántica del módulo, específica no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-142">Se emite una advertencia por cada símbolo importado sin usar.</span><span class="sxs-lookup"><span data-stu-id="005cd-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="005cd-143">Error irrecuperable 1028</span><span class="sxs-lookup"><span data-stu-id="005cd-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="005cd-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> irrecuperable: "módulo <identifier> no importado en la sección de importaciones"**</span><span class="sxs-lookup"><span data-stu-id="005cd-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-145">Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-146">Un nombre de módulo que se usa para hacer referencia a un símbolo debe estar presente en la cláusula Imports o ser el nombre del módulo actual.</span><span class="sxs-lookup"><span data-stu-id="005cd-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="005cd-147">Error irrecuperable 1029</span><span class="sxs-lookup"><span data-stu-id="005cd-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="005cd-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> grave: " <fileName><> de línea \# : el módulo actual <identifier> no se puede importar"**</span><span class="sxs-lookup"><span data-stu-id="005cd-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-149">Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-150">El nombre del módulo actual también se muestra en la lista de IMPORTAciones.</span><span class="sxs-lookup"><span data-stu-id="005cd-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="005cd-151">Error irrecuperable 1030</span><span class="sxs-lookup"><span data-stu-id="005cd-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="005cd-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> grave: " <fileName><\#> de línea: símbolo <identifier> no importado desde el módulo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="005cd-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="005cd-153">Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="005cd-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="005cd-154">Ha usado la notación "module. Symbol", pero el símbolo no se ha importado desde el módulo especificado en la sección Imports.</span><span class="sxs-lookup"><span data-stu-id="005cd-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



