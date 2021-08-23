---
description: Describe los errores del proveedor WMI SNMP del 211 al 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Errores del 211 al 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3394f6ca4317d14e83ca17b3a8ef9b516d218c072659041f7c6f5b035e6cdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556707"
---
# <a name="errors-211-through-220"></a>Errores del 211 al 220

Describe los errores del proveedor WMI SNMP del 211 al 220.

[Mensaje de información 211](#information-message-211)

[Error irresal 212](#fatal-error-212)

[Error irresal 213](#fatal-error-213)

[Error irresal 214](#fatal-error-214)

[Error irresal 215](#fatal-error-215)

[Error irresal 216](#fatal-error-216)

[Error irresal 217](#fatal-error-217)

[Error irresal 218](#fatal-error-218)

[Error irresal 219](#fatal-error-219)

[Error irresal 220](#fatal-error-220)

## <a name="information-message-211"></a>Mensaje de información 211

<dl> <dt>

<span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Información>: "Omisión de <identifier> TRAP-TYPE"**
</dt> <dd>

Los errores de la definición TRAP-TYPE generan este mensaje.

</dd> </dl>

## <a name="fatal-error-212"></a>Error irresal 212

<dl> <dt>

<span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Error>: " :<línea>: Error de sintaxis en la <fileName> \# definición de SEQUENCE. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis del módulo en la asignación de tipos. Hay un error entre las llaves izquierda y derecha de una construcción SEQUENCE, que equivale a un error de sintaxis en una asignación de tipo MIB.

</dd> </dl>

## <a name="fatal-error-213"></a>Error irresal 213

<dl> <dt>

<span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Error>: " :<línea>: Error de sintaxis en el valor identificador <fileName> \# de objeto. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis del módulo en la asignación de valores. Hay un error entre las llaves izquierda y derecha de un valor de identificador de objeto.

</dd> </dl>

## <a name="fatal-error-214"></a>Error irresal 214

<dl> <dt>

<span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Error de sintaxis>: " :<line>: Error de sintaxis en la lista de símbolos <fileName> \# de IMPORTS. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis del módulo en la sección IMPORTS.

</dd> </dl>

## <a name="fatal-error-215"></a>Error irresal 215

<dl> <dt>

<span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Error de>: " <fileName> :<line>: Error de sintaxis en IMPORTS (¿falta el nombre \# del módulo?). La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis del módulo en la sección IMPORTS.

</dd> </dl>

## <a name="fatal-error-216"></a>Error irresal 216

<dl> <dt>

<span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Error>: " <fileName> :<línea \#>: Error de sintaxis en la sección IMPORTS. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis del módulo en la sección IMPORTS.

</dd> </dl>

## <a name="fatal-error-217"></a>Error irresal 217

<dl> <dt>

<span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Error irresumen>: " <fileName> :<línea>: Error de \# sintaxis en la enumeración INTEGER. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis de módulo entre las llaves izquierda y derecha de una definición de enumeración MIB genera este mensaje.

</dd> </dl>

## <a name="fatal-error-218"></a>Error irresal 218

<dl> <dt>

<span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Error>: " :<línea>: Error de sintaxis en la especificación <fileName> \# de subtipo. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis de módulo entre paréntesis en una especificación de subtipo genera este mensaje.

</dd> </dl>

## <a name="fatal-error-219"></a>Error irresal 219

<dl> <dt>

<span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Error>:" :<línea>: Error de sintaxis en la <fileName> \# especificación SIZE. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis de módulo en la cláusula SIZE entre los paréntesis izquierdo y derecho genera este mensaje.

</dd> </dl>

## <a name="fatal-error-220"></a>Error irresal 220

<dl> <dt>

<span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Error>:" :<line>: No se permite la invocación <fileName> \# object-TYPE de SNMPv2SMI"**
</dt> <dd>

Error de sintaxis del módulo. Ha usado la invocación **OBJECT-TYPE** específica de SNMPv2C en la MIB, pero ha especificado el modificador **/v1,** que requiere una conformidad estricta con la sintaxis de SNMPv1.

</dd> </dl>

 

 



