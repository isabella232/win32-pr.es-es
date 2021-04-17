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
# <a name="sql-dialect"></a><span data-ttu-id="a1377-105">Dialecto SQL</span><span class="sxs-lookup"><span data-stu-id="a1377-105">SQL Dialect</span></span>

<span data-ttu-id="a1377-106">El dialecto SQL, derivado del Lenguaje de consulta estructurado, utiliza expresiones legibles para el usuario para definir instrucciones de consulta.</span><span class="sxs-lookup"><span data-stu-id="a1377-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="a1377-107">Use una instrucción de consulta SQL con las siguientes interfaces de búsqueda ADSI:</span><span class="sxs-lookup"><span data-stu-id="a1377-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="a1377-108">Interfaces de [objetos de datos ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , que son interfaces de automatización que utilizan OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a1377-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="a1377-109">[OLE DB](searching-with-ole-db.md), que es un conjunto de interfaces de C/C++ para la consulta de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a1377-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="a1377-110">Las instrucciones SQL requieren la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="a1377-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="a1377-111">En la tabla siguiente se enumeran las palabras clave de instrucción de consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="a1377-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="a1377-112">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="a1377-112">Keyword</span></span>  | <span data-ttu-id="a1377-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1377-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1377-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="a1377-114">SELECT</span></span>   | <span data-ttu-id="a1377-115">Especifica una lista separada por comas de los atributos que se van a recuperar para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="a1377-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="a1377-116">Si especifica \* , la consulta solo recupera el ADsPath de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="a1377-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a1377-117">FROM</span><span class="sxs-lookup"><span data-stu-id="a1377-117">FROM</span></span>     | <span data-ttu-id="a1377-118">Especifica el ADsPath de la base de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a1377-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="a1377-119">Por ejemplo, la ADsPath del contenedor de usuarios en un dominio de Active Directory podría ser "LDAP:Rio = users, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="a1377-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="a1377-120">Tenga en cuenta que la ruta de acceso está delimitada por un par de comillas simples (').</span><span class="sxs-lookup"><span data-stu-id="a1377-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a1377-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="a1377-121">WHERE</span></span>    | <span data-ttu-id="a1377-122">Palabra clave opcional que especifica el filtro de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a1377-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a1377-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="a1377-123">ORDER BY</span></span> | <span data-ttu-id="a1377-124">Palabra clave opcional que genera una ordenación del lado servidor si el servidor admite el control de ordenación LDAP.</span><span class="sxs-lookup"><span data-stu-id="a1377-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="a1377-125">Active Directory admite el control de ordenación, pero puede afectar al rendimiento del servidor, especialmente si el conjunto de resultados es grande.</span><span class="sxs-lookup"><span data-stu-id="a1377-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="a1377-126">La lista de ordenación es una lista separada por comas de atributos por los que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="a1377-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="a1377-127">Tenga en cuenta que Active Directory solo admite una única clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="a1377-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="a1377-128">Puede usar las palabras clave ASC y DESC opcionales para especificar el criterio de ordenación ascendente o descendente. el valor predeterminado es Ascending.</span><span class="sxs-lookup"><span data-stu-id="a1377-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="a1377-129">La palabra clave ORDER BY invalida cualquier clave de ordenación especificada con la propiedad "Sort on" del objeto Command de ADO.</span><span class="sxs-lookup"><span data-stu-id="a1377-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a1377-130">En los casos en los que se usa un juego de caracteres multibyte, si ADO realiza la búsqueda con el dialecto SQL, no se puede utilizar una barra diagonal inversa para los caracteres de escape.</span><span class="sxs-lookup"><span data-stu-id="a1377-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="a1377-131">En su lugar, se deben usar las secuencias de escape que se enumeran en [caracteres especiales](search-filter-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="a1377-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="a1377-132">Por ejemplo, para una instrucción que usaba la sintaxis "samAccountName = \( Test", que usa la barra diagonal inversa, " \\ ", para escapar el paréntesis de apertura, "(", en su lugar, reemplazaría la barra diagonal inversa por el carácter especial " \\ 28", como se indica a continuación: "samAccountName = \\ 28Test".</span><span class="sxs-lookup"><span data-stu-id="a1377-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="a1377-133">Las siguientes instrucciones de consulta son ejemplos de dialecto SQL en ADSI.</span><span class="sxs-lookup"><span data-stu-id="a1377-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="a1377-134">Para buscar todos los objetos de grupo.</span><span class="sxs-lookup"><span data-stu-id="a1377-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="a1377-135">Para buscar todos los usuarios cuyo apellido empieza por la letra H.</span><span class="sxs-lookup"><span data-stu-id="a1377-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="a1377-136">La gramática formal de las consultas SQL se define en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a1377-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="a1377-137">Todas las palabras clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a1377-137">All keywords are case-insensitive.</span></span>


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



<span data-ttu-id="a1377-138">Las combinaciones internas de SQL no son compatibles con el proveedor de OLE DB de Active Directory, pero puede usar SQL para combinar datos de SQL y Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1377-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="a1377-139">Para obtener más información, vea [crear una combinación heterogénea entre SQL Server y Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="a1377-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1377-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1377-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1377-141">Sintaxis de filtro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="a1377-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="a1377-142">Dialecto LDAP</span><span class="sxs-lookup"><span data-stu-id="a1377-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="a1377-143">Buscar con la interfaz IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a1377-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="a1377-144">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="a1377-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="a1377-145">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1377-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




