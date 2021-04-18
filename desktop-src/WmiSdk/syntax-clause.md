---
description: Contiene una cláusula de sintaxis que define los datos y el tipo para el objeto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Cláusula de sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707346"
---
# <a name="syntax-clause"></a>Cláusula de sintaxis

La macro [Object-Type](object-type-macro.md) contiene una cláusula de sintaxis que define los datos y el tipo para el objeto MIB. Aunque el proveedor SNMP observa reglas generales para asignar cláusulas de sintaxis, el proveedor también sigue las reglas específicas de varios tipos de datos.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Las siguientes reglas de asignación se aplican a todos los tipos de datos descritos en la tabla siguiente:

-   La representación textual de la cláusula de sintaxis se asigna a la **\_ Convención textual** de la propiedad CIM.
-   La definición de tipo con nombre de la cláusula de sintaxis se asigna a **la \_ Sintaxis de objeto** de calificador de propiedad CIM. Esta asignación difiere en función del tipo de datos. Para obtener más información, vea las descripciones de la asignación.
-   El tipo de SNMP que se usa al codificar los marcos del protocolo SNMPv1 y SNMPv2C se asigna a la **codificación** del calificador de la propiedad CIM.
-   El calificador de propiedad de CIM **CIMTYPE** contiene la representación textual que da formato al valor del protocolo CIM subyacente.

En la tabla siguiente se enumeran los tipos de datos que tienen reglas específicas que rigen el comportamiento de la asignación de proveedores.



| Tipo de datos SNMP                                     | Descripción                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo primitivo](#primitive-type)                  | Uno de los tipos de datos básicos definidos en la estructura de documentos de información de administración (SMI) RFC 1213 y RFC 1903.                                                                                                                            |
| [Convención textual](textual-convention-macro.md) | Definición de tipo generada mediante el uso explícito de la macro de **Convención de texto** SNMPv2c o generada mediante el uso de un tipo con nombre. Una Convención textual asigna un nombre y, en algunos casos, un intervalo de valores a un tipo de datos existente. |
| [Tipo con nombre](#named-type)                          | Referencia con nombre a un tipo primitivo, una Convención textual o un tipo restringido.                                                                                                                                                                    |
| [Tipo restringido](#constrained-type)              | Tipo primitivo, tipo con nombre o Convención textual que se ha restringido mediante algún mecanismo de subescritura definido en los documentos de SMI RFC 1213 y RFC 1903.                                                                                      |



 

## <a name="primitive-type"></a>Tipo primitivo

El tipo primitivo es uno de los tipos de datos básicos definidos en la estructura de documentos de información de administración (SMI) RFC 1213 y RFC 1903. Los tipos primitivos SNMP se asignan a los tipos definidos por CIM. En la tabla siguiente se muestra la asignación que se produce cuando la cláusula de sintaxis hace referencia explícitamente a un tipo primitivo para SNMPv1. Los calificadores de sintaxis de **texto \_**, **codificación** y **\_ Sintaxis de objetos** siempre son los mismos que el tipo de MIB y el valor predeterminado es siempre **null**.



| Tipo de MIB         | Tipo de variante CIM | valor de CIMTYPE |
|------------------|------------------|---------------|
| INTEGER          | VT \_ I4           | **sint32**    |
| OCTETSTRING      | VT \_ BSTR         | **string**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **string**    |
| NULL             | VT \_ null         | No compatible |
| IpAddress        | VT \_ BSTR         | **string**    |
| Contador          | VT \_ I4           | **uint32**    |
| Indicador            | VT \_ I4           | **uint32**    |
| TimeTicks        | VT \_ I4           | **uint32**    |
| Opaca           | VT \_ BSTR         | **string**    |
| NetworkAddress   | VT \_ BSTR         | **string**    |



 

El proveedor omite la macro OBJECT-TYPE cuando la cláusula de sintaxis hace referencia a **null**, ya sea explícitamente o a través de una asignación de tipo con nombre. En la tabla siguiente se muestra la asignación que se produce cuando la cláusula de sintaxis hace referencia de forma explícita a un tipo primitivo para SNMPv2. Los calificadores de sintaxis de **texto \_**, **codificación** y **\_ Sintaxis de objetos** siempre son los mismos que el tipo de MIB y el valor predeterminado es siempre **null**.



| Tipo de MIB          | Tipo de variante CIM | valor de CIMTYPE |
|-------------------|------------------|---------------|
| INTEGER           | VT \_ I4           | **sint32**    |
| CADENA DE OCTETO      | VT \_ BSTR         | **string**    |
| IDENTIFICADOR DE OBJETO | VT \_ BSTR         | **string**    |
| IpAddress         | VT \_ BSTR         | **string**    |
| Counter32         | VT \_ I4           | **uint32**    |
| Gauge32           | VT \_ I4           | **uint32**    |
| Unsigned32        | VT \_ I4           | **uint32**    |
| Integer32         | VT \_ I4           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| TimeTicks         | VT \_ I4           | **uint32**    |
| Opaca            | VT \_ BSTR         | **string**    |



 

## <a name="named-type"></a>Tipo con nombre

Los tipos con nombre SNMP se asignan a los tipos definidos por CIM. Cuando la cláusula de sintaxis hace referencia a un [tipo primitivo](#primitive-type), una [Convención textual](textual-convention-macro.md)o un [tipo restringido](#constrained-type) a través de una derivación de asignación de tipo, use esos tipos para determinar qué procedimientos de asignación se aplican.

-   Si, mediante la derivación de las reglas de asignación de tipos, encuentra una definición de Tipo restringida:

    -   Y si, a través de la derivación adicional, se encuentra con una de las convenciones de texto enumeradas en [la macro de Convención de texto](textual-convention-macro.md), aplique las reglas de asignación para los tipos y las convenciones de texto restringidos.
    -   De lo contrario, si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipo primitivo, aplique las reglas de asignación para los tipos primitivos y los tipos restringidos.

-   Si encuentra una de las convenciones de texto enumeradas [en \_ macro de Convención textual](textual-convention-macro.md), aplique las reglas de asignación para las convenciones textuales.
-   Si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipo primitivo, aplique las reglas de asignación para los tipos primitivos.

> [!Note]  
> Las clases que contienen tipos de propiedad que no se ajustan a la asignación descrita anteriormente no son válidas. En este caso, el proveedor devuelve un error si y cuando el proveedor solicita la recuperación de una definición de clase al ejecutar una función de recuperación de instancia.

 

## <a name="constrained-type"></a>Tipo restringido

Un tipo restringido es un tipo primitivo, un tipo con nombre o una Convención textual que se ha restringido mediante algún mecanismo de subescritura definido en los documentos SMI RFC 1213 y RFC 1903. Cuando se producen subtipos, se necesitan calificadores CIM adicionales para especificar los valores de subtipo. La definición de tipo con nombre de la cláusula de sintaxis se asigna literalmente a la **\_ Sintaxis de objeto** de calificador de propiedad CIM hasta, pero sin incluir las restricciones del subtipo.

Los subtipos pueden seguir cualquiera de los siguientes formatos:

-   ENTERO enumerado

    La **enumeración** de calificador de propiedad CIM especifica los valores enumerados. Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits firmados. En la tabla siguiente se enumeran los tipos de asignación. El valor predeterminado es siempre **null**.



| Tipo de MIB restringido | Tipo de variante CIM | Calificadores CIM                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| ENTERO enumerado   | VT \_ BSTR         | **\_ Convención textual**: enumeratedinteger<br/> **codificación**: entero<br/> **CIMTYPE**: cadena<br/> |



 

-   BITS

    Los **bits** del calificador de la propiedad CIM especifican los valores enumerados. Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits firmados. En la tabla siguiente se enumeran los tipos de asignación. El valor predeterminado es siempre **null**.



| Tipo de MIB restringido | Tipo de variante CIM      | Calificadores CIM                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | \_matriz VT \| VT \_ BSTR | **\_ Convención textual**: bits<br/> **codificación**: OCTETSTRING<br/> **CIMTYPE**: cadena<br/> |



 

-   Longitud variable

    Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como una cadena de octeto de longitud variable u opaca, **la \_ longitud variable** del calificador de propiedad CIM especifica los valores mínimo, máximo y de longitud fija asociados con la definición de tipo. Este calificador se implementa como una cadena en el formato siguiente, donde los valores de longitud variable se representan como enteros de 32 bits sin signo.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Longitud fija

    Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como una cadena de octeto de longitud fija o opaca, **la \_ longitud fija** del calificador de propiedad CIM especifica el valor de longitud fija. Este calificador se representa como un valor entero de 32 bits sin signo.

-   Intervalo

    Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como un indicador o un entero de valor fijo o de intervalo, el **\_ valor** de la variable de calificador de propiedad CIM especifica los valores de intervalo y fijos asociados a la definición de tipo. Este calificador se implementa como una cadena en el formato siguiente, donde los valores de intervalo y de longitud fija se representan como enteros de 32 bits sin signo.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Código de ejemplo

En el siguiente ejemplo se describe un subtipo de entero enumerado.

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

En el ejemplo de código siguiente se describe un subtipo de BITS.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

El siguiente ejemplo de código se asigna a:

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

En el siguiente ejemplo se describe un subtipo de intervalo.

``` syntax
Status := INTEGER (10..20|8)
```

Este ejemplo se asigna a:

``` syntax
variable_value("10..20,8")
```

 

 




