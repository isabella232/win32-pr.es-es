---
title: Buscar objetos
description: Julia Bankert debe buscar los números de teléfono de todos los administradores de programas que trabajan en el Departamento 101. Puede crear un script que utilice ADO y ADSI para lograrlo.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- buscar objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103904421"
---
# <a name="searching-for-objects"></a><span data-ttu-id="56d22-105">Buscar objetos</span><span class="sxs-lookup"><span data-stu-id="56d22-105">Searching for Objects</span></span>

<span data-ttu-id="56d22-106">Julia Bankert debe buscar los números de teléfono de todos los administradores de programas que trabajan en el Departamento 101.</span><span class="sxs-lookup"><span data-stu-id="56d22-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="56d22-107">Puede crear un script que utilice ADO y ADSI para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="56d22-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="56d22-108">Cuando se usa el proveedor de ADO para realizar una consulta, el conjunto de resultados solo devolverá los primeros 1000 objetos.</span><span class="sxs-lookup"><span data-stu-id="56d22-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="56d22-109">Por esta razón, es importante usar una consulta paginada para poder recuperar todos los objetos del conjunto de resultados, siempre que no se haya establecido el servicio de directorio para limitar el número de elementos de un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="56d22-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="56d22-110">Los conjuntos de valores devueltos contendrán el número de elementos que se especifican en el tamaño de página y se seguirán devolviendo los conjuntos paginados hasta que se devuelvan todos los elementos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="56d22-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



<span data-ttu-id="56d22-111">Para realizar una búsqueda ADSI en Visual Basic o en un entorno de scripting, se necesitan tres componentes de ADO: **conexión**, **comando** y **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="56d22-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="56d22-112">El objeto de **conexión** le permite especificar el nombre del proveedor, las credenciales alternativas, si procede, y otras marcas.</span><span class="sxs-lookup"><span data-stu-id="56d22-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="56d22-113">El objeto de **comando** permite especificar preferencias de búsqueda y la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="56d22-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="56d22-114">Debe asociar el objeto de **conexión** a un objeto de **comando** antes de la ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="56d22-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="56d22-115">Por último, el objeto de **conjunto de registros** se usa para recorrer en iteración el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="56d22-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="56d22-116">ADSI admite dos tipos de cadenas de consulta o dialectos.</span><span class="sxs-lookup"><span data-stu-id="56d22-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="56d22-117">En el ejemplo de código anterior se usa el dialecto SQL.</span><span class="sxs-lookup"><span data-stu-id="56d22-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="56d22-118">También puede usar el dialecto LDAP.</span><span class="sxs-lookup"><span data-stu-id="56d22-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="56d22-119">La cadena de consulta de dialecto LDAP se basa en [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (una RFC es una solicitud de documento de comentarios, que es la base para desarrollar estándares LDAP).</span><span class="sxs-lookup"><span data-stu-id="56d22-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="56d22-120">El ejemplo anterior se puede traducir en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="56d22-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="56d22-121">¿Por qué aparece la palabra "subárbol" al final de la cadena?</span><span class="sxs-lookup"><span data-stu-id="56d22-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="56d22-122">En el mundo del directorio, puede especificar el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="56d22-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="56d22-123">Las opciones son: "base", "ONELEVEL" y "subárbol".</span><span class="sxs-lookup"><span data-stu-id="56d22-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="56d22-124">"base" se usa para leer el propio objeto; "ONELEVEL" hace referencia a los elementos secundarios inmediatos, similar al comando **dir** ; "subárbol" se usa para buscar varios niveles en profundidad o descendente (similar a **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="56d22-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="56d22-125">Con el dialecto SQL, puede especificar el ámbito en la propiedad Command, como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="56d22-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="56d22-126">Si no se especifica el ámbito, usa de forma predeterminada una búsqueda de subárbol.</span><span class="sxs-lookup"><span data-stu-id="56d22-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="56d22-127">Si usa C++, puede usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) de ADSI.</span><span class="sxs-lookup"><span data-stu-id="56d22-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="56d22-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56d22-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d22-129">Reorganización</span><span class="sxs-lookup"><span data-stu-id="56d22-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




