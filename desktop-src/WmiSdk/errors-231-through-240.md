---
description: Describe los errores del proveedor SNMP de WMI de 231 a 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Errores de 231 a 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278767"
---
# <a name="errors-231-through-240"></a><span data-ttu-id="d2b6f-103">Errores de 231 a 240</span><span class="sxs-lookup"><span data-stu-id="d2b6f-103">Errors 231 through 240</span></span>

<span data-ttu-id="d2b6f-104">Describe los errores del proveedor SNMP de WMI de 231 a 240.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-104">Describes WMI SNMP provider errors 231 through 240.</span></span>

[<span data-ttu-id="d2b6f-105">Error irrecuperable 232</span><span class="sxs-lookup"><span data-stu-id="d2b6f-105">Fatal Error 232</span></span>](#fatal-error-232)

[<span data-ttu-id="d2b6f-106">Error irrecuperable 233</span><span class="sxs-lookup"><span data-stu-id="d2b6f-106">Fatal Error 233</span></span>](#fatal-error-233)

[<span data-ttu-id="d2b6f-107">Error irrecuperable 234</span><span class="sxs-lookup"><span data-stu-id="d2b6f-107">Fatal Error 234</span></span>](#fatal-error-234)

[<span data-ttu-id="d2b6f-108">Error irrecuperable 236</span><span class="sxs-lookup"><span data-stu-id="d2b6f-108">Fatal Error 236</span></span>](#fatal-error-236)

## <a name="fatal-error-232"></a><span data-ttu-id="d2b6f-109">Error irrecuperable 232</span><span class="sxs-lookup"><span data-stu-id="d2b6f-109">Fatal Error 232</span></span>

<dl> <dt>

<span data-ttu-id="d2b6f-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> irrecuperable: " <fileName> : <línea \#>: invocación de la opción de tipo objeto SMI de SNMPv1 no permitida"**</span><span class="sxs-lookup"><span data-stu-id="d2b6f-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, Fatal>:"<fileName>:<line\#>:Invocation of SNMPv1 SMI OBJECT-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="d2b6f-111">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-111">Module syntax error.</span></span> <span data-ttu-id="d2b6f-112">Ha usado la invocación de **tipo de objeto** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c** , que requiere una compatibilidad estricta con la sintaxis de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-112">You have used the SNMPv1-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-233"></a><span data-ttu-id="d2b6f-113">Error irrecuperable 233</span><span class="sxs-lookup"><span data-stu-id="d2b6f-113">Fatal Error 233</span></span>

<dl> <dt>

<span data-ttu-id="d2b6f-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> irrecuperable: " <fileName> : <línea \#>: invocación de la llamada de la opción SNMPv1 SMI-Type no permitido"**</span><span class="sxs-lookup"><span data-stu-id="d2b6f-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, Fatal>: "<fileName>:<line\#>: Invocation of SNMPv1 SMI TRAP-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="d2b6f-115">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-115">Module syntax error.</span></span> <span data-ttu-id="d2b6f-116">Ha usado la invocación de **tipo de captura** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c** , que requiere una compatibilidad estricta con la sintaxis de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-116">You have used the SNMPv1-specific **TRAP-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-234"></a><span data-ttu-id="d2b6f-117">Error irrecuperable 234</span><span class="sxs-lookup"><span data-stu-id="d2b6f-117">Fatal Error 234</span></span>

<dl> <dt>

<span data-ttu-id="d2b6f-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irrecuperable: " <fileName> : <línea \#>: la invocación de módulo-identidad solo se permite inmediatamente después de la sección de importaciones"**</span><span class="sxs-lookup"><span data-stu-id="d2b6f-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, Fatal>:"<fileName>:<line\#>: MODULE-IDENTITY invocation is allowed only immediately after the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="d2b6f-119">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-119">Module syntax error.</span></span> <span data-ttu-id="d2b6f-120">La invocación de la **identidad del módulo** se ha colocado indirectamente.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-120">The **MODULE-IDENTITY** invocation is misplaced.</span></span>

</dd> </dl>

## <a name="fatal-error-236"></a><span data-ttu-id="d2b6f-121">Error irrecuperable 236</span><span class="sxs-lookup"><span data-stu-id="d2b6f-121">Fatal Error 236</span></span>

<dl> <dt>

<span data-ttu-id="d2b6f-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irrecuperable: " <fileName> : <línea \#>: el número no cabe en la representación de bits 32 que usa el compilador"**</span><span class="sxs-lookup"><span data-stu-id="d2b6f-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, Fatal>: "<fileName>:<line\#>: Number does not fit into the 32 bit representation used by the compiler"**</span></span>
</dt> <dd>

<span data-ttu-id="d2b6f-123">Error de sintaxis de módulo en la asignación de valores.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-123">Module syntax error in value assignment.</span></span> <span data-ttu-id="d2b6f-124">Hay un error de asignación de valor de MIB en el que un valor entero es tan grande que requiere más de 32 bits para representarlo.</span><span class="sxs-lookup"><span data-stu-id="d2b6f-124">There is a MIB value assignment error in which an integer value is so large that it requires more than 32 bits to represent it.</span></span>

</dd> </dl>

 

 



