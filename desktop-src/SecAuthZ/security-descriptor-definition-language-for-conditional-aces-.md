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
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="3eeb9-104">Lenguaje de definición de descriptores de seguridad para ACE condicionales</span><span class="sxs-lookup"><span data-stu-id="3eeb9-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="3eeb9-105">Una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) condicional permite evaluar una condición de acceso cuando se realiza una comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="3eeb9-106">El lenguaje de definición de descriptores de seguridad (SDDL) proporciona la sintaxis para definir las ACE condicionales en un formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="3eeb9-107">El SDDL de una ACE condicional es el mismo que para cualquier ACE, con la sintaxis de la instrucción condicional anexada al final de la cadena ACE.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="3eeb9-108">Para obtener información sobre SDDL, consulte [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="3eeb9-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="3eeb9-109">El \# signo "" es sinónimo de "0" en los atributos de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="3eeb9-110">Por ejemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) es equivalente a e interpretado como D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="3eeb9-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="3eeb9-111">Formato de cadena ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3eeb9-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="3eeb9-112">Expresiones condicionales</span><span class="sxs-lookup"><span data-stu-id="3eeb9-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="3eeb9-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="3eeb9-114">Operadores</span><span class="sxs-lookup"><span data-stu-id="3eeb9-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="3eeb9-115">Prioridad de los operadores</span><span class="sxs-lookup"><span data-stu-id="3eeb9-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="3eeb9-116">Valores desconocidos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="3eeb9-117">Evaluación de ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3eeb9-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="3eeb9-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="3eeb9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3eeb9-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="3eeb9-120">Formato de cadena ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3eeb9-120">Conditional ACE String Format</span></span>

<span data-ttu-id="3eeb9-121">Cada ACE de una cadena de [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) se incluye entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="3eeb9-122">Los campos de la ACE están en el siguiente orden y se separan mediante signos de punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="3eeb9-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="3eeb9-123">*AceType ***;** _AceFlags_* _;_ *_Derechos_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="3eeb9-124">Los campos se describen en [cadenas ACE](ace-strings.md), con las siguientes excepciones.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="3eeb9-125">El campo *AceType* puede ser una de las siguientes cadenas.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="3eeb9-126">Cadena de tipo ACE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-126">ACE type string</span></span> | <span data-ttu-id="3eeb9-127">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="3eeb9-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="3eeb9-128">Valor AceType</span><span class="sxs-lookup"><span data-stu-id="3eeb9-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="3eeb9-129">XA</span><span class="sxs-lookup"><span data-stu-id="3eeb9-129">"XA"</span></span><br/> | <span data-ttu-id="3eeb9-130">acceso de devolución de llamada de SDDL \_ \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="3eeb9-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="3eeb9-131">\_tipo de \_ ACE de devolución de llamada permitido de \_ acceso \_</span><span class="sxs-lookup"><span data-stu-id="3eeb9-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="3eeb9-132">XD</span><span class="sxs-lookup"><span data-stu-id="3eeb9-132">"XD"</span></span><br/> | <span data-ttu-id="3eeb9-133">\_ \_ acceso denegado de devolución de llamada SDDL \_</span><span class="sxs-lookup"><span data-stu-id="3eeb9-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="3eeb9-134">tipo de ACE de devolución de llamada de acceso \_ denegado \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3eeb9-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="3eeb9-135">La cadena ACE incluye una o más expresiones condicionales, entre paréntesis al final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="3eeb9-136">Expresiones condicionales</span><span class="sxs-lookup"><span data-stu-id="3eeb9-136">Conditional Expressions</span></span>

<span data-ttu-id="3eeb9-137">Una expresión condicional puede incluir cualquiera de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="3eeb9-138">Elemento de expresión</span><span class="sxs-lookup"><span data-stu-id="3eeb9-138">Expression element</span></span>                                                | <span data-ttu-id="3eeb9-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eeb9-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eeb9-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="3eeb9-141">Comprueba si el atributo especificado tiene un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3eeb9-142">**existe** *attributeName*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="3eeb9-143">Comprueba si el atributo especificado existe en el contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3eeb9-144">*Valor* del *operador* *attributeName*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="3eeb9-145">Devuelve el resultado de la operación especificada.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3eeb9-146">\* ConditionalExpression \* **\|\|** _ConditionalExpression_</span><span class="sxs-lookup"><span data-stu-id="3eeb9-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="3eeb9-147">Comprueba si alguna de las expresiones condicionales especificadas es true.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3eeb9-148">*ConditionalExpression* **&&** *ConditionalExpression*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="3eeb9-149">Comprueba si ambas expresiones condicionales especificadas son verdaderas.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3eeb9-150">**! (**_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="3eeb9-151">Inverso de una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3eeb9-152">**Miembro \_ de {**_SidArray_*_}_*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="3eeb9-153">Comprueba si el [**SID \_ y \_**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) la matriz de atributos del contexto del cliente contiene todos los [identificadores de seguridad](security-identifiers.md) (SID) de la lista separada por comas especificada por *SidArray*.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="3eeb9-154">En el caso de las ACE de permiso, un SID de contexto de cliente debe tener el atributo de **\_ grupo se \_ habilitado** establecido para que se considere una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="3eeb9-155">En el caso de las ACE de denegación, un SID de contexto de cliente debe tener el **\_ grupo se \_ habilitado** o el **\_ grupo se usa para el atributo \_ \_ \_ \_ solo denegar** establecido para que se considere una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="3eeb9-156">La matriz *SidArray* puede contener cadenas SID (por ejemplo, "S-1-5-6") o alias de SID (por ejemplo, "BA"</span><span class="sxs-lookup"><span data-stu-id="3eeb9-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="3eeb9-157">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-157">Attributes</span></span>

<span data-ttu-id="3eeb9-158">Un atributo representa un elemento de la matriz de información de atributos de seguridad de AUTHZ en el contexto del cliente. [**\_ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information)</span><span class="sxs-lookup"><span data-stu-id="3eeb9-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="3eeb9-159">Un nombre de atributo puede contener cualquier carácter alfanumérico y cualquiera de los caracteres ":", "/", "." y " \_ ".</span><span class="sxs-lookup"><span data-stu-id="3eeb9-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="3eeb9-160">Un valor de atributo puede ser cualquiera de los siguientes tipos.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="3eeb9-161">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="3eeb9-161">Value type</span></span>         | <span data-ttu-id="3eeb9-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eeb9-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eeb9-163">Entero</span><span class="sxs-lookup"><span data-stu-id="3eeb9-163">Integer</span></span><br/> | <span data-ttu-id="3eeb9-164">Entero de 64 bits en notación decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3eeb9-165">String</span><span class="sxs-lookup"><span data-stu-id="3eeb9-165">String</span></span><br/>  | <span data-ttu-id="3eeb9-166">Un valor de cadena delimitado por Comillas.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="3eeb9-167">SID</span><span class="sxs-lookup"><span data-stu-id="3eeb9-167">SID</span></span><br/>     | <span data-ttu-id="3eeb9-168">SID (S-1-1-0) o SID (BA).</span><span class="sxs-lookup"><span data-stu-id="3eeb9-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="3eeb9-169">Debe estar en el RHS del miembro \_ del miembro o del dispositivo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3eeb9-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="3eeb9-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="3eeb9-170">BLOB</span></span><br/>    | <span data-ttu-id="3eeb9-171">\# seguido de números hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="3eeb9-172">Si la longitud de los números es impar, el \# se convierte en 0 para que sea par.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="3eeb9-173">También un \# que aparece en otro lugar del valor se convierte en 0.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="3eeb9-174">Operadores</span><span class="sxs-lookup"><span data-stu-id="3eeb9-174">Operators</span></span>

<span data-ttu-id="3eeb9-175">Los operadores siguientes se definen para su uso en expresiones condicionales para probar los valores de los atributos.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="3eeb9-176">Todos ellos son operadores binarios y se usan con el formato del *valor* del *operador* *attributeName* .</span><span class="sxs-lookup"><span data-stu-id="3eeb9-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="3eeb9-177">Operator</span><span class="sxs-lookup"><span data-stu-id="3eeb9-177">Operator</span></span>            | <span data-ttu-id="3eeb9-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eeb9-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="3eeb9-179">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="3eeb9-180">!=</span><span class="sxs-lookup"><span data-stu-id="3eeb9-180">!=</span></span><br/>       | <span data-ttu-id="3eeb9-181">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="3eeb9-182">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="3eeb9-183">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="3eeb9-184">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="3eeb9-185">Definición convencional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="3eeb9-186">Contiene</span><span class="sxs-lookup"><span data-stu-id="3eeb9-186">Contains</span></span><br/> | <span data-ttu-id="3eeb9-187">**True** si el valor del atributo especificado es un supraconjunto del valor especificado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="3eeb9-188">Cualquiera \_ de</span><span class="sxs-lookup"><span data-stu-id="3eeb9-188">Any\_of</span></span><br/>  | <span data-ttu-id="3eeb9-189">**True** si el valor especificado es un supraconjunto del valor del atributo especificado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="3eeb9-190">Además, los operadores unarios existen, Member \_ of y negaciones (!) se definen como se describe en la tabla de expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="3eeb9-191">El operador "Contains" debe ir precedido y seguido por un espacio en blanco y el operador "any \_ of" debe ir precedido por un espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="3eeb9-192">Prioridad de los operadores</span><span class="sxs-lookup"><span data-stu-id="3eeb9-192">Operator Precedence</span></span>

<span data-ttu-id="3eeb9-193">Los operadores se evalúan en el orden de prioridad siguiente, con las operaciones de igual precedencia que se evalúan de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="3eeb9-194">Exists, miembro \_ de</span><span class="sxs-lookup"><span data-stu-id="3eeb9-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="3eeb9-195">Contains, cualquiera \_ de</span><span class="sxs-lookup"><span data-stu-id="3eeb9-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="3eeb9-196">= =,! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="3eeb9-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="3eeb9-197">!</span><span class="sxs-lookup"><span data-stu-id="3eeb9-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="3eeb9-198">Además, cualquier parte de una expresión condicional se puede incluir entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="3eeb9-199">Primero se evalúan las expresiones entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="3eeb9-200">Valores desconocidos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-200">Unknown Values</span></span>

<span data-ttu-id="3eeb9-201">Los resultados de las expresiones condicionales devuelven a veces un valor **desconocido**.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="3eeb9-202">Por ejemplo, cualquiera de las operaciones relacionales devuelven **Unknown** cuando el atributo especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="3eeb9-203">En la tabla siguiente se describen los resultados de una operación **and** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="3eeb9-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="3eeb9-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="3eeb9-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="3eeb9-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-207">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-208">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="3eeb9-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-210">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-211">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-213">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="3eeb9-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-216">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-217">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-219">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-220">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-222">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-226">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="3eeb9-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-229">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="3eeb9-234">En la tabla siguiente se describen los resultados de una operación **or** lógica entre dos expresiones condicionales, *ConditionalExpression1* y *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="3eeb9-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="3eeb9-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="3eeb9-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="3eeb9-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3eeb9-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="3eeb9-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-239">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-240">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3eeb9-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-242">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-243">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3eeb9-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-245">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3eeb9-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-248">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-249">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3eeb9-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-251">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-252">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="3eeb9-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-254">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-258">**TRUE**</span></span><br/>      | <span data-ttu-id="3eeb9-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3eeb9-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-261">**FALSE**</span></span><br/>     | <span data-ttu-id="3eeb9-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="3eeb9-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3eeb9-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3eeb9-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="3eeb9-266">También se **desconoce** la negación de una expresión condicional con un valor **desconocido** .</span><span class="sxs-lookup"><span data-stu-id="3eeb9-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="3eeb9-267">Evaluación de ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3eeb9-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="3eeb9-268">En la tabla siguiente se describe el resultado de la comprobación de acceso de una ACE condicional en función de la evaluación final de la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="3eeb9-269">Tipo de ACE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-269">ACE type</span></span>         | <span data-ttu-id="3eeb9-270">TRUE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-270">TRUE</span></span>             | <span data-ttu-id="3eeb9-271">false</span><span class="sxs-lookup"><span data-stu-id="3eeb9-271">FALSE</span></span>                 | <span data-ttu-id="3eeb9-272">DESCONOCIDO</span><span class="sxs-lookup"><span data-stu-id="3eeb9-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="3eeb9-273">Allow</span><span class="sxs-lookup"><span data-stu-id="3eeb9-273">Allow</span></span><br/> | <span data-ttu-id="3eeb9-274">Allow</span><span class="sxs-lookup"><span data-stu-id="3eeb9-274">Allow</span></span><br/> | <span data-ttu-id="3eeb9-275">Omitir ACE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-275">Ignore ACE</span></span><br/> | <span data-ttu-id="3eeb9-276">Omitir ACE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="3eeb9-277">Denegar</span><span class="sxs-lookup"><span data-stu-id="3eeb9-277">Deny</span></span><br/>  | <span data-ttu-id="3eeb9-278">Denegar</span><span class="sxs-lookup"><span data-stu-id="3eeb9-278">Deny</span></span><br/>  | <span data-ttu-id="3eeb9-279">Omitir ACE</span><span class="sxs-lookup"><span data-stu-id="3eeb9-279">Ignore ACE</span></span><br/> | <span data-ttu-id="3eeb9-280">Denegar</span><span class="sxs-lookup"><span data-stu-id="3eeb9-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="3eeb9-281">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3eeb9-281">Examples</span></span>

<span data-ttu-id="3eeb9-282">En los siguientes ejemplos se muestra cómo las directivas de acceso especificadas se representan mediante una ACE condicional definida mediante SDDL.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="3eeb9-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas</span><span class="sxs-lookup"><span data-stu-id="3eeb9-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-284">Permitir la ejecución a todos los usuarios si se cumplen las dos condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="3eeb9-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="3eeb9-285">Título = PM</span><span class="sxs-lookup"><span data-stu-id="3eeb9-285">Title = PM</span></span>
-   <span data-ttu-id="3eeb9-286">Division = Finance o Division = sales</span><span class="sxs-lookup"><span data-stu-id="3eeb9-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="3eeb9-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3eeb9-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-288">D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "ventas")))</span><span class="sxs-lookup"><span data-stu-id="3eeb9-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="3eeb9-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas</span><span class="sxs-lookup"><span data-stu-id="3eeb9-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-290">Permitir la ejecución si alguno de los proyectos de usuario es de intersección con los proyectos de archivo.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="3eeb9-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3eeb9-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-292">D: (XA;; FX;;; S-1-1-0; ( @User.Project Cualquiera \_ de @Resource.Project ))</span><span class="sxs-lookup"><span data-stu-id="3eeb9-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="3eeb9-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Directivas</span><span class="sxs-lookup"><span data-stu-id="3eeb9-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-294">Permitir acceso de lectura si el usuario ha iniciado sesión con una tarjeta inteligente, es un operador de copia de seguridad y se está conectando desde un equipo con BitLocker habilitado.</span><span class="sxs-lookup"><span data-stu-id="3eeb9-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3eeb9-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3eeb9-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3eeb9-296">D: (XA;; FR;;; S-1-1-0; (Miembro \_ de {SID (SID de tarjeta inteligente \_ ), SID (BO)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="3eeb9-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3eeb9-297">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3eeb9-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3eeb9-298">[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="3eeb9-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

