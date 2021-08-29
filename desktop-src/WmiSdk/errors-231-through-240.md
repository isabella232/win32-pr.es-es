---
description: Describe los errores del proveedor SNMP de WMI del 231 al 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Errores del 231 al 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bf38ca62f543122ee937d7759ebd5655470a54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880874"
---
# <a name="errors-231-through-240"></a>Errores del 231 al 240

Describe los errores del proveedor SNMP de WMI del 231 al 240.

[Error irresal 232](#fatal-error-232)

[Error irreales 233](#fatal-error-233)

[Error irresal 234](#fatal-error-234)

[Error irreales 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Error irresal 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, Fatal>:" &lt; fileName &gt; :<line \#>:Invocation of SNMPv1 SMI OBJECT-TYPE disallowed"**
</dt> <dd>

Error de sintaxis del módulo. Ha usado la invocación **OBJECT-TYPE** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c,** que requiere una conformidad estricta con la sintaxis de SNMPv2C.

</dd> </dl>

## <a name="fatal-error-233"></a>Error irresal 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, Fatal>: " &lt; fileName &gt; :<line \#>: Invocation of SNMPv1 SMI TRAP-TYPE disallowed"**
</dt> <dd>

Error de sintaxis del módulo. Ha usado la invocación **TRAP-TYPE** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c,** que requiere una conformidad estricta con la sintaxis de SNMPv2C.

</dd> </dl>

## <a name="fatal-error-234"></a>Error irresal 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, Fatal>:" &lt; fileName &gt; :<line \#>: MODULE-IDENTITY invocation is allowed only immediately after the IMPORTS section"**
</dt> <dd>

Error de sintaxis del módulo. La **invocación MODULE-IDENTITY** está fuera de lugar.

</dd> </dl>

## <a name="fatal-error-236"></a>Error irresal 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, Error>: " &lt; fileName &gt; :<line \#>: Number does not fit into the 32 bit representation used by the compiler"**
</dt> <dd>

Error de sintaxis del módulo en la asignación de valores. Hay un error de asignación de valor MIB en el que un valor entero es tan grande que requiere más de 32 bits para representarlo.

</dd> </dl>

 

 



