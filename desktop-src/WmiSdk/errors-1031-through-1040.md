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
# <a name="errors-1031-through-1040"></a>Errores de 1031 a 1040

Describe los errores del proveedor SNMP de WMI de 1031 a 1040.

[ADVERTENCIA 1031](#warning-1031)

[Error irrecuperable 1032](#fatal-error-1032)

[Error irrecuperable 1033](#fatal-error-1033)

[ADVERTENCIA 1034](#warning-1034)

[ADVERTENCIA 1036](#warning-1036)

[Error irrecuperable 1037](#fatal-error-1037)

[Error irrecuperable 1038](#fatal-error-1038)

[Error irrecuperable 1039](#fatal-error-1039)

[Error irrecuperable 1040](#fatal-error-1040)

## <a name="warning-1031"></a>ADVERTENCIA 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, ADVERTENCIA>: " <fileName> : <línea \#>: el símbolo estándar <identifier> debe importarse desde el módulo <identifier> . Suponiendo la definición estándar ".**
</dt> <dd>

La sección de IMPORTAciones de la advertencia semántica del módulo, específica no es SNMPv1 ni SNMPv2C. Si un identificador SNMP conocido para el compilador se encuentra en la sección de IMPORTAciones, el módulo desde el que se importa debe ser uno de los módulos estándar.

Algunas de las IMPORTAciones usadas con frecuencia son "asumió el conocimiento" en la parte del compilador. No es necesario que el compilador requiera acceso a otros módulos de información para resolverlos.

Las IMPORTAciones integradas de SNMPv1 y SNMPv2C se describen en las tablas siguientes.

</dd> </dl>

**IMPORTAciones de SNMPv1 integradas**



| Import (clase) | Módulo      | Instancias                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Valor ASN. 1  | RFC1155: SMI | Internet, directorio, administración, experimental, privado, empresas |
|              | RFC1213-MIB | MIB-II e IP, interfaces, transmisión                             |
| Tipo ASN. 1   | RFC1155: SMI | NetworkAddress, IpAddress, Counter, medidor, TimeTicks, opaco        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| Macro ASN. 1  | RFC-1212    | TIPO DE OBJETO                                                         |
|              | RFC-1215    | TIPO DE CAPTURA                                                           |



 

**IMPORTAciones de SNMPv2C integradas**



| Import (clase)       | Módulo      | Instancias                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor ASN. 1        | SNMPv2-SMI  | org, Dod, Internet, Directory, MGMT, MIB-2, Transmission, experimental, Private, Enterprises, Security, SNMPv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Identidad de objetos    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| Tipo ASN. 1         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32                                                                                                                             |
| Macro ASN. 1        | SNMPv2-SMI  | MÓDULO-IDENTIDAD, OBJETO-IDENTIDAD, TIPO DE OBJETO, TIPO DE NOTIFICACIÓN                                                                                                                                               |
|                    | SNMPv2-CONF | GRUPO DE OBJETOS, GRUPO DE NOTIFICACIONES, CUMPLIMIENTO DE MÓDULOS, CAPACIDADES DE AGENTE                                                                                                                                        |
|                    | SNMPv2-TC   | CONVENCIÓN TEXTUAL                                                                                                                                                                                             |
| Convención textual | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Error irrecuperable 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> grave: " <fileName><\#> de línea: valor duplicado <value> en la enumeración"**
</dt> <dd>

Error semántico del módulo en una enumeración, específico no es SNMPv1 ni SNMPv2C. No debe haber valores duplicados. El parámetro> de línea <\# es la posición de la periodicidad del nombre o valor.

</dd> </dl>

## <a name="fatal-error-1033"></a>Error irrecuperable 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> grave: " <fileName><\#> de línea: nombre duplicado <identifier> en la enumeración"**
</dt> <dd>

Error semántico del módulo en una enumeración, específico no es SNMPv1 ni SNMPv2C. No debe haber nombres duplicados. El parámetro> de línea <\# es la posición de la periodicidad del nombre o valor.

</dd> </dl>

## <a name="warning-1034"></a>ADVERTENCIA 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, ADVERTENCIA>: " <fileName><> de línea \# : un valor de 0 no se permite en una enumeración"**
</dt> <dd>

ADVERTENCIA semántica del módulo en una enumeración, específica no es SNMPv1 ni SNMPv2C. Se recomienda no utilizar un valor con nombre de cero en una enumeración.

</dd> </dl>

## <a name="warning-1036"></a>ADVERTENCIA 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, ADVERTENCIA> " <fileName><\#> de línea: el valor de la enumeración no se resuelve como un entero positivo"**
</dt> <dd>

ADVERTENCIA semántica del módulo en una enumeración, específica no es SNMPv1 ni SNMPv2C. No se permite un valor negativo en una enumeración.

</dd> </dl>

## <a name="fatal-error-1037"></a>Error irrecuperable 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> grave: " <fileName><\#> de línea: el identificador <identifier> no se resuelve como una cadena de octeto o tipos opacos"**
</dt> <dd>

Error semántico del módulo en la especificación de tamaño, específico no es SNMPv1 ni SNMPv2C. El símbolo que se usa en una especificación de tamaño debe resolverse como una cadena de octeto o opaca.

</dd> </dl>

## <a name="fatal-error-1038"></a>Error irrecuperable 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> grave: " <fileName><\#> de línea: el identificador <identifier> no resuelve un entero o tipo de medidor"**
</dt> <dd>

Error semántico del módulo en la especificación del intervalo. Este error puede producirse en SNMPv1 o SNMPv2C.

En SNMPv1, el símbolo que se usa en una especificación de intervalo debe resolverse en un entero o medidor.

En SNMPv2C, el símbolo que se usa en una especificación de intervalo debe resolverse en Integer, Gauge32, Integer32 o Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Error irrecuperable 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> irrecuperable: <fileName><\# de línea>: valor negativo usado en la especificación de tamaño "**
</dt> <dd>

Error semántico del módulo en la especificación de tamaño, específico no es SNMPv1 ni SNMPv2C. Cualquier valor usado para especificar el tamaño no debe ser negativo.

</dd> </dl>

## <a name="fatal-error-1040"></a>Error irrecuperable 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> grave: " <fileName><\#> de línea: <identifier> el identificador de la especificación de tamaño no se resuelve como un valor entero no negativo"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 o SNMPv2C. Cualquier símbolo usado en la especificación de un valor en una especificación de tamaño se resuelve como un valor no negativo.

</dd> </dl>

 

 



