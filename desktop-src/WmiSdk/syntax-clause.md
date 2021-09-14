---
description: Contiene una cláusula SYNTAX que define los datos y el tipo del objeto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: CLÁUSULA SYNTAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973711"
---
# <a name="syntax-clause"></a>CLÁUSULA SYNTAX

La [macro OBJECT-TYPE](object-type-macro.md) contiene una cláusula SYNTAX que define los datos y el tipo del objeto MIB. Aunque el proveedor SNMP observa reglas generales para asignar cláusulas SYNTAX, el proveedor también sigue reglas específicas de varios tipos de datos.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Las siguientes reglas de asignación se aplican a todos los tipos de datos descritos en la tabla siguiente:

-   La representación textual de la cláusula SYNTAX se asigna a la convención textual del calificador de **propiedad CIM \_**.
-   La definición de tipo con nombre de la cláusula SYNTAX se asigna a la sintaxis del objeto de **calificador de \_ propiedad CIM**. Esta asignación difiere en función del tipo de datos. Para obtener más información, vea las descripciones de la asignación.
-   El tipo SNMP usado al codificar marcos de protocolo SNMPv1 y SNMPv2C se asigna a la codificación del calificador de **propiedad CIM**.
-   El calificador de propiedad **CIM cimtype** contiene la representación textual que da formato al valor del protocolo CIM subyacente.

En la tabla siguiente se enumeran los tipos de datos que tienen reglas específicas que rigen el comportamiento de asignación del proveedor.



| Tipo de datos SNMP                                     | Descripción                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo primitivo](#primitive-type)                  | Uno de los tipos de datos básicos definidos en los documentos de estructura de información de administración (SMI) RFC 1213 y RFC 1903.                                                                                                                            |
| [Convención textual](textual-convention-macro.md) | Definición de tipo generada mediante el uso explícito de la macro **TEXTUAL-CONVENTION** de SNMPv2C o generada mediante el uso de un tipo con nombre. Una convención textual asigna un nombre y, en algunos casos, un intervalo de valores a un tipo de datos existente. |
| [Tipo con nombre](#named-type)                          | Referencia con nombre a un tipo primitivo, convención textual o tipo restringido.                                                                                                                                                                    |
| [Tipo restringido](#constrained-type)              | Tipo primitivo, tipo con nombre o convención textual que se ha restringido mediante algún mecanismo de subtipado definido en los documentos SMI RFC 1213 y RFC 1903.                                                                                      |



 

## <a name="primitive-type"></a>Tipo primitivo

El tipo primitivo es uno de los tipos de datos básicos definidos en los documentos de estructura de información de administración (SMI) RFC 1213 y RFC 1903. Los tipos primitivos snmp se asignan a tipos definidos por CIM. En la tabla siguiente se muestra la asignación que se produce cuando la cláusula SYNTAX hace referencia explícitamente a un tipo primitivo para SNMPv1. La convención textual , **la codificación** y **\_ los** calificadores de sintaxis de objeto siempre son iguales que el tipo MIB y el valor predeterminado siempre es **NULL.** **\_**



| Tipo de MIB         | Tipo de variante CIM | valor cimtype |
|------------------|------------------|---------------|
| INTEGER          | VT \_ I4           | **sint32**    |
| OCTETSTRING      | VT \_ BSTR         | **string**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **string**    |
| NULL             | VT \_ NULL         | No compatible |
| IpAddress        | VT \_ BSTR         | **string**    |
| Contador          | VT \_ I4           | **uint32**    |
| Medidor            | VT \_ I4           | **uint32**    |
| TimeTicks        | VT \_ I4           | **uint32**    |
| Opaca           | VT \_ BSTR         | **string**    |
| NetworkAddress   | VT \_ BSTR         | **string**    |



 

El proveedor omite la macro OBJECT-TYPE cuando la cláusula SYNTAX hace referencia a **NULL,** ya sea explícitamente o a través de una asignación de tipo con nombre. En la tabla siguiente se muestra la asignación que se produce cuando la cláusula SYNTAX hace referencia explícitamente a un tipo primitivo para SNMPv2. La convención textual , **la codificación** y **\_ los** calificadores de sintaxis de objeto siempre son iguales que el tipo MIB y el valor predeterminado siempre es **NULL.** **\_**



| Tipo de MIB          | Tipo de variante CIM | valor cimtype |
|-------------------|------------------|---------------|
| INTEGER           | VT \_ I4           | **sint32**    |
| OCTET STRING      | VT \_ BSTR         | **string**    |
| IDENTIFICADOR DE OBJETO | VT \_ BSTR         | **string**    |
| IpAddress         | VT \_ BSTR         | **string**    |
| Contador32         | VT \_ I4           | **uint32**    |
| Medidor32           | VT \_ I4           | **uint32**    |
| Unsigned32        | VT \_ I4           | **uint32**    |
| Integer32         | VT \_ I4           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| TimeTicks         | VT \_ I4           | **uint32**    |
| Opaca            | VT \_ BSTR         | **string**    |



 

## <a name="named-type"></a>Tipo con nombre

Los tipos con nombre SNMP se asignan a tipos definidos por CIM. Cuando la cláusula SYNTAX hace referencia [a](#primitive-type) [](#constrained-type) un tipo primitivo , convención [textual](textual-convention-macro.md)o tipo restringido a través de una derivación de asignación de tipos, use esos tipos para determinar qué procedimientos de asignación se aplican.

-   Si, mediante la derivación de las reglas de asignación de tipos, se encuentra una definición de tipo restringida:

    -   Y si, a través de una derivación adicional, encuentra una de las convenciones textuales enumeradas en [la macro TEXTUAL-CONVENTION](textual-convention-macro.md), aplique las reglas de asignación para tipos restringidos y convenciones textuales.
    -   De lo contrario, si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipos primitivos, aplique las reglas de asignación para los tipos primitivos y los tipos restringidos.

-   Si encuentra una de las convenciones de texto enumeradas en [la macro TEXTUAL CONVENTION \_ ,](textual-convention-macro.md)aplique las reglas de asignación para las convenciones textuales.
-   Si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipos primitivos, aplique las reglas de asignación para los tipos primitivos.

> [!Note]  
> Las clases que contienen tipos de propiedad que no se ajustan a la asignación descrita anteriormente no son válidas. En este caso, el proveedor devuelve un error si el proveedor solicita la recuperación de una definición de clase mientras ejecuta una función de recuperación de instancia.

 

## <a name="constrained-type"></a>Tipo restringido

Un tipo restringido es un tipo primitivo, un tipo con nombre o una convención textual que se ha restringido mediante algún mecanismo de subtipado definido en los documentos SMI RFC 1213 y RFC 1903. Cuando se produce la subtipo, se requieren calificadores CIM adicionales para especificar los valores de subtipo. La definición de tipo con nombre de la cláusula **\_** SYNTAX asigna textualmente a la sintaxis del objeto calificador de propiedad CIM hasta , pero sin incluir las restricciones del subtipo.

Los subtipos pueden seguir cualquiera de los formatos siguientes:

-   ENTERO enumerado

    La enumeración de **calificador de propiedad** CIM especifica los valores enumerados. Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits con signo. En la tabla siguiente se enumeran los tipos de asignación. El valor predeterminado es siempre **NULL.**



| Tipo de MIB restringido | Tipo de variante CIM | Calificadores CIM                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| ENTERO enumerado   | VT \_ BSTR         | **convención \_ textual:** enumeratedinteger<br/> **encoding:** INTEGER<br/> **cimtype**: string<br/> |



 

-   BITS

    Los bits del **calificador** de propiedad CIM especifican los valores enumerados. Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits con signo. En la tabla siguiente se enumeran los tipos de asignación. El valor predeterminado es siempre **NULL.**



| Tipo de MIB restringido | Tipo de variante CIM      | Calificadores CIM                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | VT \_ ARRAY \| VT \_ BSTR | **convención \_ textual:** bits<br/> **encoding:** OCTETSTRING<br/> **cimtype**: string<br/> |



 

-   Longitud variable

    Cuando la cláusula SYNTAX hace referencia a un tipo primitivo, un tipo con nombre o una convención textual **\_** que se subtipo como UNA CADENA DE OCTETO de longitud variable o Opaca, la longitud variable del calificador de propiedad CIM especifica los valores mínimo, máximo y de longitud fija asociados a la definición de tipo. Este calificador se implementa como una cadena en el formato siguiente, donde los valores de longitud variable se representan como enteros de 32 bits sin signo.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Longitud fija

    Cuando la cláusula SYNTAX hace referencia a un tipo primitivo, un tipo con nombre o una convención textual **\_** que se subtipo como UNA CADENA DE OCTETO de longitud fija o Opaca, el calificador de propiedad CIM de longitud fija especifica el valor de longitud fija. Este calificador se representa como un valor entero de 32 bits sin signo.

-   Intervalo

    Cuando la cláusula SYNTAX hace referencia a un tipo primitivo, un tipo con nombre o una convención textual que está subtipo como un valor entero o un medidor de valor fijo o de rango, el valor de **variable \_** calificador de propiedad CIM especifica los valores fijos y de rango asociados a la definición de tipo. Este calificador se implementa como una cadena en el formato siguiente, donde los valores de intervalo y longitud fija se representan como enteros de 32 bits sin signo.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se describe un subtipo INTEGER enumerado.

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

Este ejemplo se asigna a:

``` syntax
enumeration("up(1),down(2),testing(3)")
```

En el ejemplo de código siguiente se describe un subtipo BITS.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

El ejemplo de código siguiente se asigna a:

``` syntax
bits("up(1),down(2),testing(3)")
```

En el ejemplo de código siguiente se describe un subtipo de longitud variable.

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

Este ejemplo se asigna a:

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

En el ejemplo siguiente se describe un subtipo de longitud fija.

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

Este ejemplo se asigna a:

``` syntax
fixed_length(6)
```

En el ejemplo siguiente se describe un subtipo de intervalo.

``` syntax
Status := INTEGER (10..20|8)
```

Este ejemplo se asigna a:

``` syntax
variable_value("10..20,8")
```

 

 




