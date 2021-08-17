---
description: Describe los errores del proveedor SNMP de WMI de 1061 a 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Errores de 1061 a 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0072f30c8daf584c1aaf2acf783b15d2d9498a3c1479264a1db361c3e3ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924582"
---
# <a name="errors-1061-through-1070"></a>Errores de 1061 a 1070

Describe los errores del proveedor SNMP de WMI de 1061 a 1070.

[Error irresal 1063](#fatal-error-1063)

[Error irresal 1064](#fatal-error-1064)

[Error irresal 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Error irresal 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Error>: "<línea>: el límite superior de la especificación SIZE es menor que el <fileName> \# límite inferior"**
</dt> <dd>

Error semántico del módulo en la especificación SIZE, específico de SNMPv1 ni SNMPv2C. El símbolo utilizado en una especificación SIZE debe resolverse en OCTET STRING u Opaque. El límite inferior de un intervalo o especificación SIZE no debe ser mayor que el límite superior.

</dd> </dl>

## <a name="fatal-error-1064"></a>Error irresal 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Error>: " <fileName> :<line \#>: SEQUENCE item does <identifier> not resolve to an OBJECT-TYPE"**
</dt> <dd>

Error semántico del módulo de asignación de tipos, específico de SNMPv1 ni SNMPv2C. Todos los elementos individuales de una declaración SEQUENCE deben resolverse como OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1070"></a>Error irresal 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Error>: "<línea>: El módulo MIB , desde el que se importa el símbolo, no está presente en la <fileName> \# <moduleName> <symbolName> entrada"**
</dt> <dd>

Error semántico del módulo en la referencia cruzada, específico de SNMPv1 ni SNMPv2C. Si uno de los módulos de la sección IMPORTS del módulo principal o un módulo de subsidiarias no existe y se hace referencia realmente a uno o varios símbolos de este módulo, se produce este error grave.

</dd> </dl>

 

 



