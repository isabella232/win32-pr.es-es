---
title: Dialecto LDAP
description: El dialecto LDAP es un formato para las instrucciones de consulta que usan la sintaxis de filtro de búsqueda LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI de dialecto LDAP
- dialectos ADSI, dialecto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903046"
---
# <a name="ldap-dialect"></a><span data-ttu-id="462ee-105">Dialecto LDAP</span><span class="sxs-lookup"><span data-stu-id="462ee-105">LDAP Dialect</span></span>

<span data-ttu-id="462ee-106">El dialecto LDAP es un formato para las instrucciones de consulta que usan la [Sintaxis de filtro de búsqueda LDAP](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="462ee-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="462ee-107">Use una instrucción de consulta LDAP con las siguientes interfaces de búsqueda ADSI:</span><span class="sxs-lookup"><span data-stu-id="462ee-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="462ee-108">Interfaces de [objetos de datos ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , que son interfaces de automatización que utilizan OLE DB.</span><span class="sxs-lookup"><span data-stu-id="462ee-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="462ee-109">[OLE DB](searching-with-ole-db.md), que es un conjunto de interfaces de C/C++ para la consulta de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="462ee-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="462ee-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), que es la interfaz de C/C++ para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="462ee-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="462ee-111">Una cadena de dialecto LDAP consta de cuatro partes separadas por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="462ee-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="462ee-112">Nombre distintivo base.</span><span class="sxs-lookup"><span data-stu-id="462ee-112">Base distinguished name.</span></span> <span data-ttu-id="462ee-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="462ee-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="462ee-114">Filtros de búsqueda LDAP.</span><span class="sxs-lookup"><span data-stu-id="462ee-114">LDAP search filters.</span></span> <span data-ttu-id="462ee-115">Para obtener más información sobre los filtros de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="462ee-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="462ee-116">Nombre LDAP para mostrar de los atributos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="462ee-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="462ee-117">Varios atributos se separan mediante una coma.</span><span class="sxs-lookup"><span data-stu-id="462ee-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="462ee-118">Especifica el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="462ee-118">Specifies the scope of the search.</span></span> <span data-ttu-id="462ee-119">Los valores válidos son "base", "ONELEVEL" y "subárbol".</span><span class="sxs-lookup"><span data-stu-id="462ee-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="462ee-120">El ámbito especificado en una cadena de consulta LDAP invalida cualquier ámbito de búsqueda especificado con la propiedad "SearchScope" del objeto de comando de ADO.</span><span class="sxs-lookup"><span data-stu-id="462ee-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="462ee-121">El siguiente es un ejemplo de código del dialecto LDAP en ADSI que busca en todos los objetos del subárbol.</span><span class="sxs-lookup"><span data-stu-id="462ee-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="462ee-122">No todas las opciones de búsqueda (por ejemplo, el tamaño de la página de búsqueda) se pueden expresar en el dialecto LDAP, por lo que debe establecer las opciones antes de que se inicie la ejecución real de la consulta.</span><span class="sxs-lookup"><span data-stu-id="462ee-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="462ee-123">Código de ejemplo para realizar una consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="462ee-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="462ee-124">En el ejemplo de código siguiente se muestra cómo usar una consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="462ee-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="462ee-125">Para obtener más información sobre la sintaxis de consulta, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="462ee-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="462ee-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="462ee-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="462ee-127">Sintaxis de filtro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="462ee-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="462ee-128">Dialecto SQL</span><span class="sxs-lookup"><span data-stu-id="462ee-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="462ee-129">Buscar con la interfaz IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="462ee-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="462ee-130">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="462ee-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="462ee-131">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="462ee-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




