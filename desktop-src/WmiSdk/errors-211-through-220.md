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
# <a name="errors-211-through-220"></a>Errores de 211 a 220

Describe los errores del proveedor SNMP de WMI de 211 a 220.

[Mensaje de información 211](#information-message-211)

[Error irrecuperable 212](#fatal-error-212)

[Error irrecuperable 213](#fatal-error-213)

[Error irrecuperable 214](#fatal-error-214)

[Error irrecuperable 215](#fatal-error-215)

[Error irrecuperable 216](#fatal-error-216)

[Error irrecuperable 217](#fatal-error-217)

[Error irrecuperable 218](#fatal-error-218)

[Error irrecuperable 219](#fatal-error-219)

[Error irrecuperable 220](#fatal-error-220)

## <a name="information-message-211"></a>Mensaje de información 211

<dl> <dt>

<span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, información>: "omitiendo el tipo de captura <identifier> "**
</dt> <dd>

Los errores de la definición de tipo de captura generan este mensaje.

</dd> </dl>

## <a name="fatal-error-212"></a>Error irrecuperable 212

<dl> <dt>

<span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la definición de la secuencia. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis de módulo en la asignación de tipo. Hay un error entre las llaves izquierda y derecha de una construcción de secuencia, que se remonta en un error de sintaxis en una asignación de tipo de MIB.

</dd> </dl>

## <a name="fatal-error-213"></a>Error irrecuperable 213

<dl> <dt>

<span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en el valor del identificador de objeto. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis de módulo en la asignación de valores. Hay un error entre las llaves izquierda y derecha de un valor de identificador de objeto.

</dd> </dl>

## <a name="fatal-error-214"></a>Error irrecuperable 214

<dl> <dt>

<span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la lista de símbolos de las importaciones. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis de módulo en la sección Imports.

</dd> </dl>

## <a name="fatal-error-215"></a>Error irrecuperable 215

<dl> <dt>

<span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en las importaciones (falta el nombre del módulo?). La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis de módulo en la sección Imports.

</dd> </dl>

## <a name="fatal-error-216"></a>Error irrecuperable 216

<dl> <dt>

<span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216,> grave: " <fileName> : <línea \#>: error de sintaxis en la sección Imports. La última lectura del token es <token> "**
</dt> <dd>

Error de sintaxis de módulo en la sección Imports.

</dd> </dl>

## <a name="fatal-error-217"></a>Error irrecuperable 217

<dl> <dt>

<span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la enumeración de enteros. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis del módulo entre las llaves izquierda y derecha de una definición de enumeración MIB genera este mensaje.

</dd> </dl>

## <a name="fatal-error-218"></a>Error irrecuperable 218

<dl> <dt>

<span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la especificación de subtipos. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis de módulo entre los paréntesis de una especificación de subtipo genera este mensaje.

</dd> </dl>

## <a name="fatal-error-219"></a>Error irrecuperable 219

<dl> <dt>

<span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219,> irrecuperable: " <fileName> : <línea \#>: error de sintaxis en la especificación de tamaño. La última lectura del token es <token> "**
</dt> <dd>

Cualquier error de sintaxis del módulo en la cláusula SIZE entre los paréntesis izquierdo y derecho genera este mensaje.

</dd> </dl>

## <a name="fatal-error-220"></a>Error irrecuperable 220

<dl> <dt>

<span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220,> irrecuperable: " <fileName> : <línea \#>: no se permite la invocación del tipo de objeto de SNMPv2SMI"**
</dt> <dd>

Error de sintaxis de módulo. Ha usado la invocación de **tipo de objeto** específica de SNMPv2c en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.

</dd> </dl>

 

 



