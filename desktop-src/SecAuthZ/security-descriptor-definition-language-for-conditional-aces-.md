---
description: Una entrada de control de acceso (ACE) condicional permite evaluar una condición de acceso cuando se realiza una comprobación de acceso. El lenguaje de definición de descriptores de seguridad (SDDL) proporciona la sintaxis para definir las ACE condicionales en un formato de cadena.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Lenguaje de definición de descriptores de seguridad para ACE condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542710"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Lenguaje de definición de descriptores de seguridad para ACE condicionales

Una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) condicional permite evaluar una condición de acceso cuando se realiza una comprobación de acceso. El lenguaje de definición de descriptores de seguridad (SDDL) proporciona la sintaxis para definir las ACE condicionales en un formato de cadena.

El SDDL de una ACE condicional es el mismo que para cualquier ACE, con la sintaxis de la instrucción condicional anexada al final de la cadena ACE. Para obtener información sobre SDDL, consulte [Security Descriptor Definition Language](security-descriptor-definition-language.md).

El \# signo "" es sinónimo de "0" en los atributos de recursos. Por ejemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) es equivalente a e interpretado como D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).

-   [Formato de cadena ACE condicional](#conditional-ace-string-format)
-   [Expresiones condicionales](#conditional-expressions)
-   [Atributos](#attributes)
-   [Operadores](#operators)
-   [Prioridad de los operadores](#operator-precedence)
-   [Valores desconocidos](#unknown-values)
-   [Evaluación de ACE condicional](#conditional-ace-evaluation)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato de cadena ACE condicional

Cada ACE de una cadena de [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) se incluye entre paréntesis. Los campos de la ACE están en el siguiente orden y se separan mediante signos de punto y coma (;).

*AceType ***;** _AceFlags_* _;_ *_Derechos_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Los campos se describen en [cadenas ACE](ace-strings.md), con las siguientes excepciones.

-   El campo *AceType* puede ser una de las siguientes cadenas.

    | Cadena de tipo ACE | Constante en SDDL. h                         | Valor AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | XA<br/> | acceso de devolución de llamada de SDDL \_ \_ \_ permitido<br/> | \_tipo de \_ ACE de devolución de llamada permitido de \_ acceso \_<br/> |
    | XD<br/> | \_ \_ acceso denegado de devolución de llamada SDDL \_<br/>  | tipo de ACE de devolución de llamada de acceso \_ denegado \_ \_ \_<br/>  |

    

     

-   La cadena ACE incluye una o más expresiones condicionales, entre paréntesis al final de la cadena.

## <a name="conditional-expressions"></a>Expresiones condicionales

Una expresión condicional puede incluir cualquiera de los siguientes elementos.



| Elemento de expresión                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Comprueba si el atributo especificado tiene un valor distinto de cero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **existe** *attributeName*<br/>                             | Comprueba si el atributo especificado existe en el contexto de cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valor* del *operador* *attributeName*<br/>                     | Devuelve el resultado de la operación especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * ConditionalExpression * **\|\|** _ConditionalExpression_<br/> | Comprueba si alguna de las expresiones condicionales especificadas es true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Comprueba si ambas expresiones condicionales especificadas son verdaderas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Inverso de una expresión condicional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Miembro \_ de {**_SidArray_*_}_*<br/>                         | Comprueba si el [**SID \_ y \_**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) la matriz de atributos del contexto del cliente contiene todos los [identificadores de seguridad](security-identifiers.md) (SID) de la lista separada por comas especificada por *SidArray*.<br/> En el caso de las ACE de permiso, un SID de contexto de cliente debe tener el atributo de **\_ grupo se \_ habilitado** establecido para que se considere una coincidencia.<br/> En el caso de las ACE de denegación, un SID de contexto de cliente debe tener el **\_ grupo se \_ habilitado** o el **\_ grupo se usa para el atributo \_ \_ \_ \_ solo denegar** establecido para que se considere una coincidencia.<br/> La matriz *SidArray* puede contener cadenas SID (por ejemplo, "S-1-5-6") o alias de SID (por ejemplo, "BA"<br/> |



 

## <a name="attributes"></a>Atributos

Un atributo representa un elemento de la matriz de información de atributos de seguridad de AUTHZ en el contexto del cliente. [**\_ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) Un nombre de atributo puede contener cualquier carácter alfanumérico y cualquiera de los caracteres ":", "/", "." y " \_ ".

Un valor de atributo puede ser cualquiera de los siguientes tipos.



| Tipo de valor         | Descripción                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entero<br/> | Entero de 64 bits en notación decimal o hexadecimal.<br/>                                                                                                                              |
| String<br/>  | Un valor de cadena delimitado por Comillas.<br/>                                                                                                                                                      |
| SID<br/>     | SID (S-1-1-0) o SID (BA). Debe estar en el RHS del miembro \_ del miembro o del dispositivo \_ \_ .<br/>                                                                                                           |
| BLOB<br/>    | \# seguido de números hexadecimales. Si la longitud de los números es impar, el \# se convierte en 0 para que sea par. También un \# que aparece en otro lugar del valor se convierte en 0.<br/> |



 

## <a name="operators"></a>Operadores

Los operadores siguientes se definen para su uso en expresiones condicionales para probar los valores de los atributos. Todos ellos son operadores binarios y se usan con el formato del *valor* del *operador* *attributeName* .



| Operator            | Descripción                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definición convencional.<br/>                                                                                      |
| !=<br/>       | Definición convencional.<br/>                                                                                      |
| <<br/>     | Definición convencional.<br/>                                                                                      |
| <=<br/>    | Definición convencional.<br/>                                                                                      |
| ><br/>     | Definición convencional.<br/>                                                                                      |
| >=<br/>    | Definición convencional.<br/>                                                                                      |
| Contiene<br/> | **True** si el valor del atributo especificado es un supraconjunto del valor especificado; en caso contrario, **false**.<br/>  |
| Cualquiera \_ de<br/>  | **True** si el valor especificado es un supraconjunto del valor del atributo especificado; en caso contrario, **false**. <br/> |



 

Además, los operadores unarios existen, Member \_ of y negaciones (!) se definen como se describe en la tabla de expresiones condicionales.

El operador "Contains" debe ir precedido y seguido por un espacio en blanco y el operador "any \_ of" debe ir precedido por un espacio en blanco.

## <a name="operator-precedence"></a>Prioridad de los operadores

Los operadores se evalúan en el orden de prioridad siguiente, con las operaciones de igual precedencia que se evalúan de izquierda a derecha.

1.  Exists, miembro \_ de
2.  Contains, cualquiera \_ de
3.  = =,! =, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Además, cualquier parte de una expresión condicional se puede incluir entre paréntesis. Primero se evalúan las expresiones entre paréntesis.

## <a name="unknown-values"></a>Valores desconocidos

Los resultados de las expresiones condicionales devuelven a veces un valor **desconocido**. Por ejemplo, cualquiera de las operaciones relacionales devuelven **Unknown** cuando el atributo especificado no existe.

En la tabla siguiente se describen los resultados de una operación **and** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2*.



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



 

En la tabla siguiente se describen los resultados de una operación **or** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2*.



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



 

También se **desconoce** la negación de una expresión condicional con un valor **desconocido** .

## <a name="conditional-ace-evaluation"></a>Evaluación de ACE condicional

En la tabla siguiente se describe el resultado de la comprobación de acceso de una ACE condicional en función de la evaluación final de la expresión condicional.

| Tipo de ACE         | TRUE             | false                 | DESCONOCIDO               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Omitir ACE<br/> | Omitir ACE<br/> |
| Denegar<br/>  | Denegar<br/>  | Omitir ACE<br/> | Denegar<br/>       |



 

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra cómo las directivas de acceso especificadas se representan mediante una ACE condicional definida mediante SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas
</dt> <dd>

Permitir la ejecución a todos los usuarios si se cumplen las dos condiciones siguientes:

-   Título = PM
-   Division = Finance o Division = sales

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "ventas")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas
</dt> <dd>

Permitir la ejecución si alguno de los proyectos de usuario es de intersección con los proyectos de archivo.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Project Cualquiera \_ de @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas
</dt> <dd>

Permitir acceso de lectura si el usuario ha iniciado sesión con una tarjeta inteligente, es un operador de copia de seguridad y se está conectando desde un equipo con BitLocker habilitado.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FR;;; S-1-1-0; (Miembro \_ de {SID (SID de tarjeta inteligente \_ ), SID (BO)}  && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

