---
title: Errores del compilador
description: Lista de mensajes de error generados durante la compilación de MIDL.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- errores MIDL, errores del compilador
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b4bb2189e824f82cc9247abc68844068d083b2f0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149694"
---
# <a name="compiler-errors"></a>Errores del compilador

Durante la compilación de MIDL, se generan los siguientes mensajes de error:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>debe especificar/c_ext para declaradores abstractos</dt> <dd> Los declaradores abstractos representan una extensión de Microsoft a RPC y no se definen en DCE RPC. Por lo tanto, si el archivo incluye declaradores abstractos, no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que exige una compatibilidad estricta con DCE. Las versiones de MIDL 3,0 y posteriores usan el modificador <a href="-c-ext.md"><strong>/c_ext</strong></a> como valor predeterminado; el modificador <strong>/OSF</strong> desactiva el modificador <strong>/c_ext</strong> . Para obtener información sobre los declaradores abstractos, vea <a href="/windows/desktop/Rpc/the-acf-body">el cuerpo ACF</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>la creación de instancias de los datos no es válida; debe usar &quot; extern &quot; o &quot; static&quot;</dt> <dd> La declaración y la inicialización en el archivo IDL no son compatibles con el RPC de DCE. Esta característica es una extensión de Microsoft que no está disponible al compilar en modo de compatibilidad con DCE (<a href="-osf.md"><strong>/OSF</strong></a>).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>desbordamiento de pila del compilador</dt> <dd> El compilador se quedó sin espacio de pila al procesar el archivo IDL. Este problema puede producirse cuando el compilador está procesando una declaración o expresión compleja. Para solucionar el problema, simplifique la declaración o expresión compleja.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>nueva definición</dt> <dd> Este mensaje de error puede aparecer en las siguientes circunstancias: se ha redefinido un tipo. se ha redefinido un prototipo de procedimiento. ya existe un miembro de una estructura o unión con el mismo nombre; ya existe un parámetro con el mismo nombre en el prototipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] se usará el enlace</dt> <dd> No se ha definido ningún tipo de identificador como el tipo de identificador predeterminado. El compilador supone que se usará un identificador automático como identificador de enlace para el procedimiento especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>memoria insuficiente</dt> <dd> El compilador se quedó sin memoria durante la compilación. Reduzca el tamaño o la complejidad del archivo IDL o asigne más memoria al proceso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>definición recursiva</dt> <dd> Una estructura o Unión se ha definido de forma recursiva. Este error puede producirse cuando se omite una especificación de puntero en una definición de estructura anidada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>importación omitida; archivo ya importado</dt> <dd> La importación de un archivo IDL es una operación idempotente. Incluirlo más de una vez no tiene ningún efecto. Se omiten todas las operaciones de importación excepto la primera.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>las enumeraciones dispersas requieren/c_ext o/ms_ext</dt> <dd> La asignación de valores a constantes de enumeración no es compatible con el RPC de DCE. Si desea usar las extensiones de Microsoft para MIDL que permiten asignar valores a constantes de enumeración, no puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que exige una compatibilidad estricta con DCE. Las versiones 3,0 y posteriores de MIDL usan los modificadores <a href="-c-ext.md"><strong>/c_ext</strong></a> y <a href="-ms-ext.md"><strong>/ms_ext</strong></a> como valor predeterminado; el modificador <strong>/OSF</strong> desactiva estos modificadores de extensión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>símbolo sin definir</dt> <dd> Se ha utilizado un símbolo no definido en una expresión. Este error puede producirse cuando se usa un valor enumerado sin definir.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>tipo usado en el archivo ACF no definido en el archivo IDL</dt> <dd> Se está utilizando un tipo no definido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>Declaración de tipos sin resolver</dt> <dd> El tipo indicado en el campo de información de error adicional no se ha definido en ningún otro lugar del archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>el uso de constantes de caracteres anchos requiere/ms_ext o/c_ext</dt> <dd> Las constantes de caracteres anchos son una extensión de Microsoft a DCE IDL. Para usar el tipo de datos <a href="wchar-t.md"><strong>wchar_t</strong></a>, no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que invalida los modificadores predeterminados <a href="-ms-ext.md"><strong>/ms_ext</strong></a> y <a href="-c-ext.md"><strong>/c_ext</strong></a>del compilador de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>el uso de cadenas de caracteres anchos requiere/ms_ext o/c_ext</dt> <dd> Las constantes de cadena de caracteres anchos son una extensión de Microsoft a DCE IDL. Para usar el tipo de datos <a href="wchar-t.md"><strong>wchar_t</strong></a>, no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que invalida los modificadores predeterminados <a href="-ms-ext.md"><strong>/ms_ext</strong></a> y <a href="-c-ext.md"><strong>/c_ext</strong></a>del compilador de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>redefinición incoherente del tipo wchar_t</dt> <dd> El tipo <a href="wchar-t.md"><strong>wchar_t</strong></a> se ha redefinido como un tipo que no es equivalente a dos cortos sin signo *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>no se encontró importlib</dt> <dd> El compilador no encontró la biblioteca de tipos especificada por la Directiva [ <a href="importlib.md"><strong>importlib</strong></a>]. Asegúrese de que la ruta de acceso y el nombre de la biblioteca son correctos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>dos bloques de biblioteca</dt> <dd> Dos bloques de biblioteca (incluso con nombres diferentes) en el mismo archivo de código fuente no son válidos. Combine todos los elementos en un único bloque de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>la instrucción dispinterface requiere una definición para IDispatch</dt> <dd> Este error suele producirse cuando no se importan los archivos Stdole2. tlb o Oaidl. idl.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>Error al acceder a la biblioteca de tipos</dt> <dd> El compilador no encontró la biblioteca de tipos especificada. Asegúrese de que ha especificado la ruta de acceso correctamente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>Error al acceder a la información de tipo</dt> <dd> La biblioteca de tipos importada está dañada, no es válida o solo se ha construido parcialmente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>Error al generar la biblioteca de tipos</dt> <dd> No se pudo generar la biblioteca de tipos. Una posible causa de este error es la especificación de una ruta de acceso al archivo IDL que tiene más de 126 caracteres. Oleaut32.dll no admite nombres de ruta de acceso de más de 126 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>identificador duplicado</dt> <dd> Las aplicaciones usan la instrucción <a href="id.md"><strong>ID</strong></a> en los archivos IDL para especificar un DISPID para las funciones miembro. Las funciones miembro pueden ser propiedades o métodos de interfaces o interfaces dispinterface. Este error indica que el archivo IDL especifica el mismo número de identificador para dos métodos o propiedades.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>falta un valor o no es válido para el atributo de entrada</dt> <dd> El argumento para el atributo de entrada puede ser una cadena que especifique un punto de entrada con nombre o un número ordinal que defina el punto de entrada. Falta este argumento o contiene un valor no válido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>se presupone la recuperación de errores</dt> <dd> El compilador MIDL encontró caracteres no válidos en el archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>descartes de recuperación de errores</dt> <dd> El compilador MIDL encontró caracteres no válidos en el archivo IDL. Omitirá los caracteres no válidos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>error de sintaxis</dt> <dd> El compilador detectó un error de sintaxis en la línea especificada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>no se puede recuperar de errores de sintaxis anteriores; anulando compilación</dt> <dd> El compilador MIDL intenta recuperar automáticamente los errores de sintaxis agregando o quitando elementos sintácticos. Este mensaje indica que, a pesar de estos intentos de recuperación, el compilador detectó demasiados errores. Corrija los errores especificados y vuelva a compilar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>opción pragma desconocida</dt> <dd> La Directiva pragma de C especificada no es compatible con MIDL. Quite la Directiva pragma del archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>característica no implementada</dt> <dd> La característica MIDL, aunque forma parte de la definición del lenguaje, no se implementa en Microsoft RPC y no es compatible con el compilador de MIDL. Por ejemplo, no se implementan las siguientes características de lenguaje: BitSet, Pipe y el tipo de carácter internacional. La característica de lenguaje no implementado aparece en el campo de información de error adicional del mensaje de error.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>tipo no implementado</dt> <dd> El tipo de datos especificado, aunque es una palabra clave válida de MIDL, no se implementa en Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>no puntero utilizado en una operación de desreferencia</dt> <dd> Un tipo de datos que no es un puntero se ha asociado a las operaciones de puntero. No se puede obtener acceso al objeto a través del puntero no especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>la expresión tiene una división por cero</dt> <dd> La expresión constante contiene división por cero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>la expresión usa tipos incompatibles</dt> <dd> Los lados izquierdo y derecho del operador en una expresión son de tipos incompatibles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>la expresión nonarray usa el operador index</dt> <dd> La expresión usa la operación de indización de matriz en un elemento de datos que no es del tipo de matriz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>la parte izquierda de la expresión no se evalúa como struct/union/enum</dt> <dd> Operador de referencia directo o indirecto &quot; . o se ha &quot; &quot; -> &quot; aplicado a un objeto de datos que no es una estructura, una Unión o una enumeración. No se puede obtener una referencia directa o indirecta mediante el objeto especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>se esperaba una expresión constante</dt> <dd> Se esperaba una expresión constante en la sintaxis. Por ejemplo, los límites de matriz requieren una expresión constante. El compilador emite este mensaje de error cuando el límite de la matriz se define con una variable o un símbolo sin definir.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>la expresión no se puede evaluar en tiempo de compilación</dt> <dd> El compilador no puede evaluar una expresión en tiempo de compilación.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>expresión no implementada</dt> <dd> Una característica que se admitía en versiones anteriores del compilador MIDL no se admite en la versión del compilador proporcionada con Microsoft RPC. Quite la expresión especificada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>no se especificó ningún atributo [pointer_default], se supone que [Unique] para todos los punteros sin atributos</dt> <dd> El compilador MIDL ofrece tres casos predeterminados diferentes para los punteros que no tienen atributos de puntero. Los parámetros de función que son punteros de nivel superior tienen como valor predeterminado punteros [<a href="ref.md"><strong>ref</strong></a>]. Los punteros incrustados en estructuras y punteros a otros punteros (no a los punteros de nivel superior) tienen como valor predeterminado el tipo especificado por el atributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>]. Cuando no se proporciona ningún atributo [<strong>pointer_default</strong>], estos punteros de nivel de nontop tienen como valor predeterminado punteros únicos. Este mensaje de error indica el último caso: no se proporciona el atributo [<strong>pointer_default</strong>] y hay al menos un puntero de nivel no superior que se tratará como un puntero único. Para obtener más información, vea <a href="/windows/desktop/Rpc/default-pointer-types">tipos de puntero predeterminados</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>la interfaz no es compatible con el cálculo de referencias de automatización</dt> <dd> La interfaz no cumple los requisitos de una interfaz de automatización OLE. Compruebe para asegurarse de que la interfaz se deriva de <strong>IUnknown</strong> o <strong>IDispatch</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] solo el parámetro no puede ser un puntero a una estructura abierta</dt> <dd> Un parámetro [<a href="out-idl.md"><strong>out</strong></a>] solo se ha utilizado como un puntero a una estructura, lo que se conoce como estructura abierta, cuyo intervalo y tamaño transmitidos se determinan en tiempo de ejecución. El código auxiliar del servidor no sabe cuánto espacio se va a asignar para una estructura abierta. Use un puntero a un puntero a la estructura abierta y asegúrese de que la aplicación de servidor asigna espacio suficiente para ella.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] solo el parámetro no puede ser una cadena sin tamaño</dt> <dd> Una matriz con el atributo de cadena se ha declarado como un parámetro [<a href="out-idl.md"><strong>out</strong></a>] solo sin ninguna especificación de tamaño. El código auxiliar del servidor necesita información de tamaño para asignar memoria para la cadena. Puede quitar el atributo de cadena y agregar el atributo [<a href="size-is.md"><strong>size_is</strong></a>], o puede cambiar el parámetro a un parámetro [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>[out] el parámetro no es un puntero</dt> <dd> Todos los parámetros [<a href="out-idl.md"><strong>out</strong></a>] deben ser punteros, en consonancia con la Convención de llamada por valor del lenguaje de programación C. El parámetro direccional [<strong>out</strong>] indica que el servidor transmite un valor al cliente. Con la Convención llamada por valor, el servidor puede transmitir datos al cliente solo si el argumento de la función es un puntero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>la estructura de apertura no puede ser un parámetro</dt> <dd> Una estructura abierta contiene una matriz compatible como el último elemento. Una estructura o Unión se trunca cuando el último elemento de esa estructura o unión es una matriz compatible.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] el identificador de contexto/identificador genérico debe especificarse como un puntero a ese tipo de identificador</dt> <dd> Un parámetro de identificador de contexto o de identificador definido por el usuario con el atributo direccional [<a href="out-idl.md"><strong>out</strong></a>] debe ser un puntero a un puntero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>el identificador de contexto no debe derivar de un tipo que tenga el atributo [transmit_as]</dt> <dd> Los identificadores de contexto se deben transmitir como tipos de identificador de contexto. No se pueden transmitir como otros tipos y no se pueden derivar de [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>] o [<strong>user_marshal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>no se puede especificar un número variable de argumentos para un procedimiento remoto</dt> <dd> Las llamadas a procedimientos remotos que especifican un número variable de argumentos en tiempo de compilación no son compatibles con la definición de RPC de DCE. No se puede usar un número variable de argumentos en Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>el parámetro con nombre no puede ser &quot; void&quot;</dt> <dd> Un parámetro con el tipo de base <a href="void.md"><strong>void</strong></a> se especifica con un nombre.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>el parámetro deriva de &quot; CoClass &quot; o &quot; Module&quot;</dt> <dd> La <a href="coclass.md"><strong>coclase</strong></a> especifica un objeto de nivel superior que contiene interfaces e interfaces dispinterface. No se puede pasar como parámetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>solo el primer parámetro puede ser un identificador de enlace; debe especificar el modificador/ms_ext</dt> <dd> DCE RPC solo permite que el primer parámetro sea un identificador de enlace. Al compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> se desactiva el modificador predeterminado <a href="-ms-ext.md"><strong>/ms_ext</strong></a> que admite varios parámetros de identificador y se administran los parámetros en una posición distinta a la del extremo izquierdo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>no se puede usar [comm_status] en un parámetro y un tipo de valor devuelto</dt> <dd> Tanto el procedimiento como uno de sus parámetros tienen el atributo [<a href="comm-status.md"><strong>comm_status</strong></a>]. El atributo [<strong>comm_status</strong>] especifica que solo un objeto de datos a la vez puede ser de tipo <a href="error-status-t.md"><strong>error_status_t</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> el atributo [local] de un procedimiento requiere/ms_ext</dt> <dd> El atributo [<a href="local.md"><strong>local</strong></a>] es una extensión de Microsoft para DCE IDL. Para usar este atributo en una función, no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> El modificador <strong>/OSF</strong> invalida los modificadores y <a href="-ms-ext.md"><strong>ms_ext</strong></a> predeterminados del compilador MIDL y <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>los atributos de propiedad solo se pueden usar con procedimientos</dt> <dd> Uso inadecuado de un atributo [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>PROPPUT</strong></a>] o [<a href="propputref.md"><strong>PROPPUTREF</strong></a>]. Asegúrese de que ha escrito correctamente el nombre de función de la propiedad y que la propiedad y la función tienen el mismo nombre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>un procedimiento no puede tener más de un atributo de propiedad</dt> <dd> Como máximo, solo se puede especificar uno de los atributos [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>PROPPUT</strong></a>] o [<a href="propputref.md"><strong>PROPPUTREF</strong></a>] para una función.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>el procedimiento tiene una combinación no válida de atributos de operación</dt> <dd> Algunos atributos no se pueden usar en relación con otros atributos. Compruebe la referencia del lenguaje MIDL para conocer los requisitos y la sintaxis exactos de los atributos utilizados en este procedimiento.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>el campo que se deriva de una matriz compatible debe ser el último miembro de la estructura</dt> <dd> La estructura contiene una matriz compatible que no es el último elemento de la estructura. La matriz compatible debe aparecer como el último elemento de la estructura.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>etiqueta duplicada [case]</dt> <dd> Se ha especificado una etiqueta de caso duplicada. Se muestra la etiqueta duplicada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>no se especificó ningún caso [predeterminado] para la Unión discriminada</dt> <dd> Se ha especificado una Unión discriminada sin un caso predeterminado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>no se puede resolver la expresión de atributo</dt> <dd> No se puede resolver la expresión asociada con el atributo. Este error suele producirse cuando no se define una variable que aparece en la expresión. Por ejemplo, el error puede producirse si la variable <em>s</em> no está definida y la usa el atributo [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>la expresión de atributo debe ser de tipo entero, no admite expresiones de 64 bits</dt> <dd> La variable o expresión de atributo especificada debe ser un tipo entero. Este error se produce cuando el tipo de expresión de atributo no se resuelve como un entero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] requiere/ms_ext</dt> <dd> El atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] es una extensión de Microsoft para DCE IDL. Para usar este atributo no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que invalida los modificadores <a href="-ms-ext.md"><strong>/ms_ext</strong></a> predeterminados del compilador MIDL y <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] solo se puede aplicar a los parámetros out de tipo de puntero</dt> <dd> El atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] solo se puede aplicar a los parámetros [<a href="out-idl.md"><strong>out</strong></a>], y todos los parámetros [<strong>out</strong>] deben ser tipos de puntero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] no se puede especificar en un puntero a una matriz o estructura compatible</dt> <dd> El atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] no se puede aplicar a una matriz o estructura compatible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>el parámetro que especifica el recuento de bytes no es [in] solo o el parámetro de recuento de bytes no es [out].</dt> <dd> El valor asociado a [<a href="byte-count.md"><strong>byte_count</strong></a>] debe transmitirse desde el cliente al servidor; debe ser un parámetro [<a href="in.md"><strong>in</strong></a>]. No es necesario que el parámetro [<strong>byte_count</strong>] sea un parámetro [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>el parámetro que especifica el recuento de bytes no es un tipo entero</dt> <dd> El valor asociado con el recuento de bytes debe ser el tipo entero <a href="int.md"><strong>int</strong></a>, <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>o <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] no se puede especificar en un parámetro con atributos de tamaño</dt> <dd> El atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] no se puede usar con otros atributos de tamaño como [<a href="size-is.md"><strong>size_is</strong></a>] o [<a href="length-is.md"><strong>length_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>[case] la expresión no es constante</dt> <dd> La expresión especificada para la etiqueta Case no es una constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>[case] la expresión no es de tipo entero</dt> <dd> La expresión especificada para la etiqueta Case no es un tipo entero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>especificar [context_handle] en un tipo distinto de void * requiere/ms_ext</dt> <dd> Para la compatibilidad con DCE-RPC, el identificador de contexto debe ser un puntero de tipo <strong>void *</strong>. Si desea asociar los identificadores de contexto a tipos que no sean <strong>void *</strong>, no use el modificador de compilador de MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que invalida el modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a>predeterminado del compilador MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>no se puede especificar más de un parámetro con cada uno de los comm_status/fault_status</dt> <dd> Un procedimiento solo puede tener un parámetro con el atributo [<a href="comm-status.md"><strong>comm_status</strong></a>]. Puede tener como máximo un parámetro con el atributo [<a href="fault-status.md"><strong>fault_status</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>comm_status/fault_status parámetro debe ser un parámetro de puntero solo [out]</dt> <dd> Los tipos de código de error [<a href="comm-status.md"><strong>comm_status</strong></a>] y [<a href="fault-status.md"><strong>fault_status</strong></a>] se transmiten desde el servidor al cliente y, por tanto, se deben especificar como un parámetro [<a href="out-idl.md"><strong>out</strong></a>]. Debido a las restricciones en el lenguaje de programación C, todos los parámetros [<strong>out</strong>] deben ser punteros.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>error de sintaxis de extremo</dt> <dd> La sintaxis del punto de conexión es incorrecta.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>atributo no aplicable</dt> <dd> No se puede aplicar el atributo especificado en esta construcción. Por ejemplo, el atributo String se aplica a las matrices <a href="char-idl.md"><strong>Char</strong></a> o a los punteros <strong>Char</strong> y no se puede aplicar a una estructura formada por dos enteros <a href="short.md"><strong>cortos</strong></a> : <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[allocate] requiere/ms_ext</dt> <dd> El atributo <a href="allocate.md"><strong>allocate</strong></a> representa una extensión de Microsoft que no está definida como parte de DCE RPC. Para usar este atributo, no se puede compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , que invalida el modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a> predeterminado del compilador MIDL<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>modo [allocate] no válido</dt> <dd> Se ha especificado un modo no válido para la construcción de atributo [<a href="allocate.md"><strong>allocate</strong></a>]. Los cuatro modos válidos son single_node, all_nodes, on_null y siempre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>los atributos de longitud no se pueden aplicar con el atributo de cadena</dt> <dd> Cuando se usa el atributo de cadena, los archivos de código auxiliar generados llaman a la función <strong>strlen</strong> para determinar la longitud de la cadena. No use el atributo de longitud y el atributo de cadena para la misma variable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[last_is] y [length_is] no se pueden especificar al mismo tiempo</dt> <dd> Se han especificado ambos [<a href="last-is.md"><strong>last_is</strong></a>] y [<a href="length-is.md"><strong>length_is</strong></a>] para la misma matriz. Estos atributos se relacionan de la siguiente manera: length = Last First + 1. Dado que cada valor se puede derivar del otro, no especifique ambos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[max_is] y [size_is] no se pueden especificar al mismo tiempo</dt> <dd> Se han especificado ambos [ <a href="max-is.md"><strong>max_is</strong></a>] y [ <a href="size-is.md"><strong>size_is</strong></a>] para la misma matriz. Estos atributos se relacionan de la siguiente manera: Max = size + 1. Dado que cada valor se puede derivar del otro, no especifique ambos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>no se especificó ningún atributo [switch_is] al usar Union</dt> <dd> No se ha especificado ningún discriminante para la Unión. El atributo [<a href="switch-is.md"><strong>switch_is</strong></a>] indica el discriminante que se usa para seleccionar entre los campos de Unión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>no se especificó [UUID]</dt> <dd> No se ha especificado ningún UUID para la interfaz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[UUID] omitido en la interfaz [local]</dt> <dd> Al usar el atributo [<a href="local.md"><strong>local</strong></a>] en una interfaz de objeto, el compilador MIDL omite el atributo [<a href="uuid.md"><strong>UUID</strong></a>]. Los dos atributos no se pueden usar en una interfaz RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>no coinciden los tipos entre las expresiones de atributo de longitud y tamaño</dt> <dd> Las expresiones de atributo length y size deben ser de los mismos tipos. Por ejemplo, esta advertencia se emite cuando la variable de atributo para la expresión [<a href="size-is.md"><strong>size_is</strong></a>] es de tipo <strong>Long sin signo</strong> y la variable de atributo para la expresión [<a href="length-is.md"><strong>length_is</strong></a>] es de tipo <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>el atributo [String] debe especificarse &quot; como byte, &quot; &quot; Char &quot; o &quot; wchar_t &quot; matriz o puntero</dt> <dd> No se puede aplicar un atributo de cadena a un puntero o una matriz cuyo tipo base no sea un <a href="byte.md"><strong>byte</strong></a>, un <a href="char-idl.md"><strong>carácter</strong></a>o una <a href="struct.md"><strong>estructura</strong></a> en la que los miembros sean todos del tipo <strong>byte</strong> o <strong>Char</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>falta de coincidencia entre el tipo de la expresión [switch_is] y el tipo de modificador de la Unión.</dt> <dd> Si no se especifica la Unión [<a href="switch-type.md"><strong>switch_type</strong></a>], el tipo de conmutador es el mismo tipo que el campo [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] no debe aplicarse a un tipo que deriva de un identificador de contexto</dt> <dd> Los identificadores de contexto no se pueden transmitir como otros tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] debe especificar un tipo transmisible</dt> <dd> El tipo de [<a href="transmit-as.md"><strong>transmit_as</strong></a>] especificado deriva de un tipo que no se puede transmitir mediante Microsoft RPC, como <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>o <a href="int.md"><strong>int</strong></a>. Usar un tipo base RPC definido; en el caso de <strong>int</strong>, agregue especificadores de tamaño como <a href="small.md"><strong>pequeño</strong></a>, <a href="short.md"><strong>corto</strong></a>o <a href="long.md"><strong>largo</strong></a> para calificar el <strong>int</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>el tipo transmitido para [transmit_as] y [represent_as] no debe ser un puntero ni derivar de un puntero</dt> <dd> El tipo transmitido no puede ser un puntero ni derivar de un puntero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>el tipo presentado para [transmit_as] y [represent_as] no debe derivar de una matriz compatible/variable, su puntero equivalente o una estructura compatible/variable</dt> <dd> El tipo al que se ha aplicado [<a href="transmit-as.md"><strong>transmit_as</strong></a>] no puede derivar de una matriz o estructura compatible (una matriz o estructura cuyo tamaño se determina en tiempo de ejecución).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>el formato de [UUID] es incorrecto</dt> <dd> El formato de UUID no se ajusta a la especificación. El UUID debe ser una cadena que consta de cinco secuencias de dígitos hexadecimales con una longitud de 8, 4, 4, 4 y 12 dígitos. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; es un UUID válido. Use la función <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> o una utilidad para generar un UUID válido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>UUID no es un número hexadecimal</dt> <dd> El UUID especificado para la interfaz contiene caracteres que no son válidos en una representación de números hexadecimales. Los caracteres de 0 a 9 y de a a F son válidos en una representación hexadecimal.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>los parámetros opcionales deben aparecer después de los parámetros necesarios</dt> <dd> Para obtener una descripción de la ordenación de las listas de parámetros, vea [<a href="optional.md"><strong>Optional</strong></a>] en la referencia del lenguaje MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[DllName] obligatorio cuando se usa [Entry]</dt> <dd> Si va a especificar un punto de entrada en un archivo DLL, también debe especificar el nombre de ese archivo DLL mediante el atributo [<a href="dllname-str-.md"><strong>DllName</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[Bindable] no es válido sin [propget], [propput] o [PROPPUTREF]</dt> <dd> El atributo [<a href="bindable.md"><strong>Bindable</strong></a>] solo es válido en una propiedad, por lo que también debe especificar una de las funciones de acceso a propiedades o de configuración de propiedades.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>los procedimientos con [propput] o [PROPPUTREF] deben tener al menos un parámetro</dt> <dd> Un procedimiento [<a href="propput.md"><strong>PROPPUT</strong></a>] o [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>] debe tener al menos un parámetro [<a href="in.md"><strong>in</strong></a>] con la propiedad que se va a establecer. un procedimiento [<a href="propget.md"><strong>propget</strong></a>] debe tener al menos un parámetro [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retval</strong></a>] para recibir la propiedad o la referencia.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>el atributo [id] es obligatorio</dt> <dd> Esta función miembro, debido a la sintaxis de <a href="dispinterface.md"><strong>dispinterface</strong></a> usada, requiere un DISPID, que se especifica mediante el atributo [ <a href="id.md"><strong>ID</strong></a>]. Cuando se especifica una <strong>dispinterface</strong> mediante propiedades y métodos, se debe especificar un DISPID para cada propiedad y método.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>el nombre de interfaz especificado en ACF no coincide con el especificado en el archivo IDL</dt> <dd> En el modo de compilador actual, el nombre que sigue a la palabra clave interface en ACF debe ser el mismo que el nombre que sigue a la palabra clave interface en el archivo IDL. Los nombres de interfaz en los archivos IDL y ACF pueden ser diferentes cuando se compila con el modificador de compilador de MIDL <a href="-acf.md"><strong>/ACF</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>atributo duplicado</dt> <dd> Se han especificado atributos duplicados o en conflicto. Este error suele producirse cuando dos atributos son mutuamente excluyentes. Por ejemplo, los atributos [<a href="code.md"><strong>code</strong></a>] y [<a href="nocode.md"><strong>nocode</strong></a>] no se pueden usar al mismo tiempo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>el parámetro con el atributo [comm_status] o [fault_status] debe ser un puntero al tipo error_status_t</dt> <dd> Cuando se usa [<a href="fault-status.md"><strong>fault_status</strong></a>] o [<a href="comm-status.md"><strong>comm_status</strong></a>] como atributo de parámetro, el parámetro debe ser un parámetro [<a href="out-idl.md"><strong>out</strong></a>] de tipo <a href="error-status-t.md"><strong>error_status_t</strong></a>. Si se produce un error de servidor, el parámetro se establece en el código de error. Cuando la llamada remota se completa correctamente, el procedimiento establece el valor.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>no se puede especificar un procedimiento [local] en el archivo ACF</dt> <dd> Se ha especificado un procedimiento local en ACF. El procedimiento local solo puede especificarse en el archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>el tipo especificado no está definido como identificador</dt> <dd> El tipo especificado en el atributo [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>] no está definido como un tipo de identificador. Cambie la definición de tipo o el nombre de tipo especificado por el atributo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>procedimiento sin definir</dt> <dd> Se ha aplicado un atributo a un procedimiento de ACF y ese procedimiento no está definido en el archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>Este parámetro no existe en el archivo IDL</dt> <dd> Un parámetro especificado en ACF no existe en la definición del archivo IDL. Todos los parámetros, las funciones y las definiciones de tipo que aparecen en ACF deben corresponder a los parámetros, las funciones y los tipos definidos anteriormente en el archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>no se admite esta construcción de límites de matriz.</dt> <dd> MIDL admite actualmente la compresión de los límites superior e inferior de una matriz en la matriz de formulario [Lower.. Upper] solo cuando la constante que especifica el límite inferior de la matriz se resuelve en el valor cero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>la especificación del límite de la matriz no es válida</dt> <dd> La especificación del usuario de los límites de matriz para la matriz de tamaño fijo no es válida. Por ejemplo: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>no se admite el puntero a una matriz compatible o a una matriz que contiene una matriz compatible</dt> <dd> Uso de matriz compatible no válido. Para ver las reglas que rigen las matrices compatibles, vea <a href="/windows/desktop/Rpc/arrays-and-rpc">matrices y RPC</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>el puntero/matriz no deriva ningún tamaño</dt> <dd> Se ha especificado una matriz compatible sin ninguna especificación de tamaño. Puede especificar el tamaño con el atributo [<a href="max-is.md"><strong>max_is</strong></a>] o [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>solo las matrices fijas y SafeArray son válidas en una biblioteca de tipos</dt> <dd> Ha utilizado un tipo de matriz dentro de una instrucción de biblioteca que no se puede usar en una biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>Las SafeArray solo son válidas dentro de un bloque de biblioteca</dt> <dd> El compilador MIDL no reconoce un SAFEARRAY como un tipo de datos válido, excepto cuando se genera una biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>constante de caracteres con formato incorrecto</dt> <dd> No se permite el carácter de fin de línea en constantes de caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>se encontró el final del archivo en el comentario</dt> <dd> Se ha encontrado el carácter de final de archivo en un comentario.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>se encontró el final del archivo en la cadena</dt> <dd> Se ha encontrado el carácter de final de archivo en una cadena.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>la longitud del identificador supera los 31 caracteres</dt> <dd> Los identificadores se limitan a 31 caracteres alfanuméricos. Los nombres de identificador de más de 31 caracteres se truncan.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>se encontró el final de la línea en la cadena</dt> <dd> Se ha encontrado el carácter de final de línea en la cadena. Compruebe que ha incluido el carácter de comilla doble que termina la cadena.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>la constante de cadena supera el límite de 255 caracteres</dt> <dd> La cadena superó la longitud máxima permitida de 255 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>el identificador supera el límite de 255 caracteres y se ha truncado</dt> <dd> El identificador superó la longitud máxima permitida de 255 caracteres. Se truncan los caracteres sobrantes en el identificador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>constante demasiado grande</dt> <dd> La constante es demasiado grande para representarse internamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>error de análisis numérico</dt> <dd> El compilador no pudo analizar el identificador numérico.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>Error al abrir el archivo</dt> <dd> El sistema operativo ha detectado un error al intentar abrir un archivo de salida. Este error puede deberse a un nombre demasiado largo para el sistema de archivos o por un nombre de archivo duplicado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>Error al enlazar con la función<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>Error al inicializar OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>Error al cargar la biblioteca<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] solo el parámetro no debe derivar de un puntero o matriz de nivel superior [Unique] o [PTR]</dt> <dd> Un puntero único no puede ser un parámetro [<a href="out-idl.md"><strong>out</strong></a>] solo. Por definición, un puntero único puede cambiar de <strong>null</strong> a un valor distinto de<strong>null</strong>. No se pasa información sobre el parámetro [<strong>out</strong>] solo del cliente al servidor.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>el atributo no es aplicable a esta Unión no rpcable</dt> <dd> Solo los atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] y [<a href="switch-type.md"><strong>switch_type</strong></a>] se aplican a una Unión que se transmite como parte de una llamada a procedimiento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>la expresión usada para un atributo de tamaño no debe derivar de un parámetro [out] solo.</dt> <dd> El valor de un parámetro [<a href="out-idl.md"><strong>out</strong></a>] solo no se transmite al servidor y no se puede usar para determinar la longitud o el tamaño del parámetro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>la expresión usada para un atributo de longitud para un parámetro [in] no puede derivar de un parámetro [out] solo.</dt> <dd> El valor de un parámetro [<a href="out-idl.md"><strong>out</strong></a>] solo no se transmite al servidor y no se puede usar para determinar la longitud o el tamaño del parámetro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>uso de &quot; las &quot; necesidades int/c_ext</dt> <dd> MIDL es un lenguaje fuertemente tipado. Todos los parámetros transmitidos a través de la red deben derivarse de uno de los tipos base de MIDL. El tipo <a href="int.md"><strong>int</strong></a> no está definido como parte de MIDL. Los datos transmitidos deben incluir un especificador de tamaño: <a href="small.md"><strong>pequeño</strong></a>, <strong>corto</strong>o <strong>largo</strong>. Los datos que no se transmiten a través de la red se pueden incluir en una interfaz; Use el modificador <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>el campo struct/union no debe ser &quot; void&quot;</dt> <dd> Los campos de una estructura o Unión deben declararse como un tipo base específico admitido por MIDL o un tipo que se deriva de los tipos base. No se permiten tipos void en operaciones remotas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>el elemento de matriz no debe ser void</dt> <dd> Un elemento de matriz no puede ser nulo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>uso de calificadores de tipo y/o modificadores necesarios/c_ext</dt> <dd> Los modificadores de tipo como <strong>_cdecl</strong> y <strong>_far</strong> solo se pueden compilar si se especifica el modificador <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>el campo struct/union no debe derivar de una función</dt> <dd> Los campos de una estructura o Unión deben ser tipos o tipos base de MIDL que se derivan de estos tipos base. Las funciones no son válidas en los campos de estructura o Unión.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>el elemento de matriz no debe ser una función</dt> <dd> Un elemento de matriz no puede ser una función.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>el parámetro no debe ser una función</dt> <dd> El parámetro de un procedimiento remoto debe ser una variable de un tipo especificado. Una función no puede ser un parámetro del procedimiento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>struct/union con campos de bits necesarios/c_ext</dt> <dd> Debe especificar el modificador de compilador de MIDL <a href="-c-ext.md"><strong>/c_ext</strong></a> para permitir campos de bits en estructuras que no se transmiten en una llamada a procedimiento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>Especificación de campo de bits en un tipo distinto de &quot; int &quot; es una extensión que no es compatible con ANSI</dt> <dd> La especificación del lenguaje de programación ANSI C no permite aplicar campos de bits a tipos no enteros.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>la especificación de campo de bits solo se puede aplicar a tipos simples y enteros</dt> <dd> La especificación del lenguaje de programación ANSI C no permite aplicar campos de bits a tipos no enteros.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>el campo struct/union no debe derivar de handle_t ni de un identificador de contexto</dt> <dd> Los identificadores de contexto no se pueden transmitir como parte de otra estructura. Se deben transmitir como identificadores de contexto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>el elemento de matriz no debe derivar de handle_t ni de un identificador de contexto</dt> <dd> Los identificadores de contexto no se pueden transmitir como parte de una matriz.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>Esta especificación de necesidades de Unión/c_ext</dt> <dd> Una Unión que aparece en la definición de interfaz debe estar asociada a discriminante o declarada como local. Los datos que no se transmiten a través de la red se pueden declarar implícitamente como locales cuando se usa el modificador <a href="-c-ext.md"><strong>/c_ext</strong></a> , que es el valor predeterminado de MIDL. No se puede compilar este IDL con el modificador <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>el parámetro que se deriva de un &quot; int &quot; debe tener un especificador de tamaño &quot; Small, &quot; &quot; Short &quot; o &quot; Long &quot; con el valor &quot; int&quot;</dt> <dd> El tipo <a href="int.md"><strong>int</strong></a> solo es un tipo de MIDL válido en plataformas de 32 bits, en los sistemas de 16 bits <strong>int</strong> debe ir acompañado de una especificación de tamaño. Use uno de los especificadores de tamaño <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>o <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>el tipo del parámetro no puede derivar de void o void *</dt> <dd> MIDL es un lenguaje fuertemente tipado. Todos los parámetros transmitidos a través de la red deben derivarse de uno de los tipos base de MIDL. MIDL no admite <a href="void.md"><strong>void</strong></a> como tipo base. Debe cambiar la declaración a un tipo de MIDL válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>no se admite el parámetro que deriva de una estructura o unión que contiene campos de bits</dt> <dd> Los campos de bits no se definen como un tipo de datos válido mediante el RPC de DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>uso de un parámetro que deriva de un tipo que contiene los modificadores de tipo o los calificadores de tipo y c_ext</dt> <dd> El uso de palabras clave como <strong>Far</strong>, <strong>Near</strong>, <a href="const.md"><strong>const</strong></a>y <strong>volatile</strong> en el archivo IDL es una extensión de Microsoft para DCE RPC. Estas palabras clave no están disponibles al compilar con el modificador <a href="-osf.md"><strong>/OSF</strong></a> , lo que desactiva el modificador de extensión default <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>el parámetro no debe derivar de un puntero a una función</dt> <dd> Las bibliotecas en tiempo de ejecución de RPC transmiten un puntero y sus datos asociados entre el cliente y el servidor. Los punteros a funciones no se pueden transmitir como parámetros porque la función no se puede transmitir a través de la red.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>el parámetro no debe derivar de una Unión compatible con nonrpc</dt> <dd> La Unión debe estar asociada a un discriminante. Use los atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] y [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>el tipo de valor devuelto deriva de un &quot; entero. &quot; Debe utilizar especificadores de tamaño con el valor &quot; int&quot;</dt> <dd> En los sistemas de 16 bits, el tipo <a href="int.md"><strong>int</strong></a> no es un tipo de MIDL válido a menos que esté acompañado por una especificación de tamaño. Use uno de los especificadores de tamaño <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>o <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>el tipo de valor devuelto no debe derivar de un puntero void</dt> <dd> MIDL es un lenguaje fuertemente tipado. Todos los parámetros transmitidos a través de la red deben derivarse de uno de los tipos base de MIDL. Los tipos void no se definen como parte de MIDL. Debe cambiar la declaración a un tipo de MIDL válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>el tipo de valor devuelto no debe derivar de una estructura o unión que contenga campos de bits</dt> <dd> Los campos de bits no se definen como un tipo de datos válido mediante el RPC de DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>el tipo de valor devuelto no debe derivar de una Unión compatible con nonrpc</dt> <dd> La Unión debe estar asociada a un discriminante. Use los atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] y [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>el tipo de valor devuelto no debe derivar de un puntero a una función</dt> <dd> Las bibliotecas en tiempo de ejecución de RPC transmiten un puntero y sus datos asociados entre el cliente y el servidor. Los punteros a funciones no se pueden transmitir como parámetros porque RPC no define un método para transmitir la función asociada a través de la red.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>no se admiten los inicializadores compuestos.</dt> <dd> DCE RPC solo admite la inicialización simple. No se puede inicializar la estructura o matriz en el archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Los atributos ACF del archivo IDL necesitan el modificador/app_config</dt> <dd> Una extensión de Microsoft le permite especificar atributos ACF en el archivo IDL. Use el modificador <a href="-app-config.md"><strong>/app_config</strong></a> para activar esta extensión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>los comentarios de una sola línea/ms_ext o/c_ext</dt> <dd> Los comentarios de una sola línea que usan dos caracteres de barra diagonal (//) representan una extensión de Microsoft para el RPC de DCE. No puede usar comentarios de una sola línea si está compilando con el modificador <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>el formato de [versión] es incorrecto</dt> <dd> El número de versión de la interfaz en el encabezado de la interfaz debe especificarse en el formato <em>principal</em>. <em>secundaria</em>, donde cada número puede oscilar entre 0 y 65535.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;&quot;necesidades y ms_ext firmadas o/c_ext</dt> <dd> El uso de la palabra clave <a href="signed.md"><strong>signed</strong></a> es una extensión de Microsoft para DCE RPC. No puede usar el modificador <a href="-osf.md"><strong>/OSF</strong></a> si desea utilizar esta característica.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>no coincide en el tipo de asignación</dt> <dd> El tipo de la variable no coincide con el tipo del valor asignado a la variable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>la declaración debe tener el formato: const <type><declarator> = <initializing expression></dt> <dd> La declaración no es compatible con la sintaxis de DCE RPC. Utilice el modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a> o <a href="-c-ext.md"><strong>/c_ext</strong></a> modo de compilador de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>la declaración debe tener &quot; const&quot;</dt> <dd> Las declaraciones del archivo IDL deben ser expresiones constantes que utilicen la palabra clave <a href="const.md"><strong>const</strong></a>, por ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>struct/union/ENUM no se deben definir en una especificación de tipo de parámetro</dt> <dd> La estructura, la Unión o el tipo enumerado se deben indicar explícitamente fuera del prototipo de función.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>el atributo [allocate] debe aplicarse solo en tipos de puntero no void</dt> <dd> El atributo [<a href="allocate.md"><strong>allocate</strong></a>] está diseñado para estructuras de datos complejas basadas en punteros. Cuando se especifica el atributo [allocate], el archivo de código auxiliar atraviesa la estructura de datos para calcular el tamaño total de todos los objetos a los que se puede tener acceso desde el puntero y todos los demás punteros de la estructura de datos. Cambie el tipo a un tipo de puntero no nulo o quite el atributo [<strong>allocate</strong>] y use otro método para determinar su tamaño de asignación, como el operador <strong>sizeof</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>una construcción de puntero de matriz o equivalente no puede derivar de una Unión no encapsulada</dt> <dd> Cada unión debe estar asociada a un discriminante. No se permiten matrices de uniones porque no proporcionan el discriminante asociado. Matrices de estructuras en las que la estructura empaqueta la Unión y su discriminante se permiten porque el código auxiliar puede usar discriminante para determinar el tamaño de cada unión.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>el campo no debe derivar de un tipo de error_status_t</dt> <dd> El tipo de <a href="error-status-t.md"><strong>error_status_t</strong></a> solo se puede usar como un parámetro o un tipo de valor devuelto. No se puede incrustar en el campo de una estructura o Unión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>la Unión tiene al menos un brazo sin etiqueta de caso</dt> <dd> La declaración Union no coincide con la sintaxis MIDL necesaria para la Unión. Cada ARM de Unión requiere una etiqueta de caso o una etiqueta predeterminada que seleccione el brazo de la Unión.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>el parámetro o el valor devuelto no se debe derivar de un tipo que tenga aplicado [ignore]</dt> <dd> El atributo [<a href="ignore.md"><strong>Ignore</strong></a>] es un atributo de campo que solo se puede aplicar a campos, como campos de estructuras y matrices. El atributo [<strong>Ignore</strong>] indica que el código auxiliar no debe desreferenciar el puntero durante la transmisión y no se permite cuando entra en conflicto con otros atributos que se deben desreferenciar, como los parámetros [<a href="out-idl.md"><strong>out</strong></a>] y los valores devueltos de función.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>el puntero ya tiene un atributo de puntero aplicado</dt> <dd> Solo uno de los atributos de puntero, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>Unique</strong></a>] o [<a href="ptr.md"><strong>ptr</strong></a>], se puede aplicar a un único puntero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>el campo/parámetro no debe derivar de una estructura recursiva a través de un puntero de referencia</dt> <dd> Por definición, un puntero de referencia no se puede establecer en <strong>null</strong>. Una estructura de datos recursiva definida con un puntero de referencia no tiene elementos <strong>nulos</strong> y por Convención no está terminando. Use un atributo de puntero [<a href="unique.md"><strong>Unique</strong></a>] para permitir que la estructura de datos especifique un elemento <strong>null</strong> o vuelva a definir la estructura de datos como una estructura de datos no recursiva.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>uso de un campo que deriva de un puntero void necesita/c_ext</dt> <dd> El tipo <strong>void *</strong> y otros tipos y calificadores de tipo que no son compatibles con DCE IDL solo se permiten en el archivo IDL cuando se utiliza la configuración predeterminada del compilador de MIDL. El uso del modificador <a href="-osf.md"><strong>/OSF</strong></a> invalida este valor predeterminado. Si debe compilar en modo de compatibilidad de OSF, deberá volver a definir el tipo de puntero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>uso de este atributo ms_ext necesarias</dt> <dd> Esta característica de lenguaje es una extensión de Microsoft para DCE IDL. No puede usar esta característica si está compilando en el modo de compatibilidad de OSF ( <a href="-osf.md"><strong>/OSF</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>Este atributo solo se permite con las nuevas bibliotecas de tipos de formato</dt> <dd> Para usar este atributo, necesita la versión de Oleaut32.dll que se proporciona con Windows 2000 o posterior.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>uso de wchar_t necesidades/ms_ext o/c_ext</dt> <dd> El tipo de caracteres anchos representa una extensión para DCE IDL. El compilador MIDL no acepta el tipo de caracteres anchos cuando se especifica el modificador <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>los campos sin nombre necesitan/ms_ext o/c_ext</dt> <dd> DCE IDL no admite el uso de estructuras o uniones sin nombre incrustadas en otras estructuras o uniones. En DCE IDL, todos estos campos incrustados deben tener nombre. El compilador MIDL no permite su uso al especificar el modificador <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>los campos sin nombre solo se pueden derivar de tipos struct/union</dt> <dd> La extensión de Microsoft para el IDL de DCE que admite campos sin nombre solo se aplica a las estructuras y uniones. Debe asignar un nombre al campo o redefinir el campo para que cumpla esta restricción.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>el campo de una Unión no puede derivar de una matriz variable o de un puntero equivalente</dt> <dd> La matriz compatible no puede aparecer solo en la Unión, pero debe ir acompañada del valor que especifica el tamaño de la matriz. En lugar de usar la matriz como ARM de Unión, use una estructura que conste de la matriz compatible y el identificador que especifica su tamaño.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>no se especificó ningún atributo [pointer_default], se supone [PTR] para todos los punteros sin atributos de la interfaz</dt> <dd> La implementación de DCE IDL especifica que todos los punteros de cada archivo IDL deben estar asociados a atributos de puntero. Cuando no se asigna un atributo de puntero explícito al tipo de parámetro o de puntero y no se especifica ningún atributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>] en el archivo IDL, el atributo <a href="ptr.md"><strong>ptr</strong></a> de puntero completo se asocia con el puntero. Puede cambiar los atributos de puntero mediante atributos de puntero explícitos, especificando un atributo [<strong>pointer_default</strong>] o especificando el modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a> para cambiar el valor predeterminado de los punteros sin atributos a [<a href="unique.md"><strong>Unique</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>la expresión de inicialización debe resolverse como una expresión constante</dt> <dd> Si se usa una expresión como inicializador, la expresión debe ser una expresión constante. Esto es cierto en todos los modos de compilador de MIDL. La expresión debe poder resolverse en tiempo de compilación. Especifique una constante literal o una expresión que se resuelva como una constante, en lugar de una variable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>la expresión de atributo debe ser de tipo entero, Char, Boolean o enum</dt> <dd> El tipo especificado no se resuelve en un tipo de modificador válido. Use un entero, un carácter, un <a href="byte.md"><strong>byte</strong></a>, un <a href="boolean.md"><strong>valor booleano</strong></a>o un tipo de <a href="enum.md"><strong>enumeración</strong></a> , o un tipo que se derive de uno de estos tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>constante no válida</dt> <dd> La constante especificada está fuera del intervalo válido para el tipo especificado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>atributo no implementado; tendrán</dt> <dd> El atributo especificado no está implementado en esta versión de Microsoft RPC. El compilador MIDL continúa procesando el archivo IDL como si el atributo no estuviera presente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>el tipo de valor devuelto no debe derivar de un puntero [Ref]</dt> <dd> Los valores devueltos de la función que se definen como tipos de puntero deben especificarse como [<a href="unique.md"><strong>Unique</strong></a>] o como punteros <a href="ptr.md"><strong>completos</strong></a> . No se pueden usar punteros de referencia.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>la expresión de atributo debe ser un nombre de variable o una expresión de desreferencia de puntero en este modo. Debe especificar el modificador/ms_ext</dt> <dd> El compilador de DCE IDL requiere que el tamaño asociado al atributo [<a href="size-is.md"><strong>size_is</strong></a>] lo especifique una variable o una variable de puntero. Si desea aprovechar la extensión de Microsoft que permite definir el atributo [<strong>size_is</strong>] mediante una expresión constante, no puede usar el modificador de compilador <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>el parámetro no debe derivar de una Unión no encapsulada recursiva</dt> <dd> Una Unión debe incluir un discriminante, por lo que una Unión no puede tener otra unión como elemento. Una Unión se puede incrustar en otra unión solo cuando forma parte de una estructura que incluye discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>el parámetro de identificador de enlace no puede ser [out] solo</dt> <dd> El parámetro de identificador identificado por el compilador MIDL como identificador de enlace para esta operación debe ser un parámetro [<a href="in.md"><strong>in</strong></a>]. [<a href="out-idl.md"><strong>out</strong></a>]: solo los parámetros no están definidos en el código auxiliar del cliente y el identificador de enlace debe definirse en el cliente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>el puntero a un identificador no puede ser [Unique] o [PTR]</dt> <dd> No puede usar los atributos de puntero único y completo para un puntero a un identificador. Estos atributos permiten el valor <strong>null</strong>y el identificador de enlace no puede ser <strong>null</strong>. Use el atributo [<a href="ref.md"><strong>ref</strong></a>] para derivar el parámetro de identificador de enlace de los punteros de referencia.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>un parámetro que no es un identificador de enlace no debe derivar de handle_t</dt> <dd> El tipo de identificador primitivo <a href="handle-t.md"><strong>handle_t</strong></a> no es un tipo de datos válido que se transmite a través de la red. Cambie el tipo de parámetro a un tipo distinto de <strong>handle_t</strong>o quite el parámetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>se encontró un final de archivo inesperado</dt> <dd> El compilador MIDL encontró el final del archivo antes de poder resolver correctamente todos los elementos sintácticos del archivo. Compruebe que el carácter de llave de cierre (}) está presente al final del archivo o Compruebe la sintaxis.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>el tipo que se deriva de handle_t no debe tener [transmit_as] aplicado</dt> <dd> El tipo de controlador primitivo <a href="handle-t.md"><strong>handle_t</strong></a> no se transmite a través de la red.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] no debe aplicarse a un tipo al que se le ha aplicado [identificador]</dt> <dd> Los atributos [<a href="context-handle.md"><strong>context_handle</strong></a>] y [<a href="handle.md"><strong>Handle</strong></a>] no se pueden aplicar al mismo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[Handle] no debe especificarse en un tipo que derive de void o void *</dt> <dd> Un tipo especificado con el atributo [<a href="handle.md"><strong>Handle</strong></a>] se puede transmitir a través de la red, pero el tipo <strong>void *</strong> no es un tipo transmisible. El tipo de identificador debe resolverse en un tipo que se deriva de los tipos base transmisibles.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>el parámetro debe tener [in], [out] o [in, out] en este modo. Debe especificar/ms_ext o/c_ext</dt> <dd> El compilador de DCE IDL requiere que todos los parámetros tengan parámetros de dirección explícitos. Para usar las extensiones de Microsoft para DCE IDL, no puede usar el modificador <a href="-osf.md"><strong>/OSF</strong></a> , que invalida <a href="-ms-ext.md"><strong>/ms_ext</strong></a> y <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>el tipo transmitido no puede derivar de &quot; void &quot; para [transmit_as], [represent_as], [wire_marshal], [user_marshal]</dt> <dd> El atributo [<a href="transmit-as.md"><strong>transmit_as</strong></a>] solo se aplica a los tipos de puntero. Use el tipo <strong>void *</strong> en lugar de <a href="void.md"><strong>void</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; debe especificarse en la primera y única especificación de parámetro</dt> <dd> La palabra clave <a href="void.md"><strong>void</strong></a> aparece incorrectamente con otros parámetros de función. Para especificar una función sin parámetros, la palabra clave <strong>void</strong> debe ser el único elemento de la lista de parámetros, como en el ejemplo siguiente:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] debe especificarse solo en un tipo que derive de una Unión no encapsulada</dt> <dd> La palabra clave [<a href="switch-is.md"><strong>switch_is</strong></a>] no se aplica correctamente. Solo se puede usar con <a href="nonencapsulated-unions.md">tipos de Unión no encapsulados</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>las estructuras que admiten cadenas no se implementan en esta versión</dt> <dd> DCE IDL permite que el atributo [<a href="string.md"><strong>String</strong></a>] se aplique a una estructura cuyos elementos solo se componen de caracteres, bytes o tipos que se resuelven en caracteres o bytes. Esta funcionalidad no se admite en Microsoft RPC. El atributo [<strong>String</strong>] no se puede aplicar a la estructura en conjunto. Sin embargo, se puede aplicar a cada matriz individual.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>el tipo de modificador solo puede ser integral, Char, Boolean o enum</dt> <dd> El tipo especificado no se resuelve en un tipo de modificador válido. Use un entero, un carácter, un <a href="byte.md"><strong>byte</strong></a>, un <a href="boolean.md"><strong>valor booleano</strong></a>, un tipo de <a href="enum.md"><strong>enumeración</strong></a> o un tipo derivado de uno de estos tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[Handle] no debe especificarse en un tipo que derive de handle_t</dt> <dd> Un tipo de identificador debe definirse con uno y solo uno de los tipos o atributos de identificador. Use el tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> o el atributo [<a href="handle.md"><strong>Handle</strong></a>], pero no ambos. El tipo de identificador definido por el usuario debe ser transmisible, pero el tipo de <strong>handle_t</strong> no se transmite en la red.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>el parámetro que deriva de handle_t no debe ser un parámetro [out]</dt> <dd> Un identificador del tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> solo es significativo para el lado de la aplicación en el que se define. El tipo <strong>handle_t</strong> no se transmite en la red.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>la expresión de atributo deriva de la desreferenciación de puntero [Unique] o [PTR]</dt> <dd> Aunque los atributos de puntero completo (<a href="unique.md"><strong>únicos</strong></a>) y de punteros <a href="ptr.md"><strong>completos</strong></a> permiten que los punteros tengan valores <strong>null</strong> , la expresión que define el atributo de tamaño o longitud nunca debe tener un valor <strong>null</strong> . Cuando se usan punteros, MIDL restringe las expresiones a los punteros [<a href="ref.md"><strong>ref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; requiere/ms_ext</dt> <dd> El atributo <a href="cpp-quote.md"><strong>cpp_quote</strong></a> es una extensión de Microsoft a DCE IDL. No use el modificador de compilador de MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que invalida <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>UUID entre comillas requiere/ms_ext</dt> <dd> La capacidad de especificar un valor de UUID entre comillas es una extensión de Microsoft para DCE IDL. No use el modificador de compilador de MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que invalida <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>el tipo de valor devuelto no puede derivar de una Unión no encapsulada</dt> <dd> No se puede usar la Unión no encapsulada como un tipo de valor devuelto de función. Para devolver el tipo de Unión, especifique el tipo de Unión como parámetro [<a href="out-idl.md"><strong>out</strong></a>] o [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>el tipo de valor devuelto no puede derivar de una estructura compatible</dt> <dd> El tamaño del tipo de valor devuelto debe ser una constante. No se puede especificar como tipo de valor devuelto una estructura que contiene una matriz compatible incluso cuando la estructura también incluye su especificador de tamaño. Para devolver la estructura compatible, especifique la estructura como un parámetro [<a href="out-idl.md"><strong>out</strong></a>] o [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] no debe aplicarse a un tipo que derive de un identificador genérico</dt> <dd> En esta versión, los atributos [<a href="handle.md"><strong>Handle</strong></a>] y [<a href="transmit-as.md"><strong>transmit_as</strong></a>] no se pueden combinar en el mismo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[Handle] no debe aplicarse a un tipo al que se le ha aplicado [transmit_as]</dt> <dd> En esta versión, los atributos [<a href="handle.md"><strong>Handle</strong></a>] y [<a href="transmit-as.md"><strong>transmit_as</strong></a>] no se pueden combinar en el mismo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>el tipo especificado para la declaración const no es válido</dt> <dd> Las declaraciones de constantes se limitan a tipos enteros, de caracteres, de caracteres anchos, de cadena y booleanos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>no se admite el operando del operador sizeof.</dt> <dd> El compilador MIDL admite la operación <strong>sizeof</strong> solo para tipos simples. El operando especificado no se evalúa como un tipo entero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>Este nombre ya se usa como nombre de identificador const</dt> <dd> El identificador se ha utilizado previamente para identificar una constante en una declaración <a href="const.md"><strong>const</strong></a> . Cambie el nombre de uno de los identificadores para que los identificadores sean únicos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>redefinición incoherente del tipo error_status_t</dt> <dd> El tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> debe resolverse en el tipo <strong>Long sin signo</strong>. No se pueden usar otras definiciones de tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case] valor fuera del intervalo de tipo de conmutador</dt> <dd> El valor asociado al caso de la instrucción switch está fuera del intervalo para el tipo de modificador especificado. Por ejemplo, este error se produce cuando se usa un valor entero largo en la instrucción Case para un tipo de entero corto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>parámetro que deriva de wchar_t necesita/ms_ext</dt> <dd> El tipo de caracteres anchos <a href="wchar-t.md"><strong>wchar_t</strong></a> es una extensión de Microsoft a DCE IDL. No use el modificador de compilador de MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que invalida <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>Esta interfaz solo tiene devoluciones de llamada</dt> <dd> Las devoluciones de llamada solo son válidas en el contexto de una llamada a procedimiento remoto. La interfaz debe incluir al menos un prototipo de función para una llamada a procedimiento remoto que no incluya el atributo [<a href="callback.md"><strong>callback</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>atributo especificado de redundante; tendrán</dt> <dd> El atributo especificado se ha aplicado más de una vez. Se omiten varias instancias del mismo atributo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>tipo de identificador de contexto usado para un identificador implícito</dt> <dd> Un tipo definido mediante el atributo [<a href="context-handle.md"><strong>context_handle</strong></a>] se ha especificado como el tipo de identificador en un atributo [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>]. Los atributos no se pueden combinar de esta manera.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>opciones en conflicto especificadas para [allocate]</dt> <dd> Las opciones especificadas para el atributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] representan directivas en conflicto. Por ejemplo, especifique la opción all_nodes o la opción single_node, pero no ambas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>Error al escribir en el archivo</dt> <dd> Error al escribir en el archivo. Esta condición puede deberse a errores relacionados con el espacio en disco, los identificadores de archivos, las restricciones de acceso a archivos y los errores de hardware.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>no se encontró ningún tipo de conmutador en la definición de Union, con el tipo [switch_is]</dt> <dd> La definición de Unión no incluye un atributo [<a href="switch-type.md"><strong>switch_type</strong></a>] explícito. El tipo de la variable especificada por el atributo [<a href="switch-is.md"><strong>switch_is</strong></a>] se utiliza como tipo de modificador.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>comprobación semántica incompleta debido a errores anteriores</dt> <dd> El compilador MIDL hace dos pasos sobre los archivos de entrada para resolver las declaraciones adelantadas. Debido a los errores detectados durante el primer paso, no se ha realizado la comprobación de la segunda fase. Los errores no notificados relativos a las declaraciones adelantadas pueden seguir estando presentes en el archivo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>no se admite el parámetro Handle o el tipo de valor devuelto en un procedimiento [callback]</dt> <dd> Un procedimiento [<a href="callback.md"><strong>callback</strong></a>] se produce en el contexto de una llamada de un cliente al servidor y usa el mismo identificador de enlace que la llamada original. No se permiten parámetros explícitos de identificador de enlace o tipos de valor devuelto en funciones de devolución de llamada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[PTR] no admite el alias en esta versión</dt> <dd> Un alias se produce cuando se puede obtener acceso a los datos a través de más de un puntero o nombre de variable. Quite el alias. Para obtener más información, vea <a href="/windows/desktop/Rpc/unique-pointers">punteros únicos</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>el parámetro ya se ha definido como un identificador de contexto</dt> <dd> El parámetro se definió previamente como un identificador de contexto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] no debe derivarse de handle_t</dt> <dd> Las tres características de identificador: el tipo <a href="handle-t.md"><strong>handle_t</strong></a>, el atributo [<a href="handle.md"><strong>identificador</strong></a>] y el atributo [<a href="context-handle.md"><strong>context_handle</strong></a>], son mutuamente excluyentes. Solo se puede aplicar una característica a un tipo o parámetro cada vez.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>el tamaño de la matriz supera los 65536 bytes</dt> <dd> En algunas plataformas de Microsoft, el tamaño máximo de los datos transmisibles es 64K. Rediseñe la aplicación para que todos los datos transmitidos quepan dentro del tamaño máximo transmisible.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>el tamaño de la estructura supera los 65536 bytes</dt> <dd> En algunas plataformas de Microsoft, el tamaño máximo de los datos transmisibles es 64K. Rediseñe la aplicación para que todos los datos transmitidos quepan dentro del tamaño máximo transmisible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>el campo de una Unión no encapsulada no puede ser otra unión no encapsulada</dt> <dd> Las uniones que se transmiten como parte de una llamada a procedimiento remoto requieren un elemento de datos asociado, discriminante, que selecciona el brazo de la Unión. Las uniones anidadas en otras uniones no ofrecen un discriminante; como resultado, no se pueden transmitir en este formulario. Cree una estructura que conste de la Unión y de su discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>atributos de puntero aplicados en una matriz incrustada; tendrán</dt> <dd> Un atributo de puntero solo se puede aplicar a una matriz cuando la matriz es un parámetro de nivel superior. Se omiten otros atributos de puntero aplicados a matrices incrustadas en otras estructuras de datos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[allocate] no es válido en el tipo transmitido o presentado para [transmit_as], [represent_as], [wire_marshal] o [user_marshal]</dt> <dd> Los atributos [<a href="transmit-as.md"><strong>transmit_as</strong></a>] y [<a href="allocate.md"><strong>allocate</strong></a>] no se pueden aplicar a la vez al mismo tipo. El atributo [<strong>transmit_as</strong>] distingue entre los tipos presentados y transmitidos, mientras que el atributo [<strong>allocate</strong>] supone que el tipo presentado es el mismo que el tipo transmitido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[switch_type] debe especificarse en este modo de importación<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] tipo sin definir; se supone un identificador genérico</dt> <dd> El tipo de identificador especificado en ACF no está definido en el archivo IDL. El compilador MIDL supone que el tipo de identificador se resuelve en el tipo de identificador primitivo <a href="handle-t.md"><strong>handle_t</strong></a>. Agregue el atributo [<a href="handle.md"><strong>Handle</strong></a>] a la definición de tipo si desea que el identificador se comporte como un identificador genérico o definido por el usuario.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>el elemento de matriz no debe derivar de error_status_t</dt> <dd> En esta versión de Microsoft RPC, el tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> solo puede aparecer como un parámetro o tipo de valor devuelto. No puede aparecer en matrices.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[allocate] no válido en un tipo que deriva de un identificador primitivo/genérico/de contexto</dt> <dd> Por diseño, el atributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] no se puede aplicar para controlar tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>el tipo transmitido o presentado no debe derivar de error_status_t</dt> <dd> En esta versión de Microsoft RPC, el tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> no se puede usar con el atributo [<a href="transmit-as.md"><strong>transmit_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>discriminante de una Unión no debe derivar de un campo con [ignore] aplicado</dt> <dd> Una Unión utilizada en una llamada a procedimiento remoto debe estar asociada a otro elemento de datos, denominado discriminante, que selecciona el brazo de la Unión. Discriminante se debe transmitir. El atributo [<a href="ignore.md"><strong>Ignore</strong></a>] no se puede aplicar al discriminante de Unión.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[nocode] se ha omitido para el lado del servidor porque &quot; &quot; no se ha especificado/Server ninguno</dt> <dd> Algunos compiladores de DCE IDL generan un error cuando se aplica el atributo [<a href="nocode.md"><strong>nocode</strong></a>] a un procedimiento en una interfaz para la que se generan archivos de código auxiliar de servidor. Dado que el servidor debe admitir todas las operaciones, [<strong>nocode</strong>] no debe aplicarse a un procedimiento en este modo, o bien debe usar <a href="-server.md"><strong>el modificador</strong></a> del COMpilador de MIDL para especificar explícitamente que no se generarán rutinas de servidor.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>no se especificó ningún procedimiento remoto en la interfaz que no sea [local]; no se generará ningún código auxiliar de cliente/servidor</dt> <dd> La interfaz proporcionada no tiene ningún procedimiento remoto, por lo que solo se generarán archivos de encabezado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>se especificaron demasiados casos predeterminados para la Unión encapsulada</dt> <dd> Una Unión encapsulada solo puede tener un valor predeterminado: ARM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>se han especificado demasiadas interfaces predeterminadas para la coclase</dt> <dd> Una <a href="coclass.md"><strong>coclase</strong></a> puede tener, como máximo, dos miembros [<a href="default.md"><strong>predeterminados</strong></a>], uno para representar la interfaz de salida (origen) o la dispinterface y otro para representar la interfaz entrante (receptor) o dispinterface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>los elementos con [defaultvtable] también deben tener [Source]</dt> <dd> La interfaz <a href="defaultvtable.md"><strong>defaultvtable</strong></a> crea una segunda interfaz de origen para un objeto, una que permite que los receptores reciban eventos a través de la tabla V.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>la especificación de Unión sin campos no es válida</dt> <dd> Las uniones deben tener al menos un campo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>valor fuera del intervalo</dt> <dd> El valor de caso proporcionado está fuera del intervalo del tipo de modificador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] debe aplicarse en un tipo de puntero</dt> <dd> Los identificadores de contexto siempre deben ser tipos de puntero. DCE especifica que todos los identificadores de contexto deben tener tipo <strong>void *</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>el tipo de valor devuelto no debe derivar de handle_t</dt> <dd>no se puede devolver <a href="handle-t.md"><strong>handle_t</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[Handle] no debe aplicarse a un tipo que deriva de un identificador de contexto</dt> <dd> Un tipo no puede ser tanto un identificador de contexto como un identificador genérico.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>el campo que se deriva de un &quot; int &quot; debe tener un especificador de tamaño &quot; pequeño &quot; , &quot; corto &quot; o &quot; largo &quot; con el valor &quot; int&quot;</dt> <dd> El tipo <a href="int.md"><strong>int</strong></a> no es transmisible en sistemas de 16 bits, ya que el tamaño de <strong>int</strong> puede ser diferente en los equipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>el campo no debe derivar de un void o void *</dt> <dd> <strong>void</strong> y <strong>void *</strong> no se pueden usar como tipos de parámetro para procedimientos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>el campo no debe derivar de una estructura que contenga campos de bits</dt> <dd> Las estructuras que contienen campos de bits no se pueden usar como parámetros o tipos de valor devuelto para procedimientos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>el campo no debe derivar de una Unión que no sea de rpcable</dt> <dd> Una Unión debe especificarse como una Unión no encapsulada o una Unión encapsulada para su transmisión. Las uniones de C normales carecen del discriminante necesario para transmitir la Unión a través de la red.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>el campo no debe derivar de un puntero a una función</dt> <dd> Los punteros a funciones no se pueden transmitir a procedimientos remotos. Los punteros a funciones apuntan al código de función y no se puede transmitir código de función a través de la red mediante RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>no se puede usar [fault_status] en un parámetro y un tipo de valor devuelto</dt> <dd> El atributo [<a href="fault-status.md"><strong>fault_status</strong></a>] solo se puede usar una vez por procedimiento. El atributo [<a href="comm-status.md"><strong>comm_status</strong></a>] se puede usar de forma independiente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>el tipo de valor devuelto es demasiado complicado para los modos/OI, mediante/os</dt> <dd> Los tipos de valor devueltos grandes que se pasan por valor solo se pueden controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>el tipo de identificador genérico es demasiado grande para los modos/OI, mediante/os</dt> <dd> Los tipos de identificador genérico de gran tamaño que se pasan por valor solo los puede controlar el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[allocate (all_nodes)] en un parámetro [in, out] puede huérfanor la memoria original</dt> <dd> El uso de [<a href="allocate.md"><strong>alloca</strong></a>(all_nodes)] en un parámetro [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] debe reasignar la memoria contigua para la dirección [<strong>out</strong>], con lo que se huérfana el parámetro [<strong>in</strong>]. No se recomienda este uso.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>no se puede tener un puntero [Ref] como ARM de Unión</dt> <dd> Los punteros de referencia siempre deben apuntar a una memoria válida, pero una Unión [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] con un puntero de referencia puede devolver un puntero de referencia cuando la dirección [<strong>in</strong>] utiliza otro tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>no se admiten los identificadores de contexto para los modos/OI, utilizando/os</dt> <dd> MIDL no admite identificadores de contexto en los modos de optimización totalmente interpretados. Cambiar a la optimización en modo mixto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>el uso del parámetro extra [comm_status] o [fault_status] no es compatible con los modos/OI, mediante/os</dt> <dd> Los atributos [<a href="comm-status.md"><strong>comm_status</strong></a>] y [<a href="fault-status.md"><strong>fault_status</strong></a>] solo se pueden controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>no se admite el uso de un tipo desconocido para [represent_as] o [user_marshal] para los modos/OI, mediante/os</dt> <dd> El uso del atributo [<a href="represent-as.md"><strong>represent_as</strong></a>] con un tipo local que no está definido en el archivo IDL o un archivo IDL importado solo se puede controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>los tipos de matriz con [transmit_as] o [represent_as] no se admiten en el tipo de valor devuelto para los modos/OI, mediante/os</dt> <dd> Devolver una matriz con [<a href="transmit-as.md"><strong>transmit_as</strong></a>] o [<a href="represent-as.md"><strong>represent_as</strong></a>] aplicada solo se puede controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>los tipos de matriz con [transmit_as] o [represent_as] no se admiten como paso a valor para los modos/OI, mediante/os</dt> <dd> Esta acción no se admite para la optimización totalmente interpretada. Cambiar a la optimización en modo mixto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[callback] requiere/ms_ext</dt> <dd> El atributo [<a href="callback.md"><strong>callback</strong></a>] es una extensión de Microsoft y requiere que esté habilitado el modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a> . No compilar con <a href="-osf.md"><strong>/OSF</strong></a>, que invalida <strong>/ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>dependencia de interfaz circular</dt> <dd> Esta interfaz se usa a sí misma (directa o indirectamente) como una interfaz base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>solo se puede usar IUnknown como interfaz raíz</dt> <dd> Actualmente, todas las interfaces deben tener <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> como la interfaz raíz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] solo se puede aplicar a punteros a interfaces</dt> <dd> El atributo [<a href="iid-is.md"><strong>iid_is</strong></a>] solo se puede aplicar a punteros de interfaz, aunque se pueden especificar como punteros a <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>las interfaces solo se pueden usar en construcciones de puntero a interfaz</dt> <dd> Los nombres de interfaz no se pueden usar excepto como interfaces base o punteros de interfaz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>los punteros de interfaz deben tener un UUID/IID</dt> <dd> El tipo base de la expresión [<a href="iid-is.md"><strong>iid_is</strong></a>] debe ser un tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>las definiciones y declaraciones fuera del cuerpo de la interfaz requieren/ms_ext</dt> <dd> La colocación de declaraciones y definiciones fuera de cualquier cuerpo de la interfaz es una extensión de Microsoft y requiere el uso del modificador <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>varias interfaces en un archivo requieren/ms_ext</dt> <dd> El uso de varias interfaces en un solo archivo IDL es una extensión de Microsoft y no está disponible al compilar en modo <a href="-osf.md"><strong>/OSF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>solo se permite una de [implicit_handle], [auto_handle] o [explicit_handle]</dt> <dd> Cada interfaz solo puede tener uno de estos tres atributos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] hace referencia a un tipo que no es un identificador</dt> <dd> Los identificadores implícitos deben ser de uno de los tipos de identificador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>los procedimientos [Object] solo se pueden usar con &quot; /env Win32&quot;</dt> <dd> Las interfaces con el atributo [<a href="object.md"><strong>Object</strong></a>] no se pueden usar con entornos de 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[callback] con-env dos/Win16 no se admite para/OI, mediante/os</dt> <dd> Las devoluciones de llamada en entornos de 16 bits solo se pueden controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>no se admite float/double como parámetro de nivel superior para el modo/OI, utilizando/os</dt> <dd> Los tipos float y Double solo se pueden administrar como parámetros mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> . Los tipos float y Double en estructuras, matrices o uniones todavía se pueden controlar con<strong>/os</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>los punteros a identificadores de contexto no se pueden usar como valores devueltos</dt> <dd> Los identificadores de contexto deben usarse como valores devueltos directos, no como valores devueltos indirectos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>los procedimientos de una interfaz de objeto deben devolver un valor HRESULT</dt> <dd> Todos los procedimientos de una interfaz de objeto que no tienen el atributo-[<a href="local.md"><strong>local</strong></a>] deben devolver un <strong>valor HRESULT</strong> / <strong>SCODE</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>UUID duplicado</dt> <dd> Igual que UUID debe ser único.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>las interfaces [Object] deben derivarse de otra interfaz [Object] como IUnknown</dt> <dd> La herencia de interfaz solo se permite cuando se usan interfaces de objeto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>la interfaz (asincrónica) debe derivarse de otra interfaz (asincrónica)</dt> <dd> Las interfaces de objeto, tanto sincrónicas como asincrónicas, deben derivar de <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> o de cualquier otra interfaz OLE base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS] la expresión debe ser un puntero a una estructura IID</dt> <dd> El tipo base de la expresión [<a href="iid-is.md"><strong>iid_is</strong></a>] debe ser un tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] tipo debe ser un procedimiento [local]</dt> <dd> El destino de un tipo [<a href="call-as.md"><strong>call_as</strong></a>], si está definido, debe tener aplicado [ <a href="local.md"><strong>local</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>no se debe usar [call_as] sin definir en una interfaz de objeto</dt> <dd> Debe definir el destino de un tipo [<a href="call-as.md"><strong>call_as</strong></a>]. Asegúrese de que ha proporcionado <strong>call_as</strong> rutinas para las aplicaciones llamadas y llamadas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] no se puede usar con [encode] o [descode]</dt> <dd> Los atributos [ <a href="encode.md"><strong>encode</strong></a>] y [ <a href="decode.md"><strong>Decode</strong></a>] solo se pueden usar con identificadores explícitos o identificadores implícitos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>no se permiten procedimientos normales en una interfaz con [encode] o [descode]</dt> <dd> Las interfaces que contienen procedimientos [<a href="encode.md"><strong>encode</strong></a>] o [<a href="decode.md"><strong>Decode</strong></a>] también no pueden tener procedimientos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>no se permite la varianza o el cumplimiento de nivel superior con [encode] o [descode]</dt> <dd> Los tipos que tienen compatibilidad o varianza de nivel superior no pueden usar la serialización de tipos, ya que no hay ninguna manera de proporcionar el tamaño o la prolongación. Sin embargo, las estructuras que los contienen se pueden usar para la serialización de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>[out] los parámetros no pueden tener &quot; const&quot;</dt> <dd> Dado que se modifica un parámetro [<a href="out-idl.md"><strong>out</strong></a>], no debe declararse como constante SA.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>los valores devueltos no pueden tener &quot; const&quot;</dt> <dd> Dado que un valor de función se establece cuando la función devuelve, este valor no debe declararse como una constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>uso no válido &quot; del &quot; atributo retval</dt> <dd> Asegúrese de que no ha usado el atributo [<a href="optional.md"><strong>Optional</strong></a>] y que el parámetro [<a href="retval.md"><strong>retval</strong></a>] es el último parámetro de la lista.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>múltiples convenciones de llamada no válidas</dt> <dd> Solo se puede aplicar una Convención de llamada a un único procedimiento.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>atributo no válido en el procedimiento [Object]</dt> <dd> El atributo anterior solo se aplica a los procedimientos de las interfaces que no tienen el atributo [<a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] los punteros de interfaz deben usar el direccionamiento indirecto doble</dt> <dd> Puesto que el valor modificado es el puntero a la interfaz, debe haber otro nivel de direccionamiento indirecto por encima del puntero para permitir que se devuelva.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>procedimiento usado dos veces como autor de la llamada en [call_as]</dt> <dd> Un procedimiento [<a href="local.md"><strong>local</strong></a>] determinado solo se puede usar una vez como destino de un [<a href="call-as.md"><strong>call_as</strong></a>], con el fin de evitar conflictos de nombres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as] el destino debe tener [local] en una interfaz de objeto</dt> <dd> El destino de [<a href="call-as.md"><strong>call_as</strong></a>] debe ser un procedimiento definido [<a href="local.md"><strong>local</strong></a>] en la interfaz actual.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[code] y [nocode] no se pueden usar juntos</dt> <dd> Estos dos atributos son contradictorios y no se pueden usar juntos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>los procedimientos con atributos [maybe] o [Message] no pueden tener parámetros [out] o los valores devueltos deben ser de tipo HRESULT o error_status_t</dt> <dd> Dado que los procedimientos [<a href="maybe.md"><strong>maybe</strong></a>] nunca devuelven, no hay ninguna manera de obtener los valores devueltos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>se debe usar el puntero a la función</dt> <dd> Aunque las definiciones de tipo de función se permiten en el modo <a href="-c-ext.md"><strong>/c_ext</strong></a> , solo se pueden usar como punteros a funciones. Nunca se pueden transmitir como un parámetro o un valor devuelto de un procedimiento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>es posible que las funciones no se pasen en una operación RPC</dt> <dd> Las funciones y los punteros a función no se pueden pasar como parámetros o valores devueltos de procedimientos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>no se admite Hyper/Double como valor devuelto para los modos/OI, mediante/os</dt> <dd> Los valores devueltos de tipo Hyper y Double solo se pueden controlar mediante el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> . El código auxiliar de esta rutina se generará mediante la optimización <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma Pack (pop) sin coincidencia de #pragma Pack (Inserte)</dt> <dd> #pragma Pack (Inserte) y #pragma Pack (pop) deben aparecer en pares coincidentes. Se especificaron al menos un número de #pragma de paquetes (de extracción).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>los campos de estructura de cadena deben ser bytes/char/wchar_t</dt> <dd> El tipo [<a href="string.md"><strong>String</strong></a>] solo se puede aplicar a una estructura cuyos campos sean de tipo byte, o una definición de tipo equivalente a byte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[Notify] no se admite para los modos/OI, mediante/os</dt> <dd> El atributo [<a href="notify.md"><strong>Notify</strong></a>] solo puede ser procesado por el código auxiliar de optimización <a href="-os.md"><strong>/os</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> no se admite el parámetro Handle o el tipo de valor devuelto en un procedimiento de una interfaz [Object]</dt> <dd> Los identificadores no se pueden usar con interfaces [ <a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C solo permite que la matriz del extremo izquierdo esté sin especificar.</dt> <dd> En una matriz compatible, ANSI C solo permite que el límite de la matriz (más importante) de la izquierda esté sin especificar. Si hay varias dimensiones compatibles, MIDL intentará colocar un &quot; 1 &quot; en las otras dimensiones compatibles. Si las otras dimensiones se definen en una definición de tipo diferente, no es posible. Intente colocar todas las dimensiones de la matriz en la declaración de la matriz para evitar esto. En cualquier caso, tenga cuidado con los cálculos de indización de matriz realizados por el compilador; es posible que necesite realizar sus propios cálculos con los tamaños reales.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>los parámetros de Unión por valor no se admiten para los modos/OI, mediante/os</dt> <dd> Esta acción no se admite para la optimización totalmente interpretada. Cambiar a la optimización en modo mixto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>el atributo [Version] se omite en una interfaz [Object]</dt> <dd> El atributo [<a href="object.md"><strong>Object</strong></a>] identifica una interfaz com. Una lista de atributos de interfaz para una interfaz COM no puede incluir el atributo [ <a href="version.md"><strong>version</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>el atributo [size_is] o [max_is] no es válido en una matriz fija</dt> <dd> Las matrices de tamaño fijo no pueden utilizar los atributos <a href="size-is.md"><strong>size_is</strong></a> o <a href="max-is.md"><strong>max_is</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[encode] o [descode] no son válidos en una interfaz [Object]</dt> <dd> El atributo [<a href="object.md"><strong>Object</strong></a>] identifica una interfaz com. Los atributos [<a href="encode.md"><strong>encode</strong></a>] y [ <a href="decode.md"><strong>Decode</strong></a>] permiten la serialización. Es decir, puede proporcionar y controlar los búferes para calcular las referencias de los datos y anular las referencias; sin embargo, no puede realizar la serialización en las interfaces COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[encode] o [descode] en un tipo requiere/ms_ext</dt> <dd> La serialización no forma parte de la especificación de DCE-IDL. Es una extensión de Microsoft que requiere el uso del modificador de línea de comandos <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>no se admite int en/env Win16 o/env dos.</dt> <dd> Las plataformas de Microsoft de 16 bits no admiten el uso del tipo <a href="int.md"><strong>int</strong></a> en un archivo IDL. Califique el tipo <strong>int</strong> con <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>o <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[Bstring] solo se puede aplicar a un puntero a &quot; Char &quot; o &quot; whchar_t&quot;</dt> <dd> Este error está obsoleto. Solo se proporciona para la compatibilidad con versiones anteriores.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>atributo no válido en un procedimiento en una interfaz [Object]</dt> <dd> No se permite el atributo especificado en el procedimiento de una interfaz COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>atributo no válido en una interfaz [objeto]</dt> <dd> No se permite el atributo especificado en una interfaz COM.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>demasiados parámetros o una pila demasiado grande para los modos/OI, utilizando/os</dt> <dd> Esta advertencia está obsoleta. Solo se proporciona para la compatibilidad con versiones anteriores. Indica que la llamada al procedimiento remoto hace que la pila crezca más de 64 K.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>no hay atributos en la definición de tipo de archivo ACF, por lo que no hay ningún efecto</dt> <dd> El archivo IDL debe contener todas las instrucciones TypeDef que no tienen atributos. No se deben producir en archivos ACF. Si lo hacen, el compilador MIDL los interpreta como redundantes y los omite.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>las convenciones de llamada distintas de __stdcall o __cdecl no se admiten para los modos/OI, mediante/os</dt> <dd> Las convenciones de llamada, como <strong>__pascal</strong> o <strong>__fastcall</strong> cambiar el formato de la pila. Los modos <a href="-oi.md"><strong>/OI</strong></a> solo admiten las convenciones de llamada <strong>__stdcall</strong> y <strong>__cdecl</strong> . Si debe utilizar otras convenciones de llamada, use el modo <a href="-os.md"><strong>/os</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>Hay demasiados métodos de delegación en la interfaz, se requiere Windows 2000 o superior.</dt> <dd> Una interfaz puede heredar de otra. Cuando lo hace, los métodos de la interfaz base se consideran delegados. Ninguna interfaz derivada puede contener más de 256 métodos delegados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>no se admiten los identificadores automáticos con/env Mac o/env PowerMac</dt> <dd> Al compilar el archivo IDL para un PowerMac, no puede usar los identificadores de enlace automáticos. Debe especificar identificadores explícitos o implícitos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>las instrucciones fuera del bloque de biblioteca no son válidas en el modo de compatibilidad MkTypLib</dt> <dd> Es posible que tenga que especificar el modificador de línea de comandos <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> al compilar el archivo IDL.<br/>
<blockquote>
[!Note]<br />
La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>sintaxis no válida a menos que se use el modo de compatibilidad MkTypLib</dt> <dd> Es posible que tenga que especificar el modificador de línea de comandos <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> al compilar el archivo IDL.<br/>
<blockquote>
[!Note]<br />
La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>definición no válida, debe usar typedef en modo de compatibilidad de MkTypLib</dt> <dd> Es posible que tenga que especificar el modificador de línea de comandos <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> al compilar el archivo IDL.<br/>
<blockquote>
[!Note]<br />
La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>atributo de puntero explícito [PTR] [Ref] omitido para punteros de interfaz</dt> <dd> Los punteros a las interfaces no pueden tener atributos IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td>Modos <a href="-oi.md"><strong>/OI</strong></a> no implementados para PowerMac, cambiando a <a href="-os.md"> <strong>/os</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>se usó un tipo de expresión no válido en el atributo</dt> <dd> El valor predeterminado del puntero debe ser una constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>tipo no válido usado en la canalización</dt> <dd> Las canalizaciones se limitan a los tipos de datos IDL básicos. Por ejemplo, no puede especificar una canalización de matrices.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>el procedimiento usa canalizaciones con/Oicf</dt> <dd> El modo seleccionado no admite canalizaciones. El compilador MIDL detectó el uso de una o más canalizaciones en la interfaz. Por lo tanto, está compilando el archivo IDL en modo <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>el procedimiento tiene un atributo que requiere el uso de/OIF, modos de cambio</dt> <dd> Debe compilar los procedimientos [<a href="async.md"><strong>Async</strong></a>] en modo <a href="-oi.md"><strong>/OIF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>requisitos de optimización en conflicto, no se puede optimizar</dt> <dd> Este error suele indicar que se han especificado los modos de compilador de MIDL <a href="-os.md"><strong>/os</strong></a> y <a href="-oi.md"><strong>/OI</strong></a> (o una variante de <strong>/OI</strong>). También puede significar que las características especificadas en los archivos IDL y ACL requieren el uso de ambos modos. Debe seleccionar un modo u otro para optimizar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>las canalizaciones no pueden ser elementos de matriz o miembros de estructuras o uniones</dt> <dd> Los tipos de datos de canalización solo pueden ser parámetros de nivel superior.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>uso de canalización no válido</dt> <dd> No se pueden usar canalizaciones con los atributos [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] o [<a href="user-marshal.md"><strong>user_marshal</strong></a>]. Además, las canalizaciones no se pueden usar como tipos de valor devuelto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la característica requiere la opción de optimización interpretada avanzada; uso de-Oicf</dt> <dd> Este error indica que los modificadores de la línea de comandos del compilador MIDL como <a href="-robust.md"><strong>/Robust</strong></a> requieren el uso del modo <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la característica requiere la opción de optimización interpretada avanzada; uso de-Oicf</dt> <dd> Esta advertencia indica que los modificadores de la línea de comandos del compilador MIDL como <a href="-robust.md"><strong>/Robust</strong></a> requieren el uso del modo <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>la opción de optimización está obsoleta, use-OIC</dt> <dd> El modo de optimización <a href="-oi.md"><strong>/Oi1</strong></a> se especificó en la línea de comandos de MIDL. Este modo ya no se admite y se debe usar <strong>/Oicf</strong> en su lugar.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>la opción de optimización está obsoleta, use-Oicf</dt> <dd> El modo de optimización <a href="-oi.md"><strong>/Oi2</strong></a> se especificó en la línea de comandos de MIDL. Este modo ya no se admite y se debe usar <strong>/Oicf</strong> en su lugar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>la opción de optimización está obsoleta, use-IC</dt> <dd> El modo de optimización I1 se especificó en un atributo ACF [Optimize]. Este modo ya no se admite y en su lugar se debe usar ICF.<br/> Archivo ACF de ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>la opción de optimización se está quedando obsoleta, use-ICF</dt> <dd> El modo de optimización de i2 se especificó en un atributo ACF [Optimize]. Este modo ya no se admite y en su lugar se debe usar ICF.<br/> Archivo ACF de ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>los modificadores-Old y-New están obsoletos, use-oldtlb y-newtlb</dt> <dd> Este mensaje está obsoleto y ya no lo omite MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>valor de argumento no válido</dt> <dd> Las variantes permitidas del modificador de la línea de comandos/O incluyen <a href="-os.md"><strong>/os</strong></a>, <a href="-oi.md"><strong>/OI</strong></a>, <strong>/OIC</strong>, <strong>/Oicf</strong>y <strong>/OIF</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>tipo de expresión no válido en Constant</dt> <dd> La expresión no se evalúa como una constante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>tipo de expresión no válida en la enumeración</dt> <dd> Un valor enumerado en una definición de <a href="enum.md"><strong>enumeración</strong></a> no se evalúa como un tipo entero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>Declaración de avance insatisfecho</dt> <dd> El compilador MIDL no pudo resolver la definición de una declaración adelantada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>los modificadores son contradictorios</dt> <dd> No se pueden usar los modificadores de línea de comandos <a href="-osf.md"><strong>/OSF</strong></a> y <a href="-ms-ext.md"><strong>/ms_ext</strong></a> al compilar un archivo IDL. Debe elegir uno u otro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL no puede generar información de HOOKOLE para la Unión no habilitada para RPC</dt> <dd> Este error está obsoleto. Se proporciona estrictamente para la compatibilidad con versiones anteriores.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>no se encontró ninguna expresión Case para Union</dt> <dd> Cada campo de una Unión debe tener una instrucción case con una expresión constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] y [wire_marshal] no se admiten con las marcas-OI y-OIC, use-os o-Oicf</dt> <dd> Los atributos [<a href="user-marshal.md"><strong>user_marshal</strong></a>] y [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] requieren que las características de optimización específicas estén disponibles solo en <a href="-oi.md"><strong>/Oicf</strong></a> (proxy sin código con cadenas de formato rápido) o <a href="-os.md"><strong>/os</strong></a> (serialización de modo mixto).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>las canalizaciones no se pueden usar con la serialización de datos, es decir, [encode] o [descode]</dt> <dd> No se pueden pasar canalizaciones como parámetros a procedimientos que tengan los atributos [<a href="encode.md"><strong>encode</strong></a>] o [<a href="decode.md"><strong>Decode</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>todos los punteros de interfaz de canalización deben usar direccionamiento indirecto único</dt> <dd> No se puede usar un puntero a un puntero a una interfaz de canalización de esta manera.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is ()] no se puede usar con un puntero de interfaz de canalización</dt> <dd> Este mensaje está obsoleto. El compilador ya no usa este mensaje.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>conmutador no válido o inaplicable: LCID</dt> <dd> El identificador local (LCID) especificado no es válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>el LCID especificado es diferente de la especificación anterior</dt> <dd> Los valores especificados en/LCID y [<a href="lcid.md"><strong>LCID</strong></a>] son diferentes. El compilador MIDL usará el último definido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>no se permite importlib fuera de un bloque de biblioteca</dt> <dd> Todas las instrucciones [<a href="importlib.md"><strong>importlib</strong></a>] deben aparecer en un bloque [<a href="library.md"><strong>Library</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>valor de punto flotante no válido</dt> <dd> Este error no lo debe emitir MIDL. Si ve este error, notifique un error a Microsoft que proporcione todos los archivos necesarios para reproducir el error, incluidos los archivos IDL, los archivos ACF, los encabezados, etc.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>miembro no válido</dt> <dd> Los procedimientos no pueden ser miembros de una biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>posible miembro no válido</dt> <dd> Para ser un miembro válido de una biblioteca, el elemento Library debe ser un módulo, una dispinterface, una coclase, una instrucción if, una estructura, una Unión, una enumeración o una declaración adelantada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>falta de coincidencia en los tipos de canalización e interfaz</dt> <dd> Este mensaje está obsoleto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>una cadena, una matriz variable, una matriz compatible y parámetros de puntero completo pueden ser incompatibles con los parámetros de canalización durante el tiempo de ejecución</dt> <dd> Un método que combina una o más cadenas [in], matrices variables, matrices compatibles y parámetros de puntero completos y cualquier parámetro de canalización [in] producen la generación de un código auxiliar que solo se ejecuta en secuencias de protocolo <strong>ncacn_ *</strong> y <a href="ncalrpc.md"><strong>Ncalrpc</strong></a> en equipos Windows. El uso del código auxiliar para realizar llamadas en <strong>ncadg_ *</strong> secuencias de protocolo o aceptar llamadas de otros proveedores de RPC DCE de OSF puede generar errores en el servidor durante el tiempo de ejecución. Este error se produce a partir de Windows Server 2003.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>el parámetro debe estar en</dt> <dd> Los identificadores asincrónicos deben ser parámetros [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>el tipo de parámetro de un objeto [Async] debe ser un puntero doble a una interfaz</dt> <dd> El parámetro debe ser de tipo <strong>IAsyncManager</strong> * *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>tipo de identificador Async incorrecto</dt> <dd> El tipo de identificador debe ser <strong>IAsyncManager</strong> o un tipo derivado de <strong>IAsyncManager</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>el &quot; &quot; conmutador interno habilita las características no admitidas, use con precaución</dt> <dd> Evite el uso de este modificador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>los procedimientos asincrónicos no pueden usar el controlador automático</dt> <dd> Los procedimientos con el atributo [<a href="async.md"><strong>Async</strong></a>] requieren identificadores explícitos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t debe tener [comm_status] y [fault_status]</dt> <dd> Se ha especificado un procedimiento con los atributos IDL [maybe] o [Message], pero el tipo de valor devuelto solo tiene los atributos ACF [comm_status] o [fault_status]. Ambos atributos ACF son obligatorios.<br/> Archivo ACF de ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Esta construcción solo se permite dentro de un bloque de biblioteca</dt> <dd> Un módulo solo puede aparecer dentro de un bloque de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>nueva definición de tipo no válida</dt> <dd> Un nuevo tipo se definió de forma recursiva en un tipo no existente.<br/> Ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>los procedimientos con un atributo [vararg] deben tener un parámetro SAFEARRAY (VARIANT); el orden de los parámetros es [vararg], [LCID], [retval]</dt> <dd> La mayoría de los parámetros de los procedimientos con el atributo [<a href="vararg.md"><strong>vararg</strong></a>] deben aparecer antes del parámetro <strong>SAFEARRAY (variante)</strong> . El parámetro <strong>SAFEARRAY (Variant)</strong> debe estar presente. Si la lista de parámetros contiene un parámetro con el atributo [ <a href="lcid.md"><strong>LCID</strong></a>], debe seguir el parámetro <strong>SAFEARRAY (variante)</strong> . Si la lista de parámetros contiene un parámetro con el atributo [<a href="retval.md"><strong>retval</strong></a>], debe aparecer después del parámetro con el atributo [<strong>LCID</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>demasiados métodos en la interfaz, requiere Windows 2000 o superior</dt> <dd> El compilador MIDL no permite más de 1024 métodos en una interfaz al compilar en modo <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>el modificador se está cerrando.</dt> <dd> Los siguientes modificadores son obsoletos:/<strong>hookole</strong>,/<strong>env</strong>, y/<strong>env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>no se puede derivar de IAdviseSink, IAdviseSink2 o IAdviseSinkEx</dt> <dd> Estas interfaces no se pueden extender.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>no se puede asignar un valor predeterminado</dt> <dd> Se permite asignar un valor predeterminado a un parámetro en Visual Basic, pero no en C++. Si usa C++, se omite el valor predeterminado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>no se admite la generación de biblioteca de tipos para DOS/Win16/MAC</dt> <dd> MIDL no es compatible con las bibliotecas de tipos de 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>Error al generar la biblioteca de tipos; se omite</dt> <dd> Se produjo un error no irrecuperable al generar la biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>se ha superado el tamaño de pila para/OI, mediante/os</dt> <dd> El modo de optimización-OI está limitado a 128 bytes de espacio de pila para los parámetros. El compilador ha cambiado automáticamente al modo de optimización del sistema operativo para evitar esta limitación.<br/> Para evitar esta advertencia, use los modos de optimización-Oicf o-os. El modo de optimización se puede cambiar en la línea de comandos especificando-Oicf o-os en lugar de-OI o agregando un atributo [optimize9 &quot; ICF &quot; )] u optimizar [( &quot; s &quot; )] a la función en el archivo ACF.<br/> Normalmente, esta advertencia se produce al pasar estructuras grandes como parámetros por valor. Se puede reducir el tamaño de pila necesario pasando un puntero a la estructura en su lugar.<br/> Ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>el uso de/ROBUST requiere/Oicf, cambiar los modos</dt> <dd> Debe compilar en modo <a href="-oi.md"><strong>/Oicf</strong></a> al especificar el modificador <a href="-robust.md"><strong>/Robust</strong></a> en la línea de comandos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>rango incorrecto especificado</dt> <dd> El valor más alto especificado en un atributo [<a href="range.md"><strong>Range</strong></a>] es menor que el valor más bajo.<br/> Ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> combinación no válida de los parámetros [in] only y [out] para la interfaz [async_uuid]</dt> <dd> Solo se permiten combinaciones simples de atributos con parámetros [<a href="in.md"><strong>in</strong></a>] o [<a href="out-idl.md"><strong>out</strong></a>] para este tipo de interfaz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>No se admiten las plataformas DOS, Win16 y MAC con/Robust</dt> <dd> MIDL admite el modificador <a href="-robust.md"><strong>/Robust</strong></a> en Microsoft Windows 2000 o posterior.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>la compatibilidad con los proxies sin código auxiliar de estilo NT 3,51 para las interfaces de objeto quedará en fase de salida; usar/OIF.</dt> <dd> Este modo está obsoleto. Use <a href="-oi.md"><strong>/OIF</strong></a> o <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[encode] o [descode] con/Robust requiere/Oicf</dt> <dd> No se puede realizar la serialización cuando se especifica el modificador <a href="-robust.md"><strong>/Robust</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>atributos en conflicto especificados</dt> <dd> Se especificaron [<a href="context-handle-serialize.md"><strong>context_handle_serialize</strong></a>] y [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[Serialize], [noserialization] se puede aplicar a context_handles</dt> <dd> Los atributos ACF [context_handle_serialize] o [context_handle_noserialize] solo se pueden aplicar a los tipos que son identificadores de contexto.<br/> Archivo IDL de ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
Archivo ACF de ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>El compilador alcanzó un límite para una representación de cadena de formato. Consulte la documentación para obtener consejos.</dt> <dd> El compilador MIDL tiene un límite de 64 KB para las cadenas de formato. Este error suele producirse cuando los archivos IDL incluyen otros archivos IDL. El archivo IDL compuesto generado por todas las instrucciones include supera los límites de las tablas de representación de tipos del intérprete del motor de serialización. Pruebe a usar la Directiva de importación en lugar de la Directiva include en los archivos IDL. Para obtener más información, vea <a href="importing-system-header-files.md">importar archivos de encabezado del sistema</a>, <a href="include.md"><strong>incluir</strong></a>e <a href="import.md"><strong>importar</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>el formato de conexión puede ser incorrecto, puede que tenga que usar-ms_conf_struct, consulte la documentación para obtener consejos</dt> <dd> El compilador MIDL no pudo generar un formato transmisible para los datos. Una forma habitual de obtener este error es definir una <strong>ms_conf_struct</strong> dentro de una estructura compleja.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>un tamaño de pila o un desplazamiento mayor que el límite de 64 K. Consulte la documentación para obtener consejos.</dt> <dd> La llamada da como resultado una pila de más de 64 KB. Intente pasar los datos en bloques más pequeños.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>un modo de intérprete forzado para la plataforma de 64 bits </dt> <dd> las plataformas de 64 bits requieren el modo de compilación/Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>El tamaño del elemento de la matriz es mayor que el límite de 64 KB.</dt> <dd> Todos los elementos de la matriz deben tener menos de 64 KB de tamaño.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>solo puede haber un parámetro [ICID] en un método, y debe ser el último o el segundo hasta el último si el último parámetro tiene [retval]</dt> <dd> Un parámetro con el atributo [<a href="lcid.md"><strong>LCID</strong></a>] debe aparecer en último lugar. La única excepción es cuando también hay un parámetro con el atributo [<a href="retval.md"><strong>retval</strong></a>]. Cuando se producen ambos, el segundo al último parámetro de la lista de parámetros debe tener el atributo [ <strong>LCID</strong>]. El último parámetro debe tener el atributo [<strong>retval</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>Sintaxis incorrecta para midl_pragma</dt> <dd> El compilador MIDL detectó un error de sintaxis desconocido en una instrucción midl_pragma.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 no se admite en el modo/OSF</dt> <dd> Si necesita usar __int3264, compile en modo/MS-ext.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>símbolo sin resolver en la biblioteca de tipos</dt> <dd> El compilador no pudo resolver una declaración formal o un tipo al que se hace referencia en la biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>las canalizaciones asincrónicas no se pueden pasar por valor</dt> <dd> Las canalizaciones asincrónicas se deben pasar por referencia o por dirección.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>el desplazamiento de parámetro supera el límite de 64 KB para los procedimientos interpretados</dt> <dd> Normalmente, este error significa que un procedimiento tiene demasiados parámetros.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>elemento de matriz no válido</dt> <dd> Las canalizaciones no se pueden usar como elementos de matriz.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>los miembros dispinterface deben ser métodos, propiedades o interfaces.</dt> <dd> Una dispinterface no puede contener definiciones de tipo, estructuras, enumeraciones ni uniones.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local] procedimiento sin [call_as]</dt> <dd> Los procedimientos de objeto que tienen el atributo [<a href="local.md"><strong>local</strong></a>] también requieren el atributo [<a href="call-as.md"><strong>call_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>Vector multidimensional, cambiar a/Oicf</dt> <dd> El modo de optimización <a href="-os.md"><strong>/os</strong></a> no admite matrices de tamaño no fija multidimensionales. El compilador ha cambiado automáticamente el modo de optimización a/<strong>Oicf</strong> para esta función. <br/> Esta advertencia se puede suprimir globalmente cambiando el modo de compilador especificando/<strong>Oicf</strong> en la línea de comandos de MIDL o usando <strong>midl_pragma</strong> ADVERTENCIA (disable: 2393) en el archivo IDL. El modo de optimización se puede cambiar para una función individual agregando el atributo [<strong>Optimize ( &quot; ICF &quot; )</strong>] a la función en el archivo ACF.<br/> En el ejemplo siguiente se muestra esta ADVERTENCIA:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>no se admiten tipos o construcciones en un bloque de biblioteca porque falta Oleaut32.dll compatibilidad con tipos polimórficos de 64 KB</dt> <dd> La automatización OLE no admite tipos polimórficos (como _int3264, INT_PTR, etc.). Estos tipos tienen representaciones de datos incompatibles entre las plataformas 32 y 64 bits. La llamada remota producirá un error en tiempo de ejecución en las plataformas de 64 bits.<br/>
<blockquote>
[!Note]<br />
Tenga en cuenta que, a partir de la versión 2000 de Windows, los archivos TLB de 64 bits son compatibles con la automatización OLE mediante la conversión de información de TLB de 32 bits en tiempo de ejecución. Por lo tanto, MIDL solo admite la generación de TLB de 32 bits.
</blockquote>
<br/> Si se usa MIDL solo para generar un archivo de encabezado, el modificador <a href="-notlb.md"><strong>/notlb</strong></a> suprimirá la generación del archivo TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>código antiguo del intérprete que se genera para 64B</dt> <dd> Este error está obsoleto. Si ve este error, notifique un error a Microsoft y proporcione los archivos IDL, los archivos ACF y la línea de comandos de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>el modificador del compilador ya no se admite</dt> <dd> Ya no se admiten los modificadores o modificadores especificados.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>no se puede ejecutar el motor MIDL</dt> <dd> A partir de la versión 2000 de Windows (MIDL versión 5.03.279), el compilador MIDL se implementa utilizando dos archivos ejecutables: Midl.exe (el controlador) y Midlc.exe (el motor de compilador). Este error indica que el Midl.exe no se puede iniciar Midlc.exe. Asegúrese de que Midlc.exe se encuentre en el mismo directorio que Midl.exe y que tengan la misma versión.<br/> La causa del error puede ser la copia de Midl.exe pero no Midlx.exe de la última distribución. Ejecute <strong>MIDL</strong> y/o <strong>midlc</strong> en la línea de comandos sin ningún parámetro para ver el número de versión del archivo ejecutable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>comandos no válidos del controlador</dt> <dd> A partir de la versión 2000 de Windows (MIDL versión 5.03.279), el compilador MIDL se implementa utilizando dos archivos ejecutables: Midl.exe (el controlador) y Midlc.exe (el motor de compilador). Este error indica que el archivo temporal utilizado para pasar comandos desde Midl.exe a Midlc.exe falta o está dañado. Asegúrese de que Midlc.exe se encuentre en el mismo directorio que Midl.exe y que tengan la misma versión.<br/> El error puede deberse a un intento de ejecutar Midlc.exe directamente o al copiar Midl.exe pero no Midlc.exe de la última distribución. Ejecute <strong>MIDL</strong> y/o <strong>midlc</strong> en la línea de comandos sin ningún parámetro para ver el número de versión del archivo ejecutable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>para la automatización OLE, los parámetros opcionales deben ser variantes o variantes *</dt> <dd> La automatización OLE requiere que todos los parámetros [Optional] sean de tipo <strong>variante</strong> o <strong>variante *</strong>.<br/> En la automatización OLE, el uso de parámetros que no sean variantes puede provocar un error en la llamada en tiempo de ejecución o pasar datos no definidos para los parámetros [<a href="optional.md"><strong>Optional</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[DefaultValue] se aplica a una no variante y a [opcional]. Quite [opcional]</dt> <dd> El atributo [<a href="defaultvalue.md"><strong>DefaultValue</strong></a>] implica [<a href="optional.md"><strong>opcional</strong></a>]. El atributo [ <strong>Optional</strong>] no es necesario.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>el atributo [Optional] no es aplicable fuera de un bloque de biblioteca</dt> <dd> La funcionalidad que implica el atributo [ <a href="optional.md"><strong>Optional</strong></a>] no es aplicable a los servidores proxy generados para una interfaz fuera de un bloque de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>El tipo de datos del parámetro [ICID] debe ser largo</dt> <dd> La automatización OLE requiere que los parámetros con el atributo [<strong>ICID</strong>] sean de tipo <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>los procedimientos con [propput], [propget] o [propref] no pueden tener más de un parámetro obligatorio después de [Optional] uno</dt> <dd> No puede haber más de un parámetro sin [<a href="optional.md"><strong>Optional</strong></a>] después del último parámetro con [<strong>Optional</strong>] al usar [<a href="propput.md"><strong>PROPPUT</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] o [ <a href="propputref.md"><strong>PROPPUTREF</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] o [fault_status] with picking requiere-Oicf</dt> <dd> El modo de optimización anterior<strong>OI</strong> no admite procedimientos o parámetros con [ <a href="comm-status.md"><strong>comm_status</strong></a>] o [ <a href="fault-status.md"><strong>fault_status</strong></a>] con picking (es decir, mediante [ <a href="encode.md"><strong>encode</strong></a>] y/o [ <a href="decode.md"><strong>Decode</strong></a>]).<br/> Esta advertencia se puede suprimir globalmente mediante la especificación de-<strong>Oicf</strong> en la línea de comandos de MIDL o para una función individual agregando el atributo [Optimize ( &quot; ICF:)] a la función en el archivo ACF.<br/> En general, se recomienda el modo de optimización-<strong>Oicf</strong> en el modo<strong>OI</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>la versión del compilador y el controlador MIDL no coinciden</dt> <dd> A partir de la versión 2000 de Windows (MIDL versión 5.03.279), el compilador MIDL se implementa utilizando dos archivos ejecutables: Midl.exe (el controlador) y Midlc.exe (el motor de compilador). Este error indica que la versión de Midl.exe no coincide con la versión de Midlc.exe.<br/> La causa del error puede ser la copia de Midl.exe pero no Midlc.exe de la última distribución. Ejecute <strong>MIDL</strong> y/o <strong>midlc</strong> en la línea de comandos sin ningún parámetro para ver el número de versión del archivo ejecutable.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>no se especificó ningún archivo intermedio: Use Midl.exe</dt> <dd> A partir de la versión 2000 de Windows (MIDL versión 5.03.279), el compilador MIDL se implementa utilizando dos archivos ejecutables: Midl.exe (el controlador) y Midlc.exe (el motor de compilador). Este error indica que Midlc.exe se ejecutó directamente en lugar de usar Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>problema de procesamiento con un parámetro en un procedimiento</dt> <dd> Este error puede aparecer al importar datos desde un TLB y cuando un procedimiento tiene un parámetro no válido. <br/> Si ve este error, notifique un error a Microsoft. Especifique los archivos IDL, los archivos ACF, el archivo TLB y la línea de comandos de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>problema de procesamiento con un campo en una estructura</dt> <dd> Este error puede aparecer al importar datos desde un TLB y cuando una estructura tiene un campo de estructura o Unión no válido.<br/> Si ve este error, notifique un error a Microsoft. Especifique los archivos IDL, los archivos ACF, el archivo TLB y la línea de comandos de MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>incoherencia interna del compilador detectada: el desplazamiento de la cadena de formato no es válido. Consulte la documentación para obtener más información.</dt> <dd> El compilador MIDL detectó un valor no válido en sus estructuras de datos internas. Esto puede deberse a estructuras recursivas o por el compilador que infringen sus propios límites de representación de datos internos. Para identificar y/o solucionar el problema, intente simplificar el archivo IDL. Para ello, puede simplificar los parámetros complejos y las estructuras de datos recursivas o hacer que el archivo IDL sea más pequeño dividiéndolo. Este mensaje puede ir acompañado de una copia impresa de diagnóstico con información adicional sobre el problema.<br/> Si ve este error, notifique un error a Microsoft. Especifique los archivos IDL, los archivos ACF, la línea de comandos de MIDL completa y el resultado de diagnóstico, si los hay.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>incoherencia interna del compilador detectada: el desplazamiento de tipo no es válido. Consulte la documentación para obtener más información.</dt> <dd> El compilador MIDL detectó un valor no válido en sus estructuras de datos internas. Esto puede deberse a que las estructuras son recursivas o a que el compilador infringe sus propios límites de representación para los datos internos. Para identificar y/o solucionar el problema, intente simplificar el archivo IDL. Para ello, puede simplificar los parámetros complejos y las estructuras de datos recursivas, o bien hacer que el archivo IDL sea más pequeño dividiéndolo. Este mensaje puede ir acompañado de una copia impresa de diagnóstico con información adicional sobre el problema.<br/> Si ve este error, notifique un error a Microsoft. Especifique los archivos IDL, los archivos ACF, la línea de comandos de MIDL completa y el resultado de diagnóstico, si los hay.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>La sintaxis SAFEARRAY (Roo) no se admite fuera del bloque de biblioteca, use LPSAFEARRAY para el proxy</dt> <dd> No se permiten SafeArray con tipo explícito fuera de un bloque de biblioteca. Use LPSAFEARRAY en su lugar.<br/> En el ejemplo siguiente se muestra este error:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>no se admiten campos de bits</dt> <dd> Los campos de bits de estilo C no son compatibles con MIDL. Esto se aplica a la generación de proxy y a la generación de TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>no se admiten tipos de valor devueltos de punto flotante o complejos con [descode] en-Oicf, mediante-OI</dt> <dd> Los procedimientos con tipos de valor devueltos de punto flotante o de estructura/Unión no se admiten en la selección del estilo-Oicf. Una solución alternativa para 32 bits es usar el modo de optimización-OI al serializar datos (mediante [encode] y/o [descode]). Sin embargo, como el intérprete de estilo anterior OI y la compatibilidad con la selección están preparadas para salirse de la versión 2000 de Windows, se recomienda encarecidamente usar punteros como solución alternativa para este problema. Tenga en cuenta también que, normalmente, el cambio de un método de interfaz para usar un puntero [out, ref] en lugar del valor devuelto que causa el problema es totalmente compatible con la conexión y se puede ocultar fácilmente desde la capa de la aplicación. <br/> Esta advertencia se puede suprimir globalmente especificando-OI en la línea de comandos de MIDL o para una función individual agregando el atributo [Optimize ( &quot; i &quot; )] a la función en el archivo ACF.<br/> En el ejemplo siguiente se muestra el problema:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Una opción para solucionar esta limitación sería pasar un parámetro [out] para que contenga el resultado en lugar de usar un valor devuelto:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Como se mencionó anteriormente, la solución que se ha descrito anteriormente es buena no solo para las nuevas interfaces, sino también como solución alternativa para los antiguos. La representación de conexión para el &quot; nuevo &quot; argumento out es igual que para el valor devuelto (aviso void como nuevo valor devuelto).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>el tipo de valor devuelto no se admite para 64 bits al usar [descode]</dt> <dd> Los procedimientos con tipos de valor devueltos de punto flotante o de estructura/Unión no se admiten en el modo de 64 bits al realizar la serialización de datos (mediante [ <a href="encode.md"><strong>encode</strong></a>] y/o [ <a href="decode.md"><strong>Decode</strong></a>]). Está relacionado con el intérprete de estilo OI anterior y el serializador de datos no se admite en la plataforma de 64 bits. Para obtener más información, consulte la descripción de MIDL2414. <br/> En el ejemplo siguiente se muestra este error:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Lo siguiente se recomienda como solución alternativa para las interfaces nuevas y antiguas. Use un parámetro [out] para almacenar el resultado en lugar de usar un valor devuelto:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Tenga en cuenta que esta solución es totalmente compatible con la conexión, ya que la representación de conexión de un puntero [Ref, out] o Double es igual que la de Double.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>el tipo transmitido no puede contener un puntero completo para [wire_marshal] o [user_marshal]</dt> <dd> Los tipos con atributos [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] o [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] no pueden contener punteros completos ([ <strong>ptr</strong>]). Use [ <a href="unique.md"><strong>Unique</strong></a>] o [ <a href="ref.md"><strong>ref</strong></a>] en su lugar.<br/> En el ejemplo siguiente se muestra este error:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>el tipo transmitido debe ser un puntero o tener un tamaño constante para [wire_marshal] y [user_marshal]</dt> <dd> Los tipos de nivel superior con los atributos [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] o [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] deben tener un tamaño bien definido en tiempo de compilación. No pueden ser o contener matrices de tamaño variable o conformes.<br/> En el ejemplo siguiente se muestra este error:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>los procedimientos con [propget] deben tener al menos un parámetro o un valor devuelto</dt> <dd> Los procedimientos con el atributo [propget] deben tener algún medio para devolver el valor de propiedad. Deben tener al menos un parámetro [<a href="-out.md"><strong>out</strong></a>] o un valor devuelto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>El atributo [ReadOnly] se aplicó en el nivel de método.</dt> <dd> El atributo [ReadOnly] solo se puede aplicar en el nivel de parámetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Las estructuras que contienen matrices compatibles se deben pasar por referencia</dt> <dd> Los parámetros de nivel superior de RPC deben tener un tamaño bien definido en el momento de la compilación. No pueden ser, ni contener una matriz de tamaño variable o compatible. Además, los usuarios no pueden codificar o descodificar un tipo sin un tamaño bien definido. Las aplicaciones tienen que pasar Structs ajustados o variables conformes según la referencia.<br/> En el ejemplo siguiente se muestra este error:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> problema interno del compilador <system error code> - el compilador no puede continuar por un motivo desconocido. Consulte la documentación para obtener una solución alternativa.</dt> <dd> El compilador no pudo continuar y se desconoce la causa del error. El número de error hexadecimal es un identificador de error del sistema. Puede que se haya producido un error en la compilación debido a un problema externo, como una condición de memoria insuficiente. En ese caso, puede encontrar más información en Winerror. h o NTSTATUS. h. <br/> Hay dos situaciones en las que normalmente se genera este error:<br/>
<ul>
<li>No se pudo recuperar el compilador de MIDL tras detectar un error en el archivo IDL. Si MIDL devolvió algún mensaje de error sobre el archivo IDL, intente corregirlos y volver a compilarlos. Si no hay ningún mensaje de error, es posible que se haya producido un error en el compilador antes de que se pudiera informar de un error. Busque un error de sintaxis en la línea para la que se notifique el error interno del compilador.</li>
<li>El compilador MIDL no pudo generar el código correcto con una opción de optimización especificada. Intente cambiar los modos de compilador, compilar en optimización de modo mixto (/<a href="-os.md"><strong>os</strong></a>) o quitar todas las optimizaciones. O bien, vuelva a compilar con la marca/NO_FORMAT_OPT para suprimir la optimización predeterminada del procedimiento y los descriptores de tipo de MIDL.</li>
</ul>
En ocasiones, este error se produce aunque el archivo IDL sea correcto y no se utilicen opciones de optimización. Si este es el caso, intente volver a escribir la sección de código cerca de donde se comunicó el error quitando las modificaciones recientes, simplificando o reorganizando los tipos de datos, cambiando los prototipos o, de lo contrario, empiece a comentar partes del archivo IDL para localizar el código del problema.<br/> Si ninguna de estas opciones funciona, o si cree que el problema puede estar relacionado con un error en Midl.exe, notifíquelo a Microsoft y proporcione todos los detalles pertinentes.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

