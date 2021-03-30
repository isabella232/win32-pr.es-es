---
title: Combinar datos heterogéneos
description: Las organizaciones típicas almacenan datos en varias bases de datos heterogéneas. Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio. Otros datos pueden almacenarse en formatos de propiedad.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6d0303ee933b81f0c8553b6b0adae64db7f48d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103904417"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="c9975-105">Combinar datos heterogéneos</span><span class="sxs-lookup"><span data-stu-id="c9975-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="c9975-106">Las organizaciones típicas almacenan datos en varias bases de datos heterogéneas.</span><span class="sxs-lookup"><span data-stu-id="c9975-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="c9975-107">Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio.</span><span class="sxs-lookup"><span data-stu-id="c9975-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="c9975-108">Otros datos pueden almacenarse en formatos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9975-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="c9975-109">Con, SQL Server 7,0, ADSI y el proveedor de OLE DB, es posible combinar datos de Active Directory con los datos de SQL Server y crear una vista de los datos combinados.</span><span class="sxs-lookup"><span data-stu-id="c9975-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="c9975-110">**Para combinar datos de Active Directory con datos de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="c9975-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="c9975-111">Ejecutar el **analizador de consultas de SQL** (iniciar \| programas \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="c9975-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="c9975-112">Inicie sesión en el equipo SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9975-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="c9975-113">Ejecute la línea siguiente (resáltela y presione CTRL + E):</span><span class="sxs-lookup"><span data-stu-id="c9975-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="c9975-114">En esta línea, los argumentos para el procedimiento almacenado del sistema [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9975-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="c9975-115">"ADSI" es el argumento **Server** , que será el nombre de este servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="c9975-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="c9975-116">"Active Directory Services" es el argumento **srvproduct** , que es el nombre del OLE DB origen de datos que se va a agregar como servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="c9975-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="c9975-117">"ADSDSOObject" es el argumento de **\_ nombre de proveedor** e indica que se está usando el proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9975-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="c9975-118">"adsdatasource" es el **\_ argumento de origen de datos**, que es el nombre del origen de datos tal como lo interpreta el proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9975-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="c9975-119">Ahora puede usar el servidor vinculado para obtener acceso a Active Directory desde SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9975-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="c9975-120">En el ejemplo siguiente se realiza una consulta mediante la instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c9975-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="c9975-121">Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que acaba de crear y una instrucción de consulta.</span><span class="sxs-lookup"><span data-stu-id="c9975-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="c9975-122">La instrucción de consulta contiene los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9975-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="c9975-123">La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="c9975-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="c9975-124">Tendrá que usar el nombre para mostrar LDAP para indicar qué datos está buscando.</span><span class="sxs-lookup"><span data-stu-id="c9975-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="c9975-125">La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.</span><span class="sxs-lookup"><span data-stu-id="c9975-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="c9975-126">La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c9975-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="c9975-127">En este ejemplo, está buscando usuarios.</span><span class="sxs-lookup"><span data-stu-id="c9975-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="c9975-128">Escriba y ejecute:</span><span class="sxs-lookup"><span data-stu-id="c9975-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="c9975-129">También puede usar el [dialecto LDAP](ldap-dialect.md)de ADSI.</span><span class="sxs-lookup"><span data-stu-id="c9975-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="c9975-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c9975-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="c9975-131">En el ejemplo anterior, la consulta LDAP tiene cuatro partes:</span><span class="sxs-lookup"><span data-stu-id="c9975-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="c9975-132">" <LDAP://DC=Fabrikam,DC=COM> " es el nombre distintivo del servidor de directorio en el que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="c9975-132">"<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="c9975-133">"(& (objectCategory = person) (objectClass = User))" es el filtro de búsqueda LDAP (consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="c9975-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="c9975-134">"Name, ADsPath" son los nombres (con el formato de nombre para mostrar LDAP) de los atributos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c9975-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="c9975-135">"subárbol" indica el [ámbito](scope-of-query.md) de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c9975-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9975-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9975-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9975-137">Crear y ejecutar una vista</span><span class="sxs-lookup"><span data-stu-id="c9975-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




