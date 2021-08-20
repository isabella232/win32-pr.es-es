---
title: Crear un filtro de consulta
description: Un filtro de consulta indica Active Directory Domain Services buscar datos en una sintaxis de consulta LDAP. Todas las tecnologías de acceso a datos especificadas enumeradas en el tema Elección de la tecnología de búsqueda admiten la sintaxis de consulta LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , crear un filtro de consulta
- filtros de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5241cb288051515c1198c9979ef7d1a71d18524b3b2f3504f2b9141b6fb8a24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020865"
---
# <a name="creating-a-query-filter"></a>Crear un filtro de consulta

Un filtro de consulta indica Active Directory Domain Services buscar datos en una sintaxis de consulta LDAP. Todas las tecnologías de acceso a datos especificadas enumeradas en el tema [Elección de](choosing-the-search-technology.md) la tecnología de búsqueda admiten la sintaxis de consulta LDAP.

La sintaxis de consulta LDAP es la siguiente:


```C++
<expression><expression>...
```



Un filtro puede contener una o varias expresiones. Una expresión tiene el formato siguiente:


```C++
(<logicaloperator><comparison><comparison...>)
```



donde " &lt; logicaloperator &gt; " es uno de los siguientes.



| Operador        | Descripción                |
|-----------------|----------------------------|
| "\|"<br/> | OR **lógico**<br/>  |
| "&"<br/>  | AND **lógico**<br/> |
| "!"<br/>  | NOT **lógico**<br/> |



 

y " &lt; comparación " son los &gt; siguientes:


```C++
(<attribute><operator><value>)
```



donde " &lt; attribute " es el &gt; **lDAPDisplayName** del atributo que se va a evaluar, " value " es el valor con el que comparar y el operador " " es uno de los operadores de &lt; comparación &gt; &lt; &gt; siguientes.



| Operador           | Descripción                         |
|--------------------|-------------------------------------|
| "="<br/>     | Es igual que<br/>                   |
| "~="<br/>    | Aproximadamente igual a<br/>     |
| "<="<br/> | Menor o igual que<br/>    |
| ">="<br/> | Mayor o igual que<br/> |



 

Además, dependiendo de la sintaxis del atributo, el valor " &lt; " puede contener el símbolo &gt; comodín (" \* "). Un valor &lt; " " que contiene solo un carácter &gt; comodín comprobará la existencia de cualquier valor en " &lt; atributo &gt; ". Si no se establece ningún valor para el atributo " ", se producirá un error &lt; &gt; en la prueba.

Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de consulta como literales, se deben reemplazar por la secuencia de escape enumerada.



| Carácter ASCII    | Sustitución de secuencia de escape |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2a"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5c"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de secuencia de escape mediante la codificación de cada byte de datos binarios con la barra diagonal inversa seguida de dos dígitos hexadecimales. Por ejemplo, el valor de cuatro bytes 0x00000004 codifica como \\ "00 \\ 00 \\ 00 \\ 04" en una cadena de filtro.

## <a name="examples"></a>Ejemplos

La siguiente cadena de consulta buscará todos los objetos de tipo "computer".


```C++
(objectCategory=computer)
```



La siguiente cadena de consulta buscará todos los objetos de tipo "equipo" con un nombre que comience por "desktop".


```C++
(&(objectCategory=computer)(name=desktop*))
```



La siguiente cadena de consulta buscará todos los objetos de tipo "equipo" con un nombre que comience por "desktop" o un nombre que comience por "notebook".


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



La siguiente cadena de consulta buscará todos los objetos de tipo "usuario" que tengan un número de teléfono principal.


```C++
(&(objectCategory=user)(homePhone=*))
```



Para obtener más información sobre las cadenas de filtro de consulta y los ejemplos de uso, vea:

-   [Buscar objetos por clase](finding-objects-by-class.md)
-   [Buscar objetos por nombre](finding-objects-by-name.md)
-   [Buscar una lista de atributos para consultar](finding-a-list-of-attributes-to-query.md)
-   [Comprobación de la sintaxis del filtro de consulta](checking-the-query-filter-syntax.md)
-   [Cómo especificar valores de comparación](how-to-specify-comparison-values.md)

 

 





