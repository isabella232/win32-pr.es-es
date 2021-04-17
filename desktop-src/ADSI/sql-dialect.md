---
title: Dialecto SQL
description: El dialecto SQL, derivado del Lenguaje de consulta estructurado, utiliza expresiones legibles para el usuario para definir instrucciones de consulta.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- Lenguaje ADSI de dialecto SQL
- dialecto ADSI, dialecto SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656146"
---
# <a name="sql-dialect"></a>Dialecto SQL

El dialecto SQL, derivado del Lenguaje de consulta estructurado, utiliza expresiones legibles para el usuario para definir instrucciones de consulta. Use una instrucción de consulta SQL con las siguientes interfaces de búsqueda ADSI:

-   Interfaces de [objetos de datos ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , que son interfaces de automatización que utilizan OLE DB.
-   [OLE DB](searching-with-ole-db.md), que es un conjunto de interfaces de C/C++ para la consulta de bases de datos.

Las instrucciones SQL requieren la siguiente sintaxis.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



En la tabla siguiente se enumeran las palabras clave de instrucción de consulta SQL.



| Palabra clave  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Especifica una lista separada por comas de los atributos que se van a recuperar para cada objeto. Si especifica \* , la consulta solo recupera el ADsPath de cada objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Especifica el ADsPath de la base de la búsqueda. Por ejemplo, la ADsPath del contenedor de usuarios en un dominio de Active Directory podría ser "LDAP:Rio = users, DC = Fabrikam, DC = COM". Tenga en cuenta que la ruta de acceso está delimitada por un par de comillas simples (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Palabra clave opcional que especifica el filtro de la consulta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Palabra clave opcional que genera una ordenación del lado servidor si el servidor admite el control de ordenación LDAP. Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande. La lista de ordenación es una lista separada por comas de atributos por los que se va a ordenar. Tenga en cuenta que Active Directory solo admite una única clave de ordenación. Puede usar las palabras clave ASC y DESC opcionales para especificar el criterio de ordenación ascendente o descendente. el valor predeterminado es Ascending. La palabra clave ORDER BY invalida cualquier clave de ordenación especificada con la propiedad "Sort on" del objeto Command de ADO. |



 

> [!Note]  
> En los casos en los que se usa un juego de caracteres multibyte, si ADO realiza la búsqueda con el dialecto SQL, no se puede utilizar una barra diagonal inversa para los caracteres de escape. En su lugar, se deben usar las secuencias de escape que se enumeran en [caracteres especiales](search-filter-syntax.md) . Por ejemplo, para una instrucción que usaba la sintaxis "samAccountName = \( Test", que usa la barra diagonal inversa, " \\ ", para escapar el paréntesis de apertura, "(", en su lugar, reemplazaría la barra diagonal inversa por el carácter especial " \\ 28", como se indica a continuación: "samAccountName = \\ 28Test".

 

Las siguientes instrucciones de consulta son ejemplos de dialecto SQL en ADSI.

Para buscar todos los objetos de grupo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Para buscar todos los usuarios cuyo apellido empieza por la letra H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



La gramática formal de las consultas SQL se define en el ejemplo de código siguiente. Todas las palabras clave no distinguen mayúsculas de minúsculas.


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



Las combinaciones internas de SQL no son compatibles con el proveedor de OLE DB de Active Directory, pero puede usar SQL para combinar datos de SQL y Active Directory. Para obtener más información, vea [crear una combinación heterogénea entre SQL Server y Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de filtro de búsqueda](search-filter-syntax.md)
</dt> <dt>

[Dialecto LDAP](ldap-dialect.md)
</dt> <dt>

[Buscar con la interfaz IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Buscar con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




