---
description: Las convenciones de texto de SNMP se asignan a tipos definidos por CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de Convención de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706031"
---
# <a name="textual-convention-macro"></a>Macro de Convención de texto

Las convenciones de texto de SNMP se asignan a tipos definidos por CIM.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Las siguientes reglas de asignación se aplican a las convenciones de texto de SNMP:

-   La definición de tipo con nombre de la cláusula de sintaxis se asigna literalmente a **la \_ Sintaxis de objeto** de calificador de propiedad CIM.
-   Use la tabla siguiente para asignar convenciones de texto cuando la cláusula de sintaxis hace referencia de forma explícita a una Convención textual de una macro de Convención de texto SNMPv2C o hace referencia a una Convención textual implícita. El valor predeterminado es siempre **null**.



| Convención textual | Tipo de variante CIM | Calificador de CIM                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **\_ Convención textual**: DateAndTime<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: DateAndTime<br/> **CIMTYPE**: cadena<br/>       |
| Displaystring      | **VT \_ BSTR**     | **\_ Convención textual**: Displaystring<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: Displaystring<br/> **CIMTYPE**: cadena<br/>   |
| MacAddress         | **VT \_ BSTR**     | **\_ Convención textual**: MacAddress<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: MacAddress<br/> **CIMTYPE**: cadena<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **\_ Convención textual**: PhysAddress<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: PhysAddress<br/> **CIMTYPE**: cadena<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **\_ Convención textual**: SnmpUDPAddress<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: SnmpUDPAddress<br/> **CIMTYPE**: cadena<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **\_ Convención textual**: SnmpOSIAddress<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: SnmpOSIAddress<br/> **CIMTYPE**: cadena<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **\_ Convención textual**: SnmpIPXAddress<br/> **codificación**: OCTETSTRING<br/> **\_ Sintaxis de objeto**: SnmpIPXAddress<br/> **CIMTYPE**: cadena<br/> |



 

-   El tipo Variant definido por CIM y los calificadores de propiedad CIM, la **\_ Convención textual**, la **codificación**, la **\_ Sintaxis de objeto** y la asignación **CIMTYPE** mediante el tipo primitivo subyacente.
-   La cláusula DISPLAY-HINT de la macro de Convención de texto SNMPv2C se asigna literalmente a la **\_ sugerencia de presentación** del calificador de propiedad CIM. Este calificador no se genera si no hay ninguna macro de Convención de texto o la macro no contiene una cláusula de sugerencia de presentación.

## <a name="example-code"></a>Código de ejemplo

En el siguiente ejemplo se describe una Convención textual de SNMPv1.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

Este ejemplo genera los siguientes calificadores CIM.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

En el siguiente ejemplo se describe una Convención textual de SNMPv2.

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

Este ejemplo genera los siguientes calificadores CIM.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




