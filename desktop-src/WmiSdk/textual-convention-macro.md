---
description: Las convenciones textuales de SNMP se asignan a tipos definidos por CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: TEXTUAL-CONVENTION (Macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973710"
---
# <a name="textual-convention-macro"></a>TEXTUAL-CONVENTION (Macro)

Las convenciones textuales de SNMP se asignan a tipos definidos por CIM.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Las siguientes reglas de asignación se aplican a las convenciones textuales de SNMP:

-   La definición de tipo con nombre de la cláusula SYNTAX asigna textualmente a la sintaxis del objeto calificador de **\_ propiedad** CIM .
-   Use la tabla siguiente para asignar convenciones textuales cuando la cláusula SYNTAX hace referencia explícitamente a una convención textual de una macro TEXTUAL-CONVENTION de SNMPv2C o hace referencia a una convención de texto implícita. El valor predeterminado es siempre **NULL.**



| Convención textual | Tipo de variante CIM | Calificador CIM                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **convención \_ textual:** DateAndTime<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto**: DateAndTime<br/> **cimtype**: string<br/>       |
| Displaystring      | **VT \_ BSTR**     | **convención \_ textual:** Displaystring<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto:** Displaystring<br/> **cimtype**: string<br/>   |
| MacAddress         | **VT \_ BSTR**     | **convención \_ textual:** MacAddress<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto:** MacAddress<br/> **cimtype**: string<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **convención \_ textual:** PhysAddress<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto**: PhysAddress<br/> **cimtype**: string<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **convención \_ textual:** SnmpUDPAddress<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto:** SnmpUDPAddress<br/> **cimtype**: string<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **convención \_ textual:** SnmpOSIAddress<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto:** SnmpOSIAddress<br/> **cimtype**: string<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **convención \_ textual:** SnmpIPXAddress<br/> **encoding:** OCTETSTRING<br/> **Sintaxis \_ de objeto:** SnmpIPXAddress<br/> **cimtype**: string<br/> |



 

-   El tipo de variante definido por CIM y los calificadores de propiedad CIM textual convención **, \_** codificación **,** sintaxis de objeto **y \_** **asignación cimtype** mediante el tipo primitivo subyacente.
-   La cláusula DISPLAY-HINT de la macro TEXTUAL-CONVENTION de SNMPv2C asigna textualmente a la sugerencia para mostrar del calificador **de \_ propiedad CIM**. Este calificador no se genera si no hay ninguna macro TEXTUAL-CONVENTION o la macro no contiene una cláusula DISPLAY-HINT.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se describe una convención textual SNMPv1.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

En este ejemplo se generan los siguientes calificadores CIM.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

En el ejemplo siguiente se describe una convención textual SNMPv2.

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

En este ejemplo se generan los siguientes calificadores CIM.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




