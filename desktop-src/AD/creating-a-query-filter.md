---
title: Crear un filtro de consulta
description: Un filtro de consulta indica a Active Directory Domain Services que busque los datos en una sintaxis de consulta LDAP. Todas las tecnologías de acceso a datos especificadas que se enumeran en el tema elección de la tecnología de búsqueda admiten la sintaxis de consultas LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, crear un filtro de consulta
- filtros de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903003"
---
# <a name="creating-a-query-filter"></a>Crear un filtro de consulta

Un filtro de consulta indica a Active Directory Domain Services que busque los datos en una sintaxis de consulta LDAP. Todas las tecnologías de acceso a datos especificadas que se enumeran en el tema [elección de la tecnología de búsqueda](choosing-the-search-technology.md) admiten la sintaxis de consultas LDAP.

La sintaxis de consulta LDAP es la siguiente:


```C++
<expression><expression>...
```



Un filtro puede contener una o varias expresiones. Una expresión tiene el formato siguiente:


```C++
(<logicaloperator><comparison><comparison...>)
```



donde " &lt; operadorlógico &gt; " es uno de los siguientes.



| Operator        | Descripción                |
|-----------------|----------------------------|
| "\|"<br/> | **Or** lógico<br/>  |
| "&"<br/>  | **And** lógico<br/> |
| "!"<br/>  | **Not** lógico<br/> |



 

y " &lt; Comparison &gt; " es lo siguiente:


```C++
(<attribute><operator><value>)
```



donde " &lt; Attribute &gt; " es el **lDAPDisplayName** del atributo que se va a evaluar, " &lt; Value &gt; " es el valor con el que se va a comparar y " &lt; Operator &gt; " es uno de los siguientes operadores de comparación.



| Operator           | Descripción                         |
|--------------------|-------------------------------------|
| "="<br/>     | Equals<br/>                   |
| "~="<br/>    | Aproximadamente es igual a<br/>     |
| "<="<br/> | Menor o igual que<br/>    |
| ">="<br/> | Mayor o igual que<br/> |



 

Además, dependiendo de la sintaxis de atributo, el " &lt; valor &gt; " puede contener el símbolo comodín (" \* "). Un " &lt; valor &gt; " que solo contenga un carácter comodín comprobará la existencia de cualquier valor en " &lt; Attribute &gt; ". Si no se establece ningún valor para " &lt; Attribute &gt; ", se producirá un error en la prueba.

Si alguno de los siguientes caracteres especiales debe aparecer en el filtro de consulta como literales, deben reemplazarse por la secuencia de escape indicada.



| Carácter ASCII    | Sustitución de secuencias de escape |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2A"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5C"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

Además, los datos binarios arbitrarios se pueden representar mediante la sintaxis de la secuencia de escape codificando cada byte de datos binarios con la barra diagonal inversa seguida de dos dígitos hexadecimales. Por ejemplo, el valor de cuatro bytes 0x00000004 se codifica como " \\ 00 \\ 00 \\ 00 \\ 04" en una cadena de filtro.

## <a name="examples"></a>Ejemplos

La cadena de consulta siguiente buscará todos los objetos de tipo "Computer".


```C++
(objectCategory=computer)
```



La siguiente cadena de consulta buscará todos los objetos de tipo "equipo" con un nombre que comience por "escritorio".


```C++
(&(objectCategory=computer)(name=desktop*))
```



La siguiente cadena de consulta buscará todos los objetos de tipo "Computer" con un nombre que comience por "Desktop" o un nombre que comience por "Notebook".


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



La cadena de consulta siguiente buscará todos los objetos de tipo "usuario" que tengan un número de teléfono particular.


```C++
(&(objectCategory=user)(homePhone=*))
```



Para obtener más información acerca de las cadenas de filtro de consulta y ejemplos de uso, vea:

-   [Buscar objetos por clase](finding-objects-by-class.md)
-   [Buscar objetos por nombre](finding-objects-by-name.md)
-   [Buscar una lista de atributos para consultar](finding-a-list-of-attributes-to-query.md)
-   [Comprobar la sintaxis del filtro de consulta](checking-the-query-filter-syntax.md)
-   [Cómo especificar valores de comparación](how-to-specify-comparison-values.md)

 

 





