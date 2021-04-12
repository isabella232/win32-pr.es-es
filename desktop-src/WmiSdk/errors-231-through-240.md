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
# <a name="errors-231-through-240"></a>Errores de 231 a 240

Describe los errores del proveedor SNMP de WMI de 231 a 240.

[Error irrecuperable 232](#fatal-error-232)

[Error irrecuperable 233](#fatal-error-233)

[Error irrecuperable 234](#fatal-error-234)

[Error irrecuperable 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Error irrecuperable 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> irrecuperable: " <fileName> : <línea \#>: invocación de la opción de tipo objeto SMI de SNMPv1 no permitida"**
</dt> <dd>

Error de sintaxis de módulo. Ha usado la invocación de **tipo de objeto** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c** , que requiere una compatibilidad estricta con la sintaxis de SNMPv2c.

</dd> </dl>

## <a name="fatal-error-233"></a>Error irrecuperable 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> irrecuperable: " <fileName> : <línea \#>: invocación de la llamada de la opción SNMPv1 SMI-Type no permitido"**
</dt> <dd>

Error de sintaxis de módulo. Ha usado la invocación de **tipo de captura** específica de SNMPv1 en la MIB, pero ha especificado el modificador **/v2c** , que requiere una compatibilidad estricta con la sintaxis de SNMPv2c.

</dd> </dl>

## <a name="fatal-error-234"></a>Error irrecuperable 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irrecuperable: " <fileName> : <línea \#>: la invocación de módulo-identidad solo se permite inmediatamente después de la sección de importaciones"**
</dt> <dd>

Error de sintaxis de módulo. La invocación de la **identidad del módulo** se ha colocado indirectamente.

</dd> </dl>

## <a name="fatal-error-236"></a>Error irrecuperable 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irrecuperable: " <fileName> : <línea \#>: el número no cabe en la representación de bits 32 que usa el compilador"**
</dt> <dd>

Error de sintaxis de módulo en la asignación de valores. Hay un error de asignación de valor de MIB en el que un valor entero es tan grande que requiere más de 32 bits para representarlo.

</dd> </dl>

 

 



