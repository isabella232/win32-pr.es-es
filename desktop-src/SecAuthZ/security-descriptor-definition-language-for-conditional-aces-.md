---
description: Una entrada de control de acceso condicional (ACE) permite evaluar una condición de acceso cuando se realiza una comprobación de acceso. El lenguaje de definición de descriptores de seguridad (SDDL) proporciona sintaxis para definir las ACE condicionales en un formato de cadena.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Lenguaje de definición de descriptor de seguridad para AEE condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0a746460c7582d95e0c95e2a2c179aac2eb29456418234cb52e842c8c56738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780530"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Lenguaje de definición de descriptor de seguridad para AEE condicionales

Una entrada [*de control de acceso*](/windows/desktop/SecGloss/a-gly) condicional (ACE) permite evaluar una condición de acceso cuando se realiza una comprobación de acceso. El lenguaje de definición de descriptores de seguridad (SDDL) proporciona sintaxis para definir las ACE condicionales en un formato de cadena.

El SDDL de una ACE condicional es el mismo que para cualquier ACE, con la sintaxis de la instrucción condicional anexada al final de la cadena ACE. Para obtener información sobre SDDL, vea [Lenguaje de definición de descriptor de seguridad](security-descriptor-definition-language.md).

El signo \# " es sinónimo de "0" en los atributos de recursos. Por ejemplo, D:AI(XA;OICI;FA;;; WD;(OctetStringType== 1 2 3 )) es equivalente e \# \# interpretado como \# \# \# D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 01020300)).

-   [Formato de cadena ACE condicional](#conditional-ace-string-format)
-   [Expresiones condicionales](#conditional-expressions)
-   [Atributos](#attributes)
-   [Operadores](#operators)
-   [Prioridad de los operadores](#operator-precedence)
-   [Valores desconocidos](#unknown-values)
-   [Evaluación condicional de ACE](#conditional-ace-evaluation)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato de cadena ACE condicional

Cada ACE de una [*cadena de descriptor de*](/windows/desktop/SecGloss/s-gly) seguridad se incluye entre paréntesis. Los campos de la ACE están en el orden siguiente y están separados por punto y coma (;).

*AceType***;** _AceFlags_* _;_ *_Rights_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Los campos son como se describe en [Cadenas ACE](ace-strings.md), con las siguientes excepciones.

-   El *campo AceType* puede ser una de las cadenas siguientes.

    | Cadena de tipo ACE | Constante en Sddl.h                         | Valor AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | "XA"<br/> | SE PERMITE EL ACCESO \_ DE DEVOLUCIÓN DE \_ LLAMADA DE SDDL \_<br/> | TIPO \_ ACE DE \_ DEVOLUCIÓN DE LLAMADA CON ACCESO \_ \_ PERMITIDO<br/> |
    | "XD"<br/> | ACCESO DE DEVOLUCIÓN DE LLAMADA DE SDDL \_ \_ \_ DENEGADO<br/>  | TIPO \_ ACE DE \_ DEVOLUCIÓN DE LLAMADA DE DEVOLUCIÓN \_ DE LLAMADA DE ACCESO \_ DENEGADO<br/>  |

    

     

-   La cadena ACE incluye una o varias expresiones condicionales, entre paréntesis al final de la cadena.

## <a name="conditional-expressions"></a>Expresiones condicionales

Una expresión condicional puede incluir cualquiera de los siguientes elementos.



| Elemento de expresión                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Comprueba si el atributo especificado tiene un valor distinto de cero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **exists** *AttributeName*<br/>                             | Comprueba si el atributo especificado existe en el contexto de cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valor del* *operador* *AttributeName*<br/>                     | Devuelve el resultado de la operación especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *ConditionalExpression* **\|\|** _ConditionalExpression_<br/> | Comprueba si alguna de las expresiones condicionales especificadas es true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Comprueba si ambas expresiones condicionales especificadas son verdaderas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Inverso de una expresión condicional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Miembro \_ de{**_SidArray_*_}_*<br/>                         | Comprueba si la [**matriz SID \_ AND \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) del contexto de cliente contiene todos los identificadores de seguridad (SID) de la lista separada por comas especificada por *SidArray*. [](security-identifiers.md)<br/> Para Permitir ACE, un SID de contexto de cliente debe tener el atributo **\_ SE GROUP \_ ENABLED** establecido para que se considere una coincidencia.<br/> En el caso de las ACE de denegación, un SID de contexto de cliente debe tener el atributo **SE \_ GROUP \_ ENABLED** o **SE GROUP USE FOR DENY \_ \_ \_ \_ \_ ONLY** establecido para que se considere una coincidencia.<br/> La *matriz SidArray* puede contener cadenas SID (por ejemplo, "S-1-5-6") o alias SID (por ejemplo, "BA"<br/> |



 

## <a name="attributes"></a>Atributos

Un atributo representa un elemento de la [**matriz AUTHZ \_ SECURITY ATTRIBUTES \_ \_ INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) en el contexto de cliente. Un nombre de atributo puede contener cualquier carácter alfanumérico y cualquiera de los caracteres ":", "/", "." y \_ " ".

Un valor de atributo puede ser cualquiera de los tipos siguientes.



| Tipo de valor         | Descripción                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entero<br/> | Entero de 64 bits en notación decimal o hexadecimal.<br/>                                                                                                                              |
| String<br/>  | Valor de cadena delimitado por comillas.<br/>                                                                                                                                                      |
| SID<br/>     | SID(S-1-1-0) o SID(BA). Debe estar en RHS de miembro \_ de o miembro de dispositivo \_ \_ de.<br/>                                                                                                           |
| BLOB<br/>    | \# seguido de números hexadecimales. Si la longitud de los números es impar, se \# convierte en 0 para que sea uniforme. Además, \# un elemento que aparece en otra parte del valor se traduce en 0.<br/> |



 

## <a name="operators"></a>Operadores

Los operadores siguientes se definen para su uso en expresiones condicionales para probar los valores de los atributos. Todos ellos son operadores binarios y se usan con el formato *AttributeName* *Operator* *Value*.



| Operador            | Descripción                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definición convencional.<br/>                                                                                      |
| !=<br/>       | Definición convencional.<br/>                                                                                      |
| <<br/>     | Definición convencional.<br/>                                                                                      |
| <=<br/>    | Definición convencional.<br/>                                                                                      |
| ><br/>     | Definición convencional.<br/>                                                                                      |
| >=<br/>    | Definición convencional.<br/>                                                                                      |
| Contiene<br/> | **TRUE** si el valor del atributo especificado es un superconjunto del valor especificado; de lo contrario, **FALSE**.<br/>  |
| Cualquiera \_ de<br/>  | **TRUE** si el valor especificado es un superconjunto del valor del atributo especificado; de lo contrario, **FALSE**. <br/> |



 

Además, los operadores unarios Exists, Member of y negation (!) se definen como se \_ describe en la tabla Expresiones condicionales.

El operador "Contains" debe ir precedido y seguido de un espacio en blanco, y el operador "Cualquiera de" debe \_ ir precedido de un espacio en blanco.

## <a name="operator-precedence"></a>Prioridad de los operadores

Los operadores se evalúan en el orden de precedencia siguiente, con operaciones de igual prioridad que se evalúan de izquierda a derecha.

1.  Existe, miembro \_ de
2.  Contains, Any \_ of
3.  ==, !=, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Además, cualquier parte de una expresión condicional se puede incluir entre paréntesis. Las expresiones entre paréntesis se evalúan primero.

## <a name="unknown-values"></a>Valores desconocidos

Los resultados de las expresiones condicionales a veces devuelven un valor de **Unknown**. Por ejemplo, cualquiera de las operaciones relacionales devuelve **Unknown** cuando el atributo especificado no existe.

En la tabla siguiente se describen los resultados de una operación **AND** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&** *ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

En la tabla siguiente se describen los resultados de una operación **OR** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

La negación de una expresión condicional con un valor **de UNKNOWN** también es **UNKNOWN.**

## <a name="conditional-ace-evaluation"></a>Evaluación condicional de ACE

En la tabla siguiente se describe el resultado de la comprobación de acceso de una ACE condicional en función de la evaluación final de la expresión condicional.

| Tipo ace         | TRUE             | FALSE                 | DESCONOCIDO               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Omitir ACE<br/> | Omitir ACE<br/> |
| Denegar<br/>  | Denegar<br/>  | Omitir ACE<br/> | Denegar<br/>       |



 

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra cómo las directivas de acceso especificadas se representan mediante una ACE condicional definida mediante SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permitir ejecutar a todos si se cumplen las dos condiciones siguientes:

-   Título = PM
-   División = Finanzas o División = Ventas

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Title =="PM" && ( @User.Division =="Finance" \| \| @User.Division ==" Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permitir ejecución si alguno de los proyectos del usuario forma intersección con los proyectos del archivo.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Project Cualquiera \_ de @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permitir el acceso de lectura si el usuario ha iniciado sesión con una tarjeta inteligente, es un operador de copia de seguridad y se conecta desde una máquina con Bitlocker habilitado.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ;FR;;; S-1-1-0; (Miembro \_ de {SID(SID de \_ tarjeta inteligente), SID(BO)} && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\[MS-DTYP: \] lenguaje de descripción del descriptor de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

