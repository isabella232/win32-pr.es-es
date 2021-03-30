---
description: Describe los errores del proveedor SNMP de WMI de 211 a 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Errores de 211 a 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25dbf8cb8f27d4c58a1505176eca218b8d947d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817603"
---
# <a name="errors-211-through-220"></a><span data-ttu-id="b9407-103">Errores de 211 a 220</span><span class="sxs-lookup"><span data-stu-id="b9407-103">Errors 211 through 220</span></span>

<span data-ttu-id="b9407-104">Describe los errores del proveedor SNMP de WMI de 211 a 220.</span><span class="sxs-lookup"><span data-stu-id="b9407-104">Describes WMI SNMP provider errors 211 through 220.</span></span>

[<span data-ttu-id="b9407-105">Mensaje de información 211</span><span class="sxs-lookup"><span data-stu-id="b9407-105">Information Message 211</span></span>](#information-message-211)

[<span data-ttu-id="b9407-106">Error irrecuperable 212</span><span class="sxs-lookup"><span data-stu-id="b9407-106">Fatal Error 212</span></span>](#fatal-error-212)

[<span data-ttu-id="b9407-107">Error irrecuperable 213</span><span class="sxs-lookup"><span data-stu-id="b9407-107">Fatal Error 213</span></span>](#fatal-error-213)

[<span data-ttu-id="b9407-108">Error irrecuperable 214</span><span class="sxs-lookup"><span data-stu-id="b9407-108">Fatal Error 214</span></span>](#fatal-error-214)

[<span data-ttu-id="b9407-109">Error irrecuperable 215</span><span class="sxs-lookup"><span data-stu-id="b9407-109">Fatal Error 215</span></span>](#fatal-error-215)

[<span data-ttu-id="b9407-110">Error irrecuperable 216</span><span class="sxs-lookup"><span data-stu-id="b9407-110">Fatal Error 216</span></span>](#fatal-error-216)

[<span data-ttu-id="b9407-111">Error irrecuperable 217</span><span class="sxs-lookup"><span data-stu-id="b9407-111">Fatal Error 217</span></span>](#fatal-error-217)

[<span data-ttu-id="b9407-112">Error irrecuperable 218</span><span class="sxs-lookup"><span data-stu-id="b9407-112">Fatal Error 218</span></span>](#fatal-error-218)

[<span data-ttu-id="b9407-113">Error irrecuperable 219</span><span class="sxs-lookup"><span data-stu-id="b9407-113">Fatal Error 219</span></span>](#fatal-error-219)

[<span data-ttu-id="b9407-114">Error irrecuperable 220</span><span class="sxs-lookup"><span data-stu-id="b9407-114">Fatal Error 220</span></span>](#fatal-error-220)

## <a name="information-message-211"></a><span data-ttu-id="b9407-115">Mensaje de información 211</span><span class="sxs-lookup"><span data-stu-id="b9407-115">Information Message 211</span></span>

<dl> <dt>

<span data-ttu-id="b9407-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, información>: "omitiendo el tipo de captura <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Information>: "Skipping TRAP-TYPE <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-117">Los errores de la definición de tipo de captura generan este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9407-117">Any errors in the TRAP-TYPE definition generate this message.</span></span>

</dd> </dl>

## <a name="fatal-error-212"></a><span data-ttu-id="b9407-118">Error irrecuperable 212</span><span class="sxs-lookup"><span data-stu-id="b9407-118">Fatal Error 212</span></span>

<dl> <dt>

<span data-ttu-id="b9407-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la definición de la secuencia. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: "<fileName>:<line\#>: Syntax Error in SEQUENCE definition. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-120">Error de sintaxis de módulo en la asignación de tipo.</span><span class="sxs-lookup"><span data-stu-id="b9407-120">Module syntax error in type assignment.</span></span> <span data-ttu-id="b9407-121">Hay un error entre las llaves izquierda y derecha de una construcción de secuencia, que se remonta en un error de sintaxis en una asignación de tipo de MIB.</span><span class="sxs-lookup"><span data-stu-id="b9407-121">There is an error between the left and right braces of a SEQUENCE construct, which amounts to a syntax error in a MIB type assignment.</span></span>

</dd> </dl>

## <a name="fatal-error-213"></a><span data-ttu-id="b9407-122">Error irrecuperable 213</span><span class="sxs-lookup"><span data-stu-id="b9407-122">Fatal Error 213</span></span>

<dl> <dt>

<span data-ttu-id="b9407-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en el valor del identificador de objeto. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: "<fileName>:<line\#>: Syntax Error in Object Identifier value. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-124">Error de sintaxis de módulo en la asignación de valores.</span><span class="sxs-lookup"><span data-stu-id="b9407-124">Module syntax error in value assignment.</span></span> <span data-ttu-id="b9407-125">Hay un error entre las llaves izquierda y derecha de un valor de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="b9407-125">There is an error between the left and right braces of an object identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-214"></a><span data-ttu-id="b9407-126">Error irrecuperable 214</span><span class="sxs-lookup"><span data-stu-id="b9407-126">Fatal Error 214</span></span>

<dl> <dt>

<span data-ttu-id="b9407-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la lista de símbolos de las importaciones. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: "<fileName>:<line\#>: Syntax Error in the list of symbols in IMPORTS. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-128">Error de sintaxis de módulo en la sección Imports.</span><span class="sxs-lookup"><span data-stu-id="b9407-128">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-215"></a><span data-ttu-id="b9407-129">Error irrecuperable 215</span><span class="sxs-lookup"><span data-stu-id="b9407-129">Fatal Error 215</span></span>

<dl> <dt>

<span data-ttu-id="b9407-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en las importaciones (falta el nombre del módulo?). La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Fatal>: "<fileName>:<line\#>: Syntax Error in IMPORTS (missing module name?). Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-131">Error de sintaxis de módulo en la sección Imports.</span><span class="sxs-lookup"><span data-stu-id="b9407-131">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-216"></a><span data-ttu-id="b9407-132">Error irrecuperable 216</span><span class="sxs-lookup"><span data-stu-id="b9407-132">Fatal Error 216</span></span>

<dl> <dt>

<span data-ttu-id="b9407-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216,> grave: " <fileName> : <línea \#>: error de sintaxis en la sección Imports. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Fatal>: "<fileName>:<line\#>: Syntax Error in the IMPORTS section. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-134">Error de sintaxis de módulo en la sección Imports.</span><span class="sxs-lookup"><span data-stu-id="b9407-134">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-217"></a><span data-ttu-id="b9407-135">Error irrecuperable 217</span><span class="sxs-lookup"><span data-stu-id="b9407-135">Fatal Error 217</span></span>

<dl> <dt>

<span data-ttu-id="b9407-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la enumeración de enteros. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: "<fileName>:<line\#>: Syntax error in INTEGER Enumeration. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-137">Cualquier error de sintaxis del módulo entre las llaves izquierda y derecha de una definición de enumeración MIB genera este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9407-137">Any module syntax error between the left and right braces of a MIB enumeration definition generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-218"></a><span data-ttu-id="b9407-138">Error irrecuperable 218</span><span class="sxs-lookup"><span data-stu-id="b9407-138">Fatal Error 218</span></span>

<dl> <dt>

<span data-ttu-id="b9407-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la especificación de subtipos. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: "<fileName>:<line\#>: Syntax Error in sub-type specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-140">Cualquier error de sintaxis de módulo entre los paréntesis de una especificación de subtipo genera este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9407-140">Any module syntax error between the parentheses in a sub-type specification generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-219"></a><span data-ttu-id="b9407-141">Error irrecuperable 219</span><span class="sxs-lookup"><span data-stu-id="b9407-141">Fatal Error 219</span></span>

<dl> <dt>

<span data-ttu-id="b9407-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la especificación de tamaño. La última lectura del token es <token> "**</span><span class="sxs-lookup"><span data-stu-id="b9407-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Fatal>:"<fileName>:<line\#>: Syntax Error in the SIZE specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-143">Cualquier error de sintaxis del módulo en la cláusula SIZE entre los paréntesis izquierdo y derecho genera este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9407-143">Any module syntax error in the SIZE clause between the left and right parentheses generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-220"></a><span data-ttu-id="b9407-144">Error irrecuperable 220</span><span class="sxs-lookup"><span data-stu-id="b9407-144">Fatal Error 220</span></span>

<dl> <dt>

<span data-ttu-id="b9407-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220,> irrecuperable: " <fileName> : <línea \#>: no se permite la invocación del tipo de objeto de SNMPv2SMI"**</span><span class="sxs-lookup"><span data-stu-id="b9407-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE invocation of SNMPv2SMI not allowed"**</span></span>
</dt> <dd>

<span data-ttu-id="b9407-146">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="b9407-146">Module syntax error.</span></span> <span data-ttu-id="b9407-147">Ha usado la invocación de **tipo de objeto** específica de SNMPv2c en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="b9407-147">You have used the SNMPv2C-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

 

 



