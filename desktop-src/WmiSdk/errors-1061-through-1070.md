---
description: Describe los errores del proveedor WMI SNMP del 1061 al 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Errores del 1061 al 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da7fb7eeacf9200e96890581766bfe31d9f19c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270303"
---
# <a name="errors-1061-through-1070"></a>Errores del 1061 al 1070

Describe los errores del proveedor WMI SNMP del 1061 al 1070.

[Error irreales 1063](#fatal-error-1063)

[Error irreales 1064](#fatal-error-1064)

[Error irreales 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Error irreales 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, error irresal>: " fileName<line>: el límite superior de la especificación SIZE es menor que el &lt; &gt; límite \# inferior"**
</dt> <dd>

Error semántico del módulo en la especificación SIZE, específico de SNMPv1 ni SNMPv2C. El símbolo usado en una especificación SIZE debe resolverse en OCTET STRING o Opaque. El límite inferior de un intervalo o especificación SIZE no debe ser mayor que el límite superior.

</dd> </dl>

## <a name="fatal-error-1064"></a>Error irreales 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, error irresal>: " &lt; fileName &gt; :<line \#>: sequence item &lt; identifier does not resolve to an &gt; OBJECT-TYPE"**
</dt> <dd>

Error semántico del módulo de asignación de tipos, específico de SNMPv1 ni SNMPv2C. Todos los elementos individuales de una declaración SEQUENCE deben resolverse en OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1070"></a>Error irreales 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, error irresal>: " &lt; fileName &gt;<line \#>: MIB Module moduleName , desde el que se importa &lt; &gt; &lt; symbolName, &gt; no está presente en la entrada"**
</dt> <dd>

Error semántico del módulo en la referencia cruzada, específico de SNMPv1 ni SNMPv2C. Si uno de los módulos de la sección IMPORTS del módulo principal o un módulo de subsidiarias no existe y se hace referencia realmente a uno o varios símbolos de este módulo, se produce este error irresal.

</dd> </dl>

 

 



