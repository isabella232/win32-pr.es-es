---
description: Describe los errores del proveedor SNMP de WMI de 1061 a 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Errores de 1061 a 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696926"
---
# <a name="errors-1061-through-1070"></a><span data-ttu-id="d7b21-103">Errores de 1061 a 1070</span><span class="sxs-lookup"><span data-stu-id="d7b21-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="d7b21-104">Describe los errores del proveedor SNMP de WMI de 1061 a 1070.</span><span class="sxs-lookup"><span data-stu-id="d7b21-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="d7b21-105">Error irrecuperable 1063</span><span class="sxs-lookup"><span data-stu-id="d7b21-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="d7b21-106">Error irrecuperable 1064</span><span class="sxs-lookup"><span data-stu-id="d7b21-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="d7b21-107">Error irrecuperable 1070</span><span class="sxs-lookup"><span data-stu-id="d7b21-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="d7b21-108">Error irrecuperable 1063</span><span class="sxs-lookup"><span data-stu-id="d7b21-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="d7b21-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> grave: " <fileName><línea \#>: el límite superior de la especificación de tamaño es menor que el límite inferior"**</span><span class="sxs-lookup"><span data-stu-id="d7b21-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="d7b21-110">Error semántico del módulo en la especificación de tamaño, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7b21-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d7b21-111">El símbolo que se usa en una especificación de tamaño debe resolverse como una cadena de octeto o opaca.</span><span class="sxs-lookup"><span data-stu-id="d7b21-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="d7b21-112">El límite inferior de una especificación de intervalo o de tamaño no debe ser mayor que el límite superior.</span><span class="sxs-lookup"><span data-stu-id="d7b21-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="d7b21-113">Error irrecuperable 1064</span><span class="sxs-lookup"><span data-stu-id="d7b21-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="d7b21-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> irrecuperable: " <fileName> : <línea \#>: el elemento <identifier> de secuencia no se resuelve como un tipo de objeto"**</span><span class="sxs-lookup"><span data-stu-id="d7b21-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="d7b21-115">Error semántico del módulo de asignación de tipos, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7b21-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d7b21-116">Todos los elementos individuales de una declaración de secuencia deben resolverse en un tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="d7b21-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="d7b21-117">Error irrecuperable 1070</span><span class="sxs-lookup"><span data-stu-id="d7b21-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="d7b21-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> grave: " <fileName><\#> de línea: módulo MIB <moduleName> , desde el que <symbolName> se importa el símbolo, no está presente en la entrada"**</span><span class="sxs-lookup"><span data-stu-id="d7b21-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="d7b21-119">Error semántico del módulo en referencias cruzadas, específicas de SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7b21-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d7b21-120">Si uno de los módulos de la sección IMPORTAciones del módulo principal o de un módulo subsidiario no existe y se hace referencia realmente a uno o varios símbolos de este módulo, se produce este error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="d7b21-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



