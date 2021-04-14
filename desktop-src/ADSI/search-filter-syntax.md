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
# <a name="search-filter-syntax"></a>Sintaxis de filtro de búsqueda

Los filtros de búsqueda permiten definir criterios de búsqueda y proporcionar búsquedas más eficaces y eficaces.

ADSI admite los filtros de búsqueda LDAP, tal y como se define en RFC2254. Estos filtros de búsqueda se representan mediante cadenas Unicode. En la tabla siguiente se enumeran algunos ejemplos de filtros de búsqueda LDAP.



| Filtro de búsqueda                                                               | Descripción                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass = \* )"                                                          | Todos los objetos.                                               |
| "(& (objectCategory = person) (objectClass = User) (! ( CN = Andy)) "                  | Todos los objetos de usuario, pero "Andy".                               |
| "(SN = SM \* )"                                                                 | Todos los objetos con un apellido que empieza por "SM".          |
| "(& (objectCategory = person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson))" | Todos los contactos cuyo apellido sea igual a "Smith" o "Johnson". |



 

Estos filtros de búsqueda usan uno de los siguientes formatos.


```C++
<filter>=(<attribute><operator><value>)
```



or


```C++
(<operator><filter1><filter2>)
```



Los filtros de búsqueda ADSI se utilizan de dos maneras. Forman una parte del dialecto LDAP para enviar consultas a través del proveedor de OLE DB. También se usan con la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

## <a name="operators"></a>Operadores

En la tabla siguiente se enumeran los operadores de filtro de búsqueda usados con frecuencia.



| Operador lógico | Descripción                                |
|------------------|--------------------------------------------|
| =                | Igual a                                   |
| ~=               | Aproximadamente igual a                     |
| <=            | Lexicográficamente menor o igual que    |
| >=            | Lexicográficamente mayor o igual que |
| &                | y                                        |
| \|               | O BIEN                                         |
| !                | NOT                                        |



 

Además de los operadores anteriores, LDAP define dos identificadores de objeto de regla de coincidencia (OID) que se pueden usar para realizar comparaciones bit a bit de valores numéricos. Las reglas de coincidencia tienen la siguiente sintaxis.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; Attribute name &gt; " es el **lDAPDisplayName** del atributo, " &lt; Rule OID &gt; " es el OID de la regla de coincidencia y " &lt; Value &gt; " es el valor que se va a usar para la comparación. Tenga en cuenta que no se pueden usar espacios en esta cadena. " &lt; valor &gt; " debe ser un número decimal; no puede ser un número hexadecimal o un nombre de constante, como la **seguridad del tipo de grupo de ADS \_ \_ \_ \_ habilitada**. Para obtener más información sobre los atributos de Active Directory disponibles, vea [todos los atributos](/windows/desktop/ADSchema/attributes-all).

En la tabla siguiente se enumeran los OID de regla de coincidencia implementados por LDAP.



| OID de la regla de coincidencia       | Identificador de cadena (de Ntldap. h)   | Descripción                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **\_ \_ bit de la regla de coincidencia LDAP \_ \_ y**  | Se encuentra una coincidencia solo si todos los bits del atributo coinciden con el valor. Esta regla es equivalente a **un operador and bit a bit** .                                                                  |
| 1.2.840.113556.1.4.804  | **\_ \_ bit de la regla de coincidencia LDAP \_ \_ o**   | Se encuentra una coincidencia si algún bit del atributo coincide con el valor. Esta regla es equivalente a **un operador OR** bit a bit.                                                                        |
| 1.2.840.113556.1.4.1941 | **\_ \_ regla de coincidencia LDAP \_ en \_ cadena** | Esta regla se limita a los filtros que se aplican al DN. Se trata de un operador de coincidencia "extendido" especial que recorre la cadena de ascendencia en objetos hasta la raíz hasta que encuentra una coincidencia. |



 

En el ejemplo siguiente se busca una cadena de consulta para los objetos de grupo que tienen establecida la marca **\_ \_ \_ seguridad \_ habilitada de tipo de grupo ADS** . Tenga en cuenta que el valor decimal del **tipo de grupo de ADS \_ \_ con \_ seguridad \_ habilitada** (0x80000000 = 2147483648) se usa para el valor de comparación.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



La **\_ \_ regla de coincidencia LDAP \_ en \_ cadena** es un OID de regla de coincidencia diseñado para proporcionar un método para buscar la ascendencia de un objeto. Muchas aplicaciones que usan AD y AD LDS suelen trabajar con datos jerárquicos, que están ordenados por relaciones de elementos primarios y secundarios. Anteriormente, las aplicaciones realizaban la expansión de grupos transitiva para averiguar la pertenencia a grupos, que usaba demasiado ancho de banda de red. aplicaciones necesarias para realizar varios recorridos de ida y vuelta para averiguar si un objeto cayó "en la cadena" Si un vínculo se atraviesa hasta el final.

Un ejemplo de este tipo de consulta está diseñado para comprobar si un usuario "user1" es miembro del grupo "Group1". Establecería la base en el DN del usuario `(cn=user1, cn=users, dc=x)` y el ámbito en `base` , y utilizaría la siguiente consulta.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Del mismo modo, para buscar todos los grupos de los que es miembro "user1", establezca la base en el DN del contenedor grupos; por ejemplo `(OU=groupsOU, dc=x)` , y el ámbito a `subtree` , y usar el siguiente filtro.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Tenga en cuenta que cuando se usa la **\_ \_ regla de coincidencia LDAP \_ en la \_ cadena**, el ámbito no es limitado; puede ser `base` , `one-level` o `subtree` . Algunas de estas consultas en subárboles pueden hacer un uso intensivo del procesador, como buscar vínculos con un gran abanico de salida. es decir, enumera todos los grupos de los que es miembro un usuario. Las búsquedas ineficaces registrarán los mensajes de registro de eventos adecuados, como con cualquier otro tipo de consulta.

## <a name="wildcards"></a>Caracteres comodín

También puede Agregar caracteres comodín y condiciones a un filtro de búsqueda LDAP. En los ejemplos siguientes se muestran las subcadenas que se pueden usar para buscar en el directorio.

Obtener todas las entradas:


```C++
(objectClass=*)
```



Obtener entradas que contengan "Bob" en algún lugar del nombre común:


```C++
(cn=*bob*)
```



Obtener entradas con un nombre común mayor o igual que "Bob":


```C++
(cn>='bob')
```



Obtener todos los usuarios con un atributo de correo electrónico:


```C++
(&(objectClass=user)(email=*))
```



Obtener todas las entradas de usuario con un atributo de correo electrónico y un apellido igual a "Smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Obtiene todas las entradas de usuario con un nombre común que empieza por "Andy", "Steve" o "Margaret":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Obtener todas las entradas sin un atributo de correo electrónico:


```C++
(!(email=*))
```



La definición formal del filtro de búsqueda es la siguiente (desde [RFC 2254](https://tools.ietf.org/html/rfc2254)):


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



El &lt; atributo ATTR &gt; es una cadena que representa un attributeType. El valor del token &lt; &gt; es una cadena que representa un AttributeValue cuyo formato se define en el servicio de directorio subyacente.

Si un &lt; valor &gt; debe contener el carácter de asterisco ( \* ), de paréntesis de apertura (() o de paréntesis de cierre ()), el carácter debe ir precedido del carácter de escape de barra diagonal inversa ( \\ ).

## <a name="special-characters"></a>Caracteres especiales

Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de búsqueda como literales, deben reemplazarse por la secuencia de escape indicada.



| Carácter ASCII | Sustitución de secuencias de escape |
|-----------------|----------------------------|
| \*              | \\2                       |
| (               | \\26                       |
| )               | \\29                       |
| \\              | \\quater                       |
| NUL             | \\0                       |
| /               | \\relativa                       |



 

> [!Note]  
> En los casos en los que se usa un juego de caracteres multibyte, se deben usar las secuencias de escape enumeradas anteriormente si ADO realiza la búsqueda con el dialecto SQL.

 

Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de secuencia de escape codificando cada byte de datos binarios con la barra diagonal inversa ( \\ ) seguida de dos dígitos hexadecimales. Por ejemplo, el valor de cuatro bytes 0x00000004 se codifica como \\ 00 \\ 00 \\ 00 \\ 04 en una cadena de filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dialecto LDAP](ldap-dialect.md)
</dt> <dt>

[Dialecto SQL](sql-dialect.md)
</dt> <dt>

[Buscar con la interfaz IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Buscar con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
