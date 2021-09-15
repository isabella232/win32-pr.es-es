---
description: Describe los errores del proveedor SNMP de WMI del 1031 al 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Errores del 1031 al 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5986ba80a55d2d8f3d4a87b0587331765aa38d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270316"
---
# <a name="errors-1031-through-1040"></a>Errores del 1031 al 1040

Describe los errores del proveedor SNMP de WMI del 1031 al 1040.

[Advertencia 1031](#warning-1031)

[Error irreales 1032](#fatal-error-1032)

[Error irreales 1033](#fatal-error-1033)

[Advertencia 1034](#warning-1034)

[Advertencia 1036](#warning-1036)

[Error irreales 1037](#fatal-error-1037)

[Error irreales 1038](#fatal-error-1038)

[Error irreales 1039](#fatal-error-1039)

[Error irreales 1040](#fatal-error-1040)

## <a name="warning-1031"></a>Advertencia 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Advertencia>: " &lt; fileName &gt; :<line \#>: El &lt; &gt; &lt; identificador de símbolo estándar debe importarse desde el identificador del módulo &gt; . Suponiendo la definición estándar."**
</dt> <dd>

Advertencia semántica del módulo imports section, específica de SNMPv1 ni SNMPv2C. Si un identificador SNMP conocido por el compilador está en la sección IMPORTS, el módulo desde el que se importa debe ser uno de los módulos estándar.

Ciertas importaciones usadas con frecuencia son "conocimientos asumidos" por parte del compilador. No es necesario que el compilador requiera acceso a otros módulos de información para resolverlos.

Las importaciones integradas de SNMPv1 y SNMPv2C se describen en las tablas siguientes.

</dd> </dl>

**Importaciones de SNMPv1 integradas**



| Import (clase) | Módulo      | Instancias                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Valor asn.1  | RFC1155-SMI | Internet, directorio, administración, experimental, privada, empresas |
|              | RFC1213-MIB | MIB-II e IP, interfaces, transmisión                             |
| Tipo ASN.1   | RFC1155-SMI | NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| ASN.1 Macro  | RFC-1212    | OBJECT-TYPE                                                         |
|              | RFC-1215    | TRAP-TYPE                                                           |



 

**Importaciones de SNMPv2C integradas**



| Import (clase)       | Módulo      | Instancias                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor asn.1        | SNMPv2-SMI  | org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Identidad de objetos    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| Tipo ASN.1         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32                                                                                                                             |
| ASN.1 Macro        | SNMPv2-SMI  | MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE                                                                                                                                               |
|                    | SNMPv2-CONF | OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES                                                                                                                                        |
|                    | SNMPv2-TC   | TEXTUAL-CONVENTION                                                                                                                                                                                             |
| Convención textual | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Error irreales 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Error irresumen>: " fileName<línea>: Valor duplicado en &lt; &gt; la \# &lt; &gt; enumeración"**
</dt> <dd>

Error semántico del módulo en una enumeración, específica de SNMPv1 ni SNMPv2C. No debe haber ningún valor duplicado. El <línea \#> parámetro es la posición de la periodicidad del nombre o valor.

</dd> </dl>

## <a name="fatal-error-1033"></a>Error irreales 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Error irre>: " fileName<línea>: Identificador de nombre duplicado en &lt; &gt; \# &lt; &gt; enumeración"**
</dt> <dd>

Error semántico del módulo en una enumeración, específica de SNMPv1 ni SNMPv2C. No debe haber nombres duplicados. El <línea \#> parámetro es la posición de la periodicidad del nombre o valor.

</dd> </dl>

## <a name="warning-1034"></a>Advertencia 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Advertencia>: " fileName<line>: Un valor de 0 no permitido en una &lt; &gt; \# enumeración"**
</dt> <dd>

Advertencia semántica de módulo en una enumeración, específica de SNMPv1 ni SNMPv2C. Se recomienda que no se utilice un valor con nombre de cero en una enumeración.

</dd> </dl>

## <a name="warning-1036"></a>Advertencia 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Advertencia> " fileName<line>: El valor de la enumeración no se resuelve &lt; &gt; como un entero \# positivo"**
</dt> <dd>

Advertencia semántica de módulo en una enumeración, específica de SNMPv1 ni SNMPv2C. No se permite un valor negativo en una enumeración.

</dd> </dl>

## <a name="fatal-error-1037"></a>Error irreales 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Error irrespeto>: " fileName<line>: Identificador identificador no se resuelve en tipos OCTET STRING u &lt; &gt; \# &lt; &gt; Opacos"**
</dt> <dd>

Error semántico del módulo en la especificación SIZE, específico de SNMPv1 ni SNMPv2C. El símbolo usado en una especificación SIZE debe resolverse en OCTET STRING o Opaque.

</dd> </dl>

## <a name="fatal-error-1038"></a>Error irreales 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, error irresal>: " &lt; fileName<line>: Identificador de identificador no resuelve un tipo INTEGER o &gt; \# &lt; &gt; Gauge"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo. Este error puede producirse en SNMPv1 o SNMPv2C.

En SNMPv1, el símbolo usado en una especificación range debe resolverse en INTEGER o Gauge.

En SNMPv2C, el símbolo usado en una especificación range debe resolverse en INTEGER, Gauge32, Integer32 o Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Error irreales 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Error irresal>: fileName<línea>: Valor negativo usado en la especificación &lt; &gt; \# SIZE"**
</dt> <dd>

Error semántico del módulo en la especificación SIZE, específico de SNMPv1 ni SNMPv2C. Cualquier valor utilizado para especificar size debe ser no negativo.

</dd> </dl>

## <a name="fatal-error-1040"></a>Error irreales 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, error irresal>: " fileName<line>: Identificador de identificador en la especificación SIZE no se resuelve como un valor &lt; &gt; entero no \# &lt; &gt; negativo"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 ni SNMPv2C. Cualquier símbolo utilizado para especificar un valor en una especificación SIZE se resuelve como un valor no negativo.

</dd> </dl>

 

 



