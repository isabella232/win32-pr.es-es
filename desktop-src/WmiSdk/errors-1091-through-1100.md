---
description: Describe los errores del proveedor SNMP de WMI de 1091 a 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Errores del 1091 al 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedd1fc12fa5f547e041201f5411a262ddb3a3958ef58e8bed3bfcf8270d7058
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244325"
---
# <a name="errors-1091-through-1100"></a>Errores del 1091 al 1100

Describe los errores del proveedor SNMP de WMI de 1091 a 1100.

[Advertencia 1091](#warning-1091)

[Error irreales 1092](#fatal-error-1092)

[Error irreales 1093](#fatal-error-1093)

[Error irreales 1094](#fatal-error-1094)

[Error irreales 1095](#fatal-error-1095)

[Error irresal 1097](#fatal-error-1097)

[Error irreales 1098](#fatal-error-1098)

[Error irresal 1099](#fatal-error-1099)

## <a name="warning-1091"></a>Advertencia 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Advertencia>: " :<línea> cláusula IMPLIED no se permite para <fileName> \# objetos de tamaño fijo"**
</dt> <dd>

Advertencia semántica de módulo específico de SNMPv2C de invocación de macro **OBJECT-TYPE.** La palabra clave IMPLIED solo puede estar presente para un objeto que tenga una sintaxis de longitud variable, como OBJECT IDENTIFIER o OCTET STRING de longitud variable, en la cláusula INDEX.

</dd> </dl>

## <a name="fatal-error-1092"></a>Error irreales 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Error>: " :<línea> cláusula IMPLIED no permitida para objetos potencialmente <fileName> \# de longitud cero"**
</dt> <dd>

**Error semántico de** módulo específico de SNMPv2C de invocación de macro OBJECT-TYPE. La cláusula IMPLIED no se puede usar en un objeto de longitud variable si ese objeto puede tener una longitud cero.

</dd> </dl>

## <a name="fatal-error-1093"></a>Error irreales 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Error>: "<línea>: solo se puede enumerar el tipo <fileName> \# "INTEGER" según el SMI V1"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv1. Una enumeración MIB SNMPv1 solo puede usar el tipo INTEGER.

</dd> </dl>

## <a name="fatal-error-1094"></a>Error irreales 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Error>: "<línea>: el tipo utilizado en la enumeración no se resuelve <fileName> en uno de los tipos \# permitidos"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. El tipo utilizado en una enumeración debe ser INTEGER o un tipo equivalente, u otra enumeración.

</dd> </dl>

## <a name="fatal-error-1095"></a>Error irreales 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Error>: "<línea>: El miembro de enumeración <fileName> no es miembro de la \# enumeración primaria"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. Si se usa otra enumeración, su conjunto de elementos debe ser un subconjunto del conjunto de elementos de la enumeración primaria.

</dd> </dl>

## <a name="fatal-error-1097"></a>Error irreales 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Error>: "<línea>: el identificador no se resuelve <fileName> \# en un valor <name> entero"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. Los valores del tipo BITS deben ser valores enteros.

</dd> </dl>

## <a name="fatal-error-1098"></a>Error irresal 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Error>: <fileName> "<línea>: Valor duplicado en la \# construcción <value> bits"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. No debe haber nombres ni valores duplicados en una construcción BITS. El <línea \#> parámetro es la posición de la periodicidad del nombre o valor.

</dd> </dl>

## <a name="fatal-error-1099"></a>Error irreales 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Error irres>: "<línea>: Nombre duplicado en la <fileName> \# construcción <identifier> bits"**
</dt> <dd>

Asignación de tipos, error semántico de módulo específico de SNMPv2C. No debe haber nombres ni valores duplicados en una construcción BITS. El <línea \#> parámetro es la posición de la periodicidad del nombre o valor.

</dd> </dl>

 

 



