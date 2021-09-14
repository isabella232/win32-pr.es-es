---
title: Sintaxis de filtro de búsqueda
description: Los filtros de búsqueda permiten definir criterios de búsqueda y proporcionar búsquedas más eficaces y eficaces.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- ADSI de sintaxis de filtro de búsqueda
- consultas, sintaxis de filtro de búsqueda
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172170"
---
# <a name="search-filter-syntax"></a>Sintaxis de filtro de búsqueda

Los filtros de búsqueda permiten definir criterios de búsqueda y proporcionar búsquedas más eficaces y eficaces.

ADSI admite los filtros de búsqueda LDAP tal como se define en RFC2254. Estos filtros de búsqueda se representan mediante cadenas Unicode. En la tabla siguiente se enumeran algunos ejemplos de filtros de búsqueda LDAP.



| Filtro de búsqueda                                                               | Descripción                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass= \* )"                                                          | Todos los objetos.                                               |
| "(&(objectCategory=person)(objectClass=user)(!( cn=andy)))"                  | Todos los objetos de usuario menos "andy".                               |
| "(sn=sm \* )"                                                                 | Todos los objetos con un apellido que empieza por "sm".          |
| "(&(objectCategory=person)(objectClass=contact)( \| (sn=Smith)(sn=Johnson)))" | Todos los contactos con un apellido igual a "Smith" o "Smith". |



 

Estos filtros de búsqueda usan uno de los siguientes formatos.


```C++
<filter>=(<attribute><operator><value>)
```



o


```C++
(<operator><filter1><filter2>)
```



Los filtros de búsqueda adsi se usan de dos maneras. Forman parte del dialecto LDAP para enviar consultas a través del OLE DB cliente. También se usan con la [**interfaz IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

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



 

Además de los operadores anteriores, LDAP define dos identificadores de objeto de regla (ID) que se pueden usar para realizar comparaciones bit a bit de valores numéricos. Las reglas de coincidencia tienen la sintaxis siguiente.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; attribute name " is the &gt; **lDAPDisplayName** of the attribute, " &lt; rule OID " is the &gt; OID for the matching rule, and " value " is the &lt; value to use for &gt; comparison. Tenga en cuenta que los espacios no se pueden usar en esta cadena. " &lt; value " debe ser un número decimal; no puede ser un número hexadecimal o un nombre constante como &gt; ADS GROUP TYPE SECURITY **\_ \_ \_ \_ ENABLED**. Para obtener más información sobre los atributos de Active Directory disponibles, vea [Todos los atributos](/windows/desktop/ADSchema/attributes-all).

En la tabla siguiente se enumeran los ED de regla de coincidencia implementados por LDAP.



| OID de regla de coincidencia       | Identificador de cadena (de Ntldap.h)   | Descripción                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **BIT \_ DE REGLA DE COINCIDENCIA LDAP \_ \_ \_ Y**  | Solo se encuentra una coincidencia si todos los bits del atributo coinciden con el valor . Esta regla es equivalente a un operador **AND** bit a bit.                                                                  |
| 1.2.840.113556.1.4.804  | **BIT \_ DE REGLA DE COINCIDENCIA LDAP \_ \_ \_ O**   | Se encuentra una coincidencia si algún bit del atributo coincide con el valor . Esta regla es equivalente a un operador **OR** bit a bit.                                                                        |
| 1.2.840.113556.1.4.1941 | **REGLA \_ DE COINCIDENCIA LDAP EN \_ \_ \_ CADENA** | Esta regla se limita a los filtros que se aplican al DN. Se trata de un operador de coincidencia especial "extendido" que recorre la cadena de objetos hasta la raíz hasta encontrar una coincidencia. |



 

En la siguiente cadena de consulta de ejemplo se buscan objetos de grupo que tienen establecida la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.** Tenga en cuenta que el valor decimal de **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648) se usa para el valor de comparación.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



**LDAP \_ MATCHING \_ RULE IN \_ \_ CHAIN** es un OID de regla de coincidencia que está diseñado para proporcionar un método para buscar el descaro de un objeto. Muchas aplicaciones que usan AD AD LDS suelen trabajar con datos jerárquicos, ordenados por relaciones de elementos primarios y secundarios. Anteriormente, las aplicaciones realizaban una expansión transitiva de grupos para averiguar la pertenencia a grupos, que usaba demasiado ancho de banda de red. Las aplicaciones necesitaban realizar varios recorridos de ida y vuelta para averiguar si un objeto caía "en la cadena" si se atraviesa un vínculo hasta el final.

Un ejemplo de este tipo de consulta es uno diseñado para comprobar si un usuario "user1" es miembro del grupo "group1". Establecería la base en el DN de usuario `(cn=user1, cn=users, dc=x)` y el ámbito en y `base` usaría la consulta siguiente.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Del mismo modo, para buscar todos los grupos de los que "user1" es miembro, establezca la base en el DN del contenedor de grupos; por `(OU=groupsOU, dc=x)` ejemplo, y el ámbito de `subtree` , y use el filtro siguiente.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Tenga en cuenta que cuando **se usa LDAP \_ MATCHING RULE IN \_ \_ \_ CHAIN**, el ámbito no está limitado, puede ser `base` , o `one-level` `subtree` . Algunas de estas consultas en subárboles pueden ser más intensivas en el procesador, como la búsqueda de vínculos con un alto nivel de salida. es decir, enumerar todos los grupos de los que es miembro un usuario. Las búsquedas ineficaces registrarán los mensajes de registro de eventos adecuados, como con cualquier otro tipo de consulta.

## <a name="wildcards"></a>Caracteres comodín

También puede agregar caracteres comodín y condiciones a un filtro de búsqueda LDAP. En los ejemplos siguientes se muestran subcadenas que se pueden usar para buscar en el directorio.

Obtenga todas las entradas:


```C++
(objectClass=*)
```



Obtenga entradas que contengan "bob" en algún lugar del nombre común:


```C++
(cn=*bob*)
```



Obtenga entradas con un nombre común mayor o igual que "bob":


```C++
(cn>='bob')
```



Obtenga todos los usuarios con un atributo de correo electrónico:


```C++
(&(objectClass=user)(email=*))
```



Obtenga todas las entradas de usuario con un atributo de correo electrónico y un apellido igual a "smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Obtenga todas las entradas de usuario con un nombre común que comience por "andy", "steve" o "iam":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Obtenga todas las entradas sin un atributo de correo electrónico:


```C++
(!(email=*))
```



La definición formal del filtro de búsqueda es la siguiente (de [RFC 2254):](https://tools.ietf.org/html/rfc2254)


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



El token &lt; attr &gt; es una cadena que representa un AttributeType. El valor &lt; del token es una cadena que representa un &gt; AttributeValue cuyo formato está definido por el servicio de directorio subyacente.

Si un valor debe contener el carácter de asterisco ( ), paréntesis izquierdo (() o paréntesis derecho &lt; &gt; \* ()), el carácter debe ir precedido del carácter de escape de barra diagonal inversa ( \\ ).

## <a name="special-characters"></a>Caracteres especiales

Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de búsqueda como literales, se deben reemplazar por la secuencia de escape enumerada.



| Carácter ASCII | Sustituto de secuencia de escape |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\29                       |
| \\              | \\5c                       |
| NUL             | \\00                       |
| /               | \\2f                       |



 

> [!Note]  
> En los casos en los que se usa un juego de caracteres multibyte, se deben usar las secuencias de escape enumeradas anteriormente si ADO realiza la búsqueda con el dialecto SQL.

 

Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de secuencia de escape codificando cada byte de datos binarios con la barra diagonal inversa ( ) seguida de \\ dos dígitos hexadecimales. Por ejemplo, el valor de cuatro 0x00000004 se codifica como \\ 00 \\ 00 \\ 00 \\ 00 04 en una cadena de filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dialecto LDAP](ldap-dialect.md)
</dt> <dt>

[SQL dialecto](sql-dialect.md)
</dt> <dt>

[Búsqueda con la interfaz IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Búsqueda con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Búsqueda con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
