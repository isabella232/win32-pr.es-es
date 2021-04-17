---
description: Describe los errores del proveedor SNMP de WMI de 1031 a 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Errores de 1031 a 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668097"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="76912-103">Errores de 1031 a 1040</span><span class="sxs-lookup"><span data-stu-id="76912-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="76912-104">Describe los errores del proveedor SNMP de WMI de 1031 a 1040.</span><span class="sxs-lookup"><span data-stu-id="76912-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="76912-105">ADVERTENCIA 1031</span><span class="sxs-lookup"><span data-stu-id="76912-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="76912-106">Error irrecuperable 1032</span><span class="sxs-lookup"><span data-stu-id="76912-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="76912-107">Error irrecuperable 1033</span><span class="sxs-lookup"><span data-stu-id="76912-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="76912-108">ADVERTENCIA 1034</span><span class="sxs-lookup"><span data-stu-id="76912-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="76912-109">ADVERTENCIA 1036</span><span class="sxs-lookup"><span data-stu-id="76912-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="76912-110">Error irrecuperable 1037</span><span class="sxs-lookup"><span data-stu-id="76912-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="76912-111">Error irrecuperable 1038</span><span class="sxs-lookup"><span data-stu-id="76912-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="76912-112">Error irrecuperable 1039</span><span class="sxs-lookup"><span data-stu-id="76912-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="76912-113">Error irrecuperable 1040</span><span class="sxs-lookup"><span data-stu-id="76912-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="76912-114">ADVERTENCIA 1031</span><span class="sxs-lookup"><span data-stu-id="76912-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="76912-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, ADVERTENCIA>: " <fileName> : <línea \#>: el símbolo estándar <identifier> debe importarse desde el módulo <identifier> . Suponiendo la definición estándar ".**</span><span class="sxs-lookup"><span data-stu-id="76912-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="76912-116">La sección de IMPORTAciones de la advertencia semántica del módulo, específica no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-117">Si un identificador SNMP conocido para el compilador se encuentra en la sección de IMPORTAciones, el módulo desde el que se importa debe ser uno de los módulos estándar.</span><span class="sxs-lookup"><span data-stu-id="76912-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="76912-118">Algunas de las IMPORTAciones usadas con frecuencia son "asumió el conocimiento" en la parte del compilador.</span><span class="sxs-lookup"><span data-stu-id="76912-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="76912-119">No es necesario que el compilador requiera acceso a otros módulos de información para resolverlos.</span><span class="sxs-lookup"><span data-stu-id="76912-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="76912-120">Las IMPORTAciones integradas de SNMPv1 y SNMPv2C se describen en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="76912-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="76912-121">**IMPORTAciones de SNMPv1 integradas**</span><span class="sxs-lookup"><span data-stu-id="76912-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="76912-122">Import (clase)</span><span class="sxs-lookup"><span data-stu-id="76912-122">Import Class</span></span> | <span data-ttu-id="76912-123">Módulo</span><span class="sxs-lookup"><span data-stu-id="76912-123">Module</span></span>      | <span data-ttu-id="76912-124">Instancias</span><span class="sxs-lookup"><span data-stu-id="76912-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="76912-125">Valor ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-125">ASN.1 Value</span></span>  | <span data-ttu-id="76912-126">RFC1155: SMI</span><span class="sxs-lookup"><span data-stu-id="76912-126">RFC1155-SMI</span></span> | <span data-ttu-id="76912-127">Internet, directorio, administración, experimental, privado, empresas</span><span class="sxs-lookup"><span data-stu-id="76912-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="76912-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="76912-128">RFC1213-MIB</span></span> | <span data-ttu-id="76912-129">MIB-II e IP, interfaces, transmisión</span><span class="sxs-lookup"><span data-stu-id="76912-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="76912-130">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-130">ASN.1 Type</span></span>   | <span data-ttu-id="76912-131">RFC1155: SMI</span><span class="sxs-lookup"><span data-stu-id="76912-131">RFC1155-SMI</span></span> | <span data-ttu-id="76912-132">NetworkAddress, IpAddress, Counter, medidor, TimeTicks, opaco</span><span class="sxs-lookup"><span data-stu-id="76912-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="76912-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="76912-133">RFC1213-MIB</span></span> | <span data-ttu-id="76912-134">DisplayString, PhysAddress</span><span class="sxs-lookup"><span data-stu-id="76912-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="76912-135">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-135">ASN.1 Macro</span></span>  | <span data-ttu-id="76912-136">RFC-1212</span><span class="sxs-lookup"><span data-stu-id="76912-136">RFC-1212</span></span>    | <span data-ttu-id="76912-137">TIPO DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="76912-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="76912-138">RFC-1215</span><span class="sxs-lookup"><span data-stu-id="76912-138">RFC-1215</span></span>    | <span data-ttu-id="76912-139">TIPO DE CAPTURA</span><span class="sxs-lookup"><span data-stu-id="76912-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="76912-140">**IMPORTAciones de SNMPv2C integradas**</span><span class="sxs-lookup"><span data-stu-id="76912-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="76912-141">Import (clase)</span><span class="sxs-lookup"><span data-stu-id="76912-141">Import Class</span></span>       | <span data-ttu-id="76912-142">Módulo</span><span class="sxs-lookup"><span data-stu-id="76912-142">Module</span></span>      | <span data-ttu-id="76912-143">Instancias</span><span class="sxs-lookup"><span data-stu-id="76912-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76912-144">Valor ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-144">ASN.1 Value</span></span>        | <span data-ttu-id="76912-145">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="76912-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="76912-146">org, Dod, Internet, Directory, MGMT, MIB-2, Transmission, experimental, Private, Enterprises, Security, SNMPv2, snmpDomains, snmpProxys, snmpModules</span><span class="sxs-lookup"><span data-stu-id="76912-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="76912-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="76912-147">SNMPv2-TM</span></span>   | <span data-ttu-id="76912-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="76912-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="76912-149">Identidad de objetos</span><span class="sxs-lookup"><span data-stu-id="76912-149">Object Identity</span></span>    | <span data-ttu-id="76912-150">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="76912-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="76912-151">zeroDotZero</span><span class="sxs-lookup"><span data-stu-id="76912-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="76912-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="76912-152">SNMPv2-TM</span></span>   | <span data-ttu-id="76912-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="76912-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="76912-154">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-154">ASN.1 Type</span></span>         | <span data-ttu-id="76912-155">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="76912-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="76912-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span><span class="sxs-lookup"><span data-stu-id="76912-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="76912-157">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="76912-157">ASN.1 Macro</span></span>        | <span data-ttu-id="76912-158">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="76912-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="76912-159">MÓDULO-IDENTIDAD, OBJETO-IDENTIDAD, TIPO DE OBJETO, TIPO DE NOTIFICACIÓN</span><span class="sxs-lookup"><span data-stu-id="76912-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="76912-160">SNMPv2-CONF</span><span class="sxs-lookup"><span data-stu-id="76912-160">SNMPv2-CONF</span></span> | <span data-ttu-id="76912-161">GRUPO DE OBJETOS, GRUPO DE NOTIFICACIONES, CUMPLIMIENTO DE MÓDULOS, CAPACIDADES DE AGENTE</span><span class="sxs-lookup"><span data-stu-id="76912-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="76912-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="76912-162">SNMPv2-TC</span></span>   | <span data-ttu-id="76912-163">CONVENCIÓN TEXTUAL</span><span class="sxs-lookup"><span data-stu-id="76912-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="76912-164">Convención textual</span><span class="sxs-lookup"><span data-stu-id="76912-164">Textual Convention</span></span> | <span data-ttu-id="76912-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="76912-165">SNMPv2-TC</span></span>   | <span data-ttu-id="76912-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span><span class="sxs-lookup"><span data-stu-id="76912-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="76912-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="76912-167">SNMPv2-TM</span></span>   | <span data-ttu-id="76912-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="76912-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="76912-169">Error irrecuperable 1032</span><span class="sxs-lookup"><span data-stu-id="76912-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="76912-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> grave: " <fileName><\#> de línea: valor duplicado <value> en la enumeración"**</span><span class="sxs-lookup"><span data-stu-id="76912-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-171">Error semántico del módulo en una enumeración, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-172">No debe haber valores duplicados.</span><span class="sxs-lookup"><span data-stu-id="76912-172">There must not be any duplicate values.</span></span> <span data-ttu-id="76912-173">El parámetro> de línea <\# es la posición de la periodicidad del nombre o valor.</span><span class="sxs-lookup"><span data-stu-id="76912-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="76912-174">Error irrecuperable 1033</span><span class="sxs-lookup"><span data-stu-id="76912-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="76912-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> grave: " <fileName><\#> de línea: nombre duplicado <identifier> en la enumeración"**</span><span class="sxs-lookup"><span data-stu-id="76912-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-176">Error semántico del módulo en una enumeración, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-177">No debe haber nombres duplicados.</span><span class="sxs-lookup"><span data-stu-id="76912-177">There must not be any duplicate names.</span></span> <span data-ttu-id="76912-178">El parámetro> de línea <\# es la posición de la periodicidad del nombre o valor.</span><span class="sxs-lookup"><span data-stu-id="76912-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="76912-179">ADVERTENCIA 1034</span><span class="sxs-lookup"><span data-stu-id="76912-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="76912-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, ADVERTENCIA>: " <fileName><> de línea \# : un valor de 0 no se permite en una enumeración"**</span><span class="sxs-lookup"><span data-stu-id="76912-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-181">ADVERTENCIA semántica del módulo en una enumeración, específica no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-182">Se recomienda no utilizar un valor con nombre de cero en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="76912-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="76912-183">ADVERTENCIA 1036</span><span class="sxs-lookup"><span data-stu-id="76912-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="76912-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, ADVERTENCIA> " <fileName><\#> de línea: el valor de la enumeración no se resuelve como un entero positivo"**</span><span class="sxs-lookup"><span data-stu-id="76912-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-185">ADVERTENCIA semántica del módulo en una enumeración, específica no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-186">No se permite un valor negativo en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="76912-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="76912-187">Error irrecuperable 1037</span><span class="sxs-lookup"><span data-stu-id="76912-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="76912-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> grave: " <fileName><\#> de línea: el identificador <identifier> no se resuelve como una cadena de octeto o tipos opacos"**</span><span class="sxs-lookup"><span data-stu-id="76912-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-189">Error semántico del módulo en la especificación de tamaño, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-190">El símbolo que se usa en una especificación de tamaño debe resolverse como una cadena de octeto o opaca.</span><span class="sxs-lookup"><span data-stu-id="76912-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="76912-191">Error irrecuperable 1038</span><span class="sxs-lookup"><span data-stu-id="76912-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="76912-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> grave: " <fileName><\#> de línea: el identificador <identifier> no resuelve un entero o tipo de medidor"**</span><span class="sxs-lookup"><span data-stu-id="76912-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-193">Error semántico del módulo en la especificación del intervalo.</span><span class="sxs-lookup"><span data-stu-id="76912-193">Module semantic error in range specification.</span></span> <span data-ttu-id="76912-194">Este error puede producirse en SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="76912-195">En SNMPv1, el símbolo que se usa en una especificación de intervalo debe resolverse en un entero o medidor.</span><span class="sxs-lookup"><span data-stu-id="76912-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="76912-196">En SNMPv2C, el símbolo que se usa en una especificación de intervalo debe resolverse en Integer, Gauge32, Integer32 o Unsigned32.</span><span class="sxs-lookup"><span data-stu-id="76912-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="76912-197">Error irrecuperable 1039</span><span class="sxs-lookup"><span data-stu-id="76912-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="76912-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> irrecuperable: <fileName><\# de línea>: valor negativo usado en la especificación de tamaño "**</span><span class="sxs-lookup"><span data-stu-id="76912-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-199">Error semántico del módulo en la especificación de tamaño, específico no es SNMPv1 ni SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-200">Cualquier valor usado para especificar el tamaño no debe ser negativo.</span><span class="sxs-lookup"><span data-stu-id="76912-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="76912-201">Error irrecuperable 1040</span><span class="sxs-lookup"><span data-stu-id="76912-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="76912-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> grave: " <fileName><\#> de línea: <identifier> el identificador de la especificación de tamaño no se resuelve como un valor entero no negativo"**</span><span class="sxs-lookup"><span data-stu-id="76912-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="76912-203">Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="76912-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="76912-204">Cualquier símbolo usado en la especificación de un valor en una especificación de tamaño se resuelve como un valor no negativo.</span><span class="sxs-lookup"><span data-stu-id="76912-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



