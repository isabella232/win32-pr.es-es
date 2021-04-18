---
description: Describe los errores del proveedor SNMP de WMI de 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errores de 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697472"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="e1572-103">Errores de 1051 a 1060</span><span class="sxs-lookup"><span data-stu-id="e1572-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="e1572-104">Describe los errores del proveedor SNMP de WMI de 1051 a 1060.</span><span class="sxs-lookup"><span data-stu-id="e1572-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="e1572-105">Error irrecuperable 1051</span><span class="sxs-lookup"><span data-stu-id="e1572-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="e1572-106">Error irrecuperable 1054</span><span class="sxs-lookup"><span data-stu-id="e1572-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="e1572-107">Error irrecuperable 1055</span><span class="sxs-lookup"><span data-stu-id="e1572-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="e1572-108">Error irrecuperable 1051</span><span class="sxs-lookup"><span data-stu-id="e1572-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="e1572-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> irrecuperable: " <fileName> : <línea \#>: referencia ambigua al símbolo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="e1572-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="e1572-110">Error semántico del módulo de la sección Imports, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e1572-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="e1572-111">Cada descriptor de objeto que corresponde a un objeto en una MIB estándar de Internet debe ser único.</span><span class="sxs-lookup"><span data-stu-id="e1572-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="e1572-112">Dado que las MIB empresariales pueden tener descriptores de objeto comunes, estos descriptores importados de dos módulos deben usarse sin ambigüedades en el módulo MIB mediante el uso de la notación "module. descriptor".</span><span class="sxs-lookup"><span data-stu-id="e1572-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="e1572-113">Error irrecuperable 1054</span><span class="sxs-lookup"><span data-stu-id="e1572-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="e1572-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> grave: " <fileName> : <línea \#>: <identifier> en la cláusula index no se resuelve como uno de los tipos permitidos"**</span><span class="sxs-lookup"><span data-stu-id="e1572-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="e1572-115">Error semántico del módulo de invocación de macros **de tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="e1572-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="e1572-116">El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, una secuencia sin secuencia o no de tipo.</span><span class="sxs-lookup"><span data-stu-id="e1572-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="e1572-117">Cualquier tipo especificado en la cláusula INDEX también debe resolverse en uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="e1572-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="e1572-118">Este error puede producirse en SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e1572-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="e1572-119">Error irrecuperable 1055</span><span class="sxs-lookup"><span data-stu-id="e1572-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="e1572-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> irrecuperable: " <fileName> : <línea \#>: la sintaxis de tipo de objeto de índice <identifier> no se resuelve como uno de los tipos permitidos"**</span><span class="sxs-lookup"><span data-stu-id="e1572-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="e1572-121">Error semántico del módulo de invocación de macros **de tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="e1572-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="e1572-122">El tipo de un objeto de la cláusula INDEX, o cualquier tipo especificado en la cláusula INDEX, debe resolverse en un tipo escalar, es decir, una secuencia sin secuencia o no de tipo.</span><span class="sxs-lookup"><span data-stu-id="e1572-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="e1572-123">Este error puede producirse en SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e1572-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



