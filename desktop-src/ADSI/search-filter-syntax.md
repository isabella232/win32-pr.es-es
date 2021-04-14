---
title: Sintaxis de filtro de búsqueda
description: Los filtros de búsqueda permiten definir criterios de búsqueda y proporcionar búsquedas más eficaces y eficaces.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Sintaxis de filtro de búsqueda ADSI
- consultas, sintaxis de filtro de búsqueda
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105661421"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="ba8ee-105">Sintaxis de filtro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ba8ee-105">Search Filter Syntax</span></span>

<span data-ttu-id="ba8ee-106">Los filtros de búsqueda permiten definir criterios de búsqueda y proporcionar búsquedas más eficaces y eficaces.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="ba8ee-107">ADSI admite los filtros de búsqueda LDAP, tal y como se define en RFC2254.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="ba8ee-108">Estos filtros de búsqueda se representan mediante cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="ba8ee-109">En la tabla siguiente se enumeran algunos ejemplos de filtros de búsqueda LDAP.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="ba8ee-110">Filtro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ba8ee-110">Search filter</span></span>                                                               | <span data-ttu-id="ba8ee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8ee-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ba8ee-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="ba8ee-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="ba8ee-113">Todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-113">All objects.</span></span>                                               |
| <span data-ttu-id="ba8ee-114">"(& (objectCategory = person) (objectClass = User) (! ( CN = Andy)) "</span><span class="sxs-lookup"><span data-stu-id="ba8ee-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="ba8ee-115">Todos los objetos de usuario, pero "Andy".</span><span class="sxs-lookup"><span data-stu-id="ba8ee-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="ba8ee-116">"(SN = SM \* )"</span><span class="sxs-lookup"><span data-stu-id="ba8ee-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="ba8ee-117">Todos los objetos con un apellido que empieza por "SM".</span><span class="sxs-lookup"><span data-stu-id="ba8ee-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="ba8ee-118">"(& (objectCategory = person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson))"</span><span class="sxs-lookup"><span data-stu-id="ba8ee-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="ba8ee-119">Todos los contactos cuyo apellido sea igual a "Smith" o "Johnson".</span><span class="sxs-lookup"><span data-stu-id="ba8ee-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="ba8ee-120">Estos filtros de búsqueda usan uno de los siguientes formatos.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="ba8ee-121">or</span><span class="sxs-lookup"><span data-stu-id="ba8ee-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="ba8ee-122">Los filtros de búsqueda ADSI se utilizan de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="ba8ee-123">Forman una parte del dialecto LDAP para enviar consultas a través del proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="ba8ee-124">También se usan con la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="ba8ee-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="ba8ee-125">Operadores</span><span class="sxs-lookup"><span data-stu-id="ba8ee-125">Operators</span></span>

<span data-ttu-id="ba8ee-126">En la tabla siguiente se enumeran los operadores de filtro de búsqueda usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="ba8ee-127">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="ba8ee-127">Logical operator</span></span> | <span data-ttu-id="ba8ee-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8ee-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="ba8ee-129">Igual a</span><span class="sxs-lookup"><span data-stu-id="ba8ee-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="ba8ee-130">Aproximadamente igual a</span><span class="sxs-lookup"><span data-stu-id="ba8ee-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="ba8ee-131">Lexicográficamente menor o igual que</span><span class="sxs-lookup"><span data-stu-id="ba8ee-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="ba8ee-132">Lexicográficamente mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="ba8ee-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="ba8ee-133">y</span><span class="sxs-lookup"><span data-stu-id="ba8ee-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="ba8ee-134">O BIEN</span><span class="sxs-lookup"><span data-stu-id="ba8ee-134">OR</span></span>                                         |
| <span data-ttu-id="ba8ee-135">!</span><span class="sxs-lookup"><span data-stu-id="ba8ee-135">!</span></span>                | <span data-ttu-id="ba8ee-136">NOT</span><span class="sxs-lookup"><span data-stu-id="ba8ee-136">NOT</span></span>                                        |



 

<span data-ttu-id="ba8ee-137">Además de los operadores anteriores, LDAP define dos identificadores de objeto de regla de coincidencia (OID) que se pueden usar para realizar comparaciones bit a bit de valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="ba8ee-138">Las reglas de coincidencia tienen la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="ba8ee-139">" &lt; Attribute name &gt; " es el **lDAPDisplayName** del atributo, " &lt; Rule OID &gt; " es el OID de la regla de coincidencia y " &lt; Value &gt; " es el valor que se va a usar para la comparación.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="ba8ee-140">Tenga en cuenta que no se pueden usar espacios en esta cadena.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="ba8ee-141">" &lt; valor &gt; " debe ser un número decimal; no puede ser un número hexadecimal o un nombre de constante, como la **seguridad del tipo de grupo de ADS \_ \_ \_ \_ habilitada**.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="ba8ee-142">Para obtener más información sobre los atributos de Active Directory disponibles, vea [todos los atributos](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="ba8ee-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="ba8ee-143">En la tabla siguiente se enumeran los OID de regla de coincidencia implementados por LDAP.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="ba8ee-144">OID de la regla de coincidencia</span><span class="sxs-lookup"><span data-stu-id="ba8ee-144">Matching rule OID</span></span>       | <span data-ttu-id="ba8ee-145">Identificador de cadena (de Ntldap. h)</span><span class="sxs-lookup"><span data-stu-id="ba8ee-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="ba8ee-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8ee-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8ee-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="ba8ee-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="ba8ee-148">**\_ \_ bit de la regla de coincidencia LDAP \_ \_ y**</span><span class="sxs-lookup"><span data-stu-id="ba8ee-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="ba8ee-149">Se encuentra una coincidencia solo si todos los bits del atributo coinciden con el valor.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="ba8ee-150">Esta regla es equivalente a **un operador and bit a bit** .</span><span class="sxs-lookup"><span data-stu-id="ba8ee-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="ba8ee-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="ba8ee-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="ba8ee-152">**\_ \_ bit de la regla de coincidencia LDAP \_ \_ o**</span><span class="sxs-lookup"><span data-stu-id="ba8ee-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="ba8ee-153">Se encuentra una coincidencia si algún bit del atributo coincide con el valor.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="ba8ee-154">Esta regla es equivalente a **un operador OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="ba8ee-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="ba8ee-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="ba8ee-156">**\_ \_ regla de coincidencia LDAP \_ en \_ cadena**</span><span class="sxs-lookup"><span data-stu-id="ba8ee-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="ba8ee-157">Esta regla se limita a los filtros que se aplican al DN.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="ba8ee-158">Se trata de un operador de coincidencia "extendido" especial que recorre la cadena de ascendencia en objetos hasta la raíz hasta que encuentra una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="ba8ee-159">En el ejemplo siguiente se busca una cadena de consulta para los objetos de grupo que tienen establecida la marca **\_ \_ \_ seguridad \_ habilitada de tipo de grupo ADS** .</span><span class="sxs-lookup"><span data-stu-id="ba8ee-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="ba8ee-160">Tenga en cuenta que el valor decimal del **tipo de grupo de ADS \_ \_ con \_ seguridad \_ habilitada** (0x80000000 = 2147483648) se usa para el valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="ba8ee-161">La **\_ \_ regla de coincidencia LDAP \_ en \_ cadena** es un OID de regla de coincidencia diseñado para proporcionar un método para buscar la ascendencia de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="ba8ee-162">Muchas aplicaciones que usan AD y AD LDS suelen trabajar con datos jerárquicos, que están ordenados por relaciones de elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="ba8ee-163">Anteriormente, las aplicaciones realizaban la expansión de grupos transitiva para averiguar la pertenencia a grupos, que usaba demasiado ancho de banda de red. aplicaciones necesarias para realizar varios recorridos de ida y vuelta para averiguar si un objeto cayó "en la cadena" Si un vínculo se atraviesa hasta el final.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="ba8ee-164">Un ejemplo de este tipo de consulta está diseñado para comprobar si un usuario "user1" es miembro del grupo "Group1".</span><span class="sxs-lookup"><span data-stu-id="ba8ee-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="ba8ee-165">Establecería la base en el DN del usuario `(cn=user1, cn=users, dc=x)` y el ámbito en `base` , y utilizaría la siguiente consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="ba8ee-166">Del mismo modo, para buscar todos los grupos de los que es miembro "user1", establezca la base en el DN del contenedor grupos; por ejemplo `(OU=groupsOU, dc=x)` , y el ámbito a `subtree` , y usar el siguiente filtro.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="ba8ee-167">Tenga en cuenta que cuando se usa la **\_ \_ regla de coincidencia LDAP \_ en la \_ cadena**, el ámbito no es limitado; puede ser `base` , `one-level` o `subtree` .</span><span class="sxs-lookup"><span data-stu-id="ba8ee-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="ba8ee-168">Algunas de estas consultas en subárboles pueden hacer un uso intensivo del procesador, como buscar vínculos con un gran abanico de salida. es decir, enumera todos los grupos de los que es miembro un usuario.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="ba8ee-169">Las búsquedas ineficaces registrarán los mensajes de registro de eventos adecuados, como con cualquier otro tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="ba8ee-170">Caracteres comodín</span><span class="sxs-lookup"><span data-stu-id="ba8ee-170">Wildcards</span></span>

<span data-ttu-id="ba8ee-171">También puede Agregar caracteres comodín y condiciones a un filtro de búsqueda LDAP.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="ba8ee-172">En los ejemplos siguientes se muestran las subcadenas que se pueden usar para buscar en el directorio.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="ba8ee-173">Obtener todas las entradas:</span><span class="sxs-lookup"><span data-stu-id="ba8ee-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="ba8ee-174">Obtener entradas que contengan "Bob" en algún lugar del nombre común:</span><span class="sxs-lookup"><span data-stu-id="ba8ee-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="ba8ee-175">Obtener entradas con un nombre común mayor o igual que "Bob":</span><span class="sxs-lookup"><span data-stu-id="ba8ee-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="ba8ee-176">Obtener todos los usuarios con un atributo de correo electrónico:</span><span class="sxs-lookup"><span data-stu-id="ba8ee-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="ba8ee-177">Obtener todas las entradas de usuario con un atributo de correo electrónico y un apellido igual a "Smith":</span><span class="sxs-lookup"><span data-stu-id="ba8ee-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="ba8ee-178">Obtiene todas las entradas de usuario con un nombre común que empieza por "Andy", "Steve" o "Margaret":</span><span class="sxs-lookup"><span data-stu-id="ba8ee-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="ba8ee-179">Obtener todas las entradas sin un atributo de correo electrónico:</span><span class="sxs-lookup"><span data-stu-id="ba8ee-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="ba8ee-180">La definición formal del filtro de búsqueda es la siguiente (desde [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span><span class="sxs-lookup"><span data-stu-id="ba8ee-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="ba8ee-181">El &lt; atributo ATTR &gt; es una cadena que representa un attributeType.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="ba8ee-182">El valor del token &lt; &gt; es una cadena que representa un AttributeValue cuyo formato se define en el servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="ba8ee-183">Si un &lt; valor &gt; debe contener el carácter de asterisco ( \* ), de paréntesis de apertura (() o de paréntesis de cierre ()), el carácter debe ir precedido del carácter de escape de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="ba8ee-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="ba8ee-184">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="ba8ee-184">Special Characters</span></span>

<span data-ttu-id="ba8ee-185">Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de búsqueda como literales, deben reemplazarse por la secuencia de escape indicada.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="ba8ee-186">Carácter ASCII</span><span class="sxs-lookup"><span data-stu-id="ba8ee-186">ASCII character</span></span> | <span data-ttu-id="ba8ee-187">Sustitución de secuencias de escape</span><span class="sxs-lookup"><span data-stu-id="ba8ee-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="ba8ee-188">\\2</span><span class="sxs-lookup"><span data-stu-id="ba8ee-188">\\2a</span></span>                       |
| <span data-ttu-id="ba8ee-189">(</span><span class="sxs-lookup"><span data-stu-id="ba8ee-189">(</span></span>               | <span data-ttu-id="ba8ee-190">\\26</span><span class="sxs-lookup"><span data-stu-id="ba8ee-190">\\28</span></span>                       |
| <span data-ttu-id="ba8ee-191">)</span><span class="sxs-lookup"><span data-stu-id="ba8ee-191">)</span></span>               | <span data-ttu-id="ba8ee-192">\\29</span><span class="sxs-lookup"><span data-stu-id="ba8ee-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="ba8ee-193">\\quater</span><span class="sxs-lookup"><span data-stu-id="ba8ee-193">\\5c</span></span>                       |
| <span data-ttu-id="ba8ee-194">NUL</span><span class="sxs-lookup"><span data-stu-id="ba8ee-194">NUL</span></span>             | <span data-ttu-id="ba8ee-195">\\0</span><span class="sxs-lookup"><span data-stu-id="ba8ee-195">\\00</span></span>                       |
| /               | <span data-ttu-id="ba8ee-196">\\relativa</span><span class="sxs-lookup"><span data-stu-id="ba8ee-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="ba8ee-197">En los casos en los que se usa un juego de caracteres multibyte, se deben usar las secuencias de escape enumeradas anteriormente si ADO realiza la búsqueda con el dialecto SQL.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="ba8ee-198">Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de secuencia de escape codificando cada byte de datos binarios con la barra diagonal inversa ( \\ ) seguida de dos dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="ba8ee-199">Por ejemplo, el valor de cuatro bytes 0x00000004 se codifica como \\ 00 \\ 00 \\ 00 \\ 04 en una cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="ba8ee-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba8ee-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba8ee-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba8ee-201">Dialecto LDAP</span><span class="sxs-lookup"><span data-stu-id="ba8ee-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="ba8ee-202">Dialecto SQL</span><span class="sxs-lookup"><span data-stu-id="ba8ee-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="ba8ee-203">Buscar con la interfaz IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="ba8ee-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="ba8ee-204">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="ba8ee-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="ba8ee-205">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="ba8ee-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
