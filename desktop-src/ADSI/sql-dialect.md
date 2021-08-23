---
title: SQL Dialecto
description: El SQL, derivado del Lenguaje de consulta estructurado, usa expresiones legibles para definir instrucciones de consulta.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL Dialect ADSI
- dialect ADSI , SQL dialecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7483a5e3785f410e6c2fd875122ba24618a82b70d1ed6dc9a85105ae4e8dcfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262055"
---
# <a name="sql-dialect"></a>SQL Dialecto

El SQL, derivado del Lenguaje de consulta estructurado, usa expresiones legibles para definir instrucciones de consulta. Use una instrucción SQL consulta con las siguientes interfaces de búsqueda ADSI:

-   Las [ActiveX de objetos de datos (ADO),](searching-with-activex-data-objects-ado.md) que son interfaces de Automation que usan OLE DB.
-   [OLE DB](searching-with-ole-db.md), que es un conjunto de interfaces de C/C++ para consultar bases de datos.

SQL instrucciones requieren la siguiente sintaxis.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



En la tabla siguiente se enumeran SQL palabras clave de instrucción de consulta.



| Palabra clave  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Especifica una lista separada por comas de atributos que se recuperarán para cada objeto. Si especifica \* , la consulta recupera solo ADsPath de cada objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Especifica el ADsPath de la base de la búsqueda. Por ejemplo, el ADsPath del contenedor Users de un dominio Active Directory podría ser "LDAP://CN=Users,DC=Fabrikam,DC=COM". Tenga en cuenta que la ruta de acceso está entre comillas simples (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Palabra clave opcional que especifica el filtro de consulta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Palabra clave opcional que genera una ordenación del lado servidor si el servidor admite el control de ordenación LDAP. Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande. La lista de ordenación es una lista separada por comas de atributos en los que se va a ordenar. Tenga en cuenta que Active Directory solo admite una única clave de ordenación. Puede usar las palabras clave ASC y DESC opcionales para especificar el criterio de ordenación ascendente o descendente. el valor predeterminado es ascendente. La palabra clave ORDER BY invalida cualquier clave de ordenación especificada con la propiedad "Ordenar por" del objeto Command de ADO. |



 

> [!Note]  
> En los casos en los que se usa un juego de caracteres multibyte, si ADO realiza la búsqueda con el dialecto SQL, no se puede usar una barra diagonal inversa para escapar caracteres. En su lugar, se deben usar las secuencias de escape [enumeradas en](search-filter-syntax.md) Caracteres especiales. Por ejemplo, para una instrucción que usaba la sintaxis "samAccountName= Test", que usa la barra diagonal inversa, " ", para escapar el paréntesis abierto, "(", en su lugar, reemplazaría la barra diagonal inversa por el carácter especial " 28", como se muestra a \( \\ continuación: \\ "samAccountName= \\ 28Test".

 

Las siguientes instrucciones de consulta son ejemplos de SQL dialecto en ADSI.

Para buscar todos los objetos de grupo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Para buscar todos los usuarios cuyo apellido empieza por la letra H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



La gramática formal para SQL consultas se define en el ejemplo de código siguiente. Todas las palabras clave no tienen en cuenta mayúsculas de minúsculas.


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



SQL el proveedor de Active Directory OLE DB no admite las combinaciones internas, pero puede usar SQL para unir SQL y Active Directory datos. Para obtener más información, vea [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de filtro de búsqueda](search-filter-syntax.md)
</dt> <dt>

[Dialecto LDAP](ldap-dialect.md)
</dt> <dt>

[Búsqueda con la interfaz IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Buscar con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




